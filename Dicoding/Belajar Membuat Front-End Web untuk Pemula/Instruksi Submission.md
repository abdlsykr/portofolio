# Submission: Membangun Bookshelf App

Buatlah aplikasi web yang dapat **memasukkan data buku ke dalam rak**, **memindahkan data buku antar rak**, dan **menghapus data buku dari rak**.

Untuk lebih jelasnya, ada lima kriteria wajib yang harus Anda penuhi.

## Kriteria Wajib 1: Gunakan localStorage sebagai Penyimpanan
Data buku yang ditampilkan pada rak-rak harus dapat bertahan walaupun halaman web ditutup. Dengan begitu, Anda harus menyimpan data buku pada **localStorage**.

Setiap buku harus berupa **objek JavaScript** dengan struktur berikut:

```json
{
  "id": string | number,
  "title": string,
  "author": string,
  "year": number,
  "isComplete": boolean
}
```

### Contoh Data Buku:
```json
{
  "id": 3657848524,
  "title": "Harry Potter and the Philosopher's Stone",
  "author": "J.K Rowling",
  "year": 1997,
  "isComplete": false
}
```

## Kriteria Wajib 2: Mampu Menambahkan Buku
Aplikasi harus mampu **menyimpan buku baru** menggunakan formulir yang telah disediakan dalam starter project.

- **ID buku** harus dihasilkan secara otomatis dan unik. Tips: gunakan **timestamp** dengan `new Date().getTime()` atau `Number(new Date())`.
- Formulir setidaknya bisa menghasilkan empat data berikut:
  - `title`: judul buku.
  - `author`: penulis buku.
  - `year`: tahun rilis buku (tipe number).
  - `isComplete`: kondisi apakah sudah selesai dibaca atau belum.

## Kriteria Wajib 3: Memiliki Dua Rak Buku
Aplikasi wajib memiliki **2 rak buku**, yakni:

- **“Belum selesai dibaca”** → Menyimpan buku dengan `isComplete: false`.
- **“Selesai dibaca”** → Menyimpan buku dengan `isComplete: true`.

## Kriteria Wajib 4: Dapat Memindahkan Buku Antar Rak
Buku-buku dalam rak harus dapat **dipindahkan ke rak lainnya**, baik **“Belum selesai dibaca”** maupun **“Selesai dibaca”**.

Pastikan perubahan ini **tersimpan dalam localStorage**.

## Kriteria Wajib 5: Dapat Menghapus Data Buku
Buku yang ditampilkan pada rak harus dapat **dihapus**. Selain menghilang dari halaman, data buku dalam **localStorage juga harus terhapus**.
