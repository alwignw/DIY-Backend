Oke Alwi, kita bahas bagaimana cara integrasi **GraphQL + PostgreSQL menggunakan Sequelize**, **termasuk dengan raw query**.

---

### 🧱 Arsitektur yang Akan Kita Bangun

| Komponen         | Teknologi                                |
| ---------------- | ---------------------------------------- |
| Server           | Express.js + express-graphql             |
| ORM              | Sequelize (akses DB PostgreSQL)          |
| DB               | PostgreSQL                               |
| GraphQL Query    | Ambil data dari Sequelize                |
| GraphQL Mutation | Insert ke DB (pakai Sequelize / raw SQL) |

---

## 🔧 Langkah-langkah Setup: GraphQL + Sequelize + PostgreSQL

---

### 🔹 1. Inisialisasi Proyek

```bash
mkdir graphql-sequelize
cd graphql-sequelize
npm init -y
npm install express express-graphql graphql sequelize pg pg-hstore
```

---

### 🔹 2. Setup Sequelize

```bash
npx sequelize-cli init
```

Akan muncul folder:

```
config/
models/
migrations/
seeders/
```

Edit `config/config.json`:

```json
{
  "development": {
    "username": "postgres",
    "password": "yourpassword",
    "database": "graphql_books",
    "host": "127.0.0.1",
    "dialect": "postgres"
  }
}
```

---

### 🔹 3. Buat Tabel Buku

```bash
npx sequelize-cli model:generate --name Book --attributes title:string,author:string
```

Jalankan migrasi:

```bash
npx sequelize-cli db:migrate
```

---

### 🔹 4. Buat Server GraphQL (`index.js`)

```js
const express = require('express');
const { graphqlHTTP } = require('express-graphql');
const {
  GraphQLSchema,
  GraphQLObjectType,
  GraphQLString,
  GraphQLList,
  GraphQLInt
} = require('graphql');

const db = require('./models'); // Sequelize models

// BookType GraphQL
const BookType = new GraphQLObjectType({
  name: 'Book',
  fields: {
    id: { type: GraphQLInt },
    title: { type: GraphQLString },
    author: { type: GraphQLString }
  }
});

// Query
const RootQuery = new GraphQLObjectType({
  name: 'Query',
  fields: {
    books: {
      type: new GraphQLList(BookType),
      resolve: () => db.Book.findAll()
    },
    book: {
      type: BookType,
      args: { id: { type: GraphQLInt } },
      resolve: (_, args) => db.Book.findByPk(args.id)
    }
  }
});

// Mutation
const RootMutation = new GraphQLObjectType({
  name: 'Mutation',
  fields: {
    addBook: {
      type: BookType,
      args: {
        title: { type: GraphQLString },
        author: { type: GraphQLString }
      },
      resolve: (_, args) => db.Book.create({ title: args.title, author: args.author })
    }
  }
});

const schema = new GraphQLSchema({
  query: RootQuery,
  mutation: RootMutation
});

const app = express();
app.use('/graphql', graphqlHTTP({
  schema,
  graphiql: true
}));

app.listen(4000, () => {
  console.log('Server running on http://localhost:4000/graphql');
});
```

---

### 🔥 BONUS: Pakai **Raw Query** dengan Sequelize

Kalau kamu mau gunakan SQL langsung tanpa ORM, Sequelize mendukung ini via `sequelize.query()`:

#### Contoh dalam resolver `books`:

```js
books: {
  type: new GraphQLList(BookType),
  resolve: async () => {
    const [results] = await db.sequelize.query("SELECT * FROM \"Books\" ORDER BY id DESC");
    return results;
  }
}
```

#### Contoh `insert` via raw query:

```js
addBook: {
  type: BookType,
  args: {
    title: { type: GraphQLString },
    author: { type: GraphQLString }
  },
  resolve: async (_, args) => {
    const [result] = await db.sequelize.query(
      `INSERT INTO "Books" (title, author, "createdAt", "updatedAt") 
       VALUES (:title, :author, NOW(), NOW()) 
       RETURNING *`,
      {
        replacements: { title: args.title, author: args.author },
        type: db.Sequelize.QueryTypes.INSERT
      }
    );
    return result[0]; // hasilnya array
  }
}
```

---

### 🔚 Kesimpulan

✅ **Sequelize** memberikan kemudahan:

* Bisa pakai ORM (model-based) ✅
* Bisa pakai raw query untuk custom SQL ✅
* Kompatibel banget buat proyek skala kecil sampai enterprise ✅

---

Kamu ingin aku bantu buatkan boilerplate project dari awal pakai Sequelize + GraphQL?
Atau ingin contoh implementasi `update` dan `delete` juga?
