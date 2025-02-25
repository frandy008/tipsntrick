# Membuat docker image dari compiled / executeable file berdasarkan Alpine Image

Pertama untuk settingan pkg pada package.json nya sendiri seperti di bawah :
```
"pkg": {
    "scripts": "build/**/*.js",
    "assets": [
      "bisa di sesuaikan dengan directory masing-masing"
    ],
    "targets": [
      "node18-linux-x64"
    ],
    "outputPath": "dist",
    "config": {
      "noBytecode": true
    }
  }
```

kemudian jika sudah jadi bisa buat Dockerfile pada folder dist atau di sesuaikan dengan masing-masing, isi nya kira-kira seperti berikut : 
```
FROM alpine:latest

WORKDIR /app

RUN apk add --no-cache libc6-compat libstdc++ libgcc

COPY nama-image-nya .

RUN chmod +x nama-image-nya && ls -lah

ENTRYPOINT ["./nama-image-nya"]
```

selamat kamu sudah berhasil menjalankan nya
