Pertanyaan super penting, Alwi! Saat backend-nya sudah jadi (pakai GraphQL), maka **frontend-nya akan "hit" API GraphQL hanya ke satu endpoint**:

```
POST http://localhost:4000/graphql
```

Namun **query atau mutation-nya** dikirim dalam bentuk **body JSON**, bukan URL seperti REST biasa.

---

## 🔥 Contoh Frontend Hit API GraphQL

### 🔹 1. **Gunakan `fetch` (Vanilla JavaScript)**

#### ✅ Query ambil semua buku:

```js
fetch('http://localhost:4000/graphql', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    query: `
      {
        books {
          id
          title
          author
        }
      }
    `
  })
})
.then(res => res.json())
.then(data => console.log(data.data.books));
```

---

#### ✅ Mutation untuk tambah buku:

```js
fetch('http://localhost:4000/graphql', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    query: `
      mutation {
        addBook(title: "The Pragmatic Programmer", author: "Andy Hunt") {
          id
          title
          author
        }
      }
    `
  })
})
.then(res => res.json())
.then(data => console.log(data.data.addBook));
```

---

## 🔧 Kalau Pakai Framework Modern (React + Apollo)

### 2. **Contoh Pakai Apollo Client (React)**

#### a. Install dulu:

```bash
npm install @apollo/client graphql
```

#### b. Setup client:

```jsx
// ApolloProvider.jsx
import { ApolloClient, InMemoryCache, ApolloProvider } from '@apollo/client';

const client = new ApolloClient({
  uri: 'http://localhost:4000/graphql',
  cache: new InMemoryCache()
});

export default function AppProvider({ children }) {
  return <ApolloProvider client={client}>{children}</ApolloProvider>;
}
```

#### c. Gunakan query:

```jsx
// BookList.jsx
import { gql, useQuery } from '@apollo/client';

const GET_BOOKS = gql`
  query {
    books {
      id
      title
      author
    }
  }
`;

export default function BookList() {
  const { data, loading } = useQuery(GET_BOOKS);
  if (loading) return <p>Loading...</p>;
  return (
    <ul>
      {data.books.map(b => (
        <li key={b.id}>{b.title} - {b.author}</li>
      ))}
    </ul>
  );
}
```

#### d. Mutation (Tambah Buku)

```jsx
import { gql, useMutation } from '@apollo/client';

const ADD_BOOK = gql`
  mutation($title: String!, $author: String!) {
    addBook(title: $title, author: $author) {
      id
      title
      author
    }
  }
`;

export default function AddBook() {
  const [addBook] = useMutation(ADD_BOOK);
  return (
    <button onClick={() => addBook({ variables: { title: "Clean Code", author: "Uncle Bob" } })}>
      Tambah Buku
    </button>
  );
}
```

---

## 🔐 Catatan Penting:

* Kamu hanya **hanya perlu 1 endpoint**: `/graphql`
* Semua request (query atau mutation) dikirim via **HTTP POST**
* Bisa kirim variabel juga untuk input yang dinamis
* Mendukung integrasi dengan REST API lain jika diperlukan

---

Kalau kamu pakai frontend lain (Vue, Next.js, React Native, dsb.), aku bisa bantu sesuaikan.

Kamu mau aku bantu buatkan contoh full stack React + GraphQL-nya? Atau kita lanjut ke integrasi auth/jwt-nya dulu?
