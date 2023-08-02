# Menghapus Node Modules di Git Repositori

Tutorial kali ini bagaimana untuk menghapus folder `node_modules` yang sudah terlanjur ke _upload_ saat _push_ ke repositori.

## 1. Buat File `.gitignore`
1. Cek apakah file `.gitignore` sudah ada
```bash
ls -a
```
2. Jika file `.gitignore` sudah ada, maka lewati langkah ini
```bash
# create .gitignore file
touch .gitignore
```

## 2. Menghapus Direktori `node_modules`
1. Buka file `.gitignore` dan tambahkan kode seperti berikut
```bash
**/node_modules
```
2. Menghapus direktori `node_modules` dari repositori git
```bash
git rm -r --cached node_modules
```

## 3. Commit Semua Perubahan
1. Commit repositori git tanpa direktori `node_modules`
```bash
git commit -m "remove node_modules folder"
```
2. Push perubahan ke repositori remote
```bash
git push origin main
```
3. Commit file `.gitignore`
```bash
git add .gitignore
git commit -m "updated .gitignore file"
git push origin main
```