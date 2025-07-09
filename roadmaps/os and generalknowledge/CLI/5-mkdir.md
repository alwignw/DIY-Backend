mkdir = make directory

untuk membuat directory baru dalam sistem file

`mkdir [options] nama_direktori`


`-p`: Membuat direktori beserta semua direktori induk yang belum ada. Ini akan membuat semua direktori yang diperlukan dalam jalur yang diberikan.
mkdir -p /path/ke/direktori/baru

`-m`: Mengatur izin (permissions) pada direktori yang baru saja dibuat.
mkdir -m 755 nama_direktori

`-v` :  menampilkan info
`mkdir -v lalal`

membuat folder tersembunyi
`mkdir .foldertersembunyi`

membuat folder space
`mkdir 'react js'`
`mkdir react\ js`
`mkdir "react js"`


membuat dua folder dengan 1 command :  
`mkdir /anime/{'naruto shipudden' , 'draggon ball'}`