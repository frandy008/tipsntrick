<h2>Cara Install dan menggunakan PM2</h2>

Pertama-tama kalian harus mempunyai NPM, biasa nya langsung terinstall saat menginstall Node JS.
Lanjut ke langkah selanjut nya jika kalian sudah punya NPM, jika belum bisa Install Node JS terlebih dahulu.

<h2>Tutorial di Windows</h2>
Install PM2 melalui NPM :

```
npm install -g pm2
```

Untuk windows kita juga harus menginstall package di bawah :
```
npm install -g pm2-windows-startup
```

Cara untuk menambahkan aplikasi :
```
pm2 start <path lengkap aplikasi> -n <nama alias>
```

Untuk menjalankan saat start-up gunakan perintah :
```
pm2-startup install
```

Saat melakukan perubahan ingat menyimpan dengan perintah :
```
pm2 save
```

<h2>Tutorial di Ubuntu</h2>
Install PM2 melalui NPM

```
npm install -g pm2
```

Tambahkan aplikasi dengan cara :
```
pm2 start <path lengkap aplikasi> -n <nama alias>
```

Jangan lupa menambahkan hak izin sebelum menambahkan aplikasi ke PM2 :
```
chmod +x <path aplikasi>
```

Untuk menambahkan ke start-up bisa gunakan :
```
pm2 startup
```



<h2>Perintah-perintah yang terdaftar</h2>

```
pm2 start <alias> //Untuk menambahkan atau menjalankan aplikasi
pm2 stop <alias atau id> untuk menghentikan aplikasi
pm2 restart <alias atau id> untuk melakukan restart aplikasi
pm2 delete <alias atau id> untuk menghapus aplikasi dari PM2
```


## Melihat log nya bisa melalui folder
```
~/.pm2/logs/
```
