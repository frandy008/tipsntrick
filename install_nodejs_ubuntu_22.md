<h2>Cara Install Node JS dengan NVM</h2>

Pertama-tama silahkan update dan upgrade :
```
sudo apt-get update && sudo apt-get upgrade -y
```

Jika belum ada CURL kita bisa install dulu dengan perintah :
```
sudo apt install curl
```
Kemudian :
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

Kemudian kita tambahkan NVM ke dalam environment ubuntu dengan cara :
```
source ~/.bashrc
```

Untuk melihat versi Node JS dengan NVM bisa gunakan perintah :
```
nvm ls-remote
```

Untuk menginstall versi terakhir gunakan :
```
nvm install --lts
```

Untuk install versi tertentu gunakan :
```
nvm install v20.9.0
```
Tunggu proses hingga selesai.

Kemudian untuk mengecek versi bisa gunakan :
```
node -v
npm -v
```
