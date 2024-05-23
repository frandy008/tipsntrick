<h2>Cara install Portainer Community Edition di Ubuntu 22.04</h2>
1. Update repository

```
sudo apt update
```

2. Install Docker

```
sudo apt install docker.io -y
```

3. Jalankan docker jika belum running

```
sudo systemctl start docker
```

4. Berikan akses usergroup

```
sudo usermod -aG docker $USER
```

5. Install Portainer di Docker

```
docker pull portainer/portainer-ce:latest
```

6. Jalankan Portainer, sesuaikan port nya

```
docker run -d -p 9000:9000 --restart always -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer-ce:latest
```

7. Cek Status nya dengan perintah

```
docker ps
```

Untuk mengakes portainer (default port 9000)
```
http://alamatip:port
```

☕ **Jangan lupa traktir kopi ada di home page github** ☕
<br>
[![Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-☕-brightgreen)](https://github.com/frandy008)

