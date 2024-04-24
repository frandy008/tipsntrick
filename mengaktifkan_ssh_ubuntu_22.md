<h2>Cara Install dan mengaktifkan SSH di Ubuntu 22</h2>

Pertama update dan upgrade :
```
sudo apt update && sudo apt upgrade
```

Install terlebih dahulu open SSH Server :
```
sudo apt install openssh-server
```

Aktifkan SSH Server dengan :
```
sudo systemctl enable --now ssh
```

Menambahkan SSH ke firewall :
```
sudo ufw allow ssh
```

Menyesuaikan sedikit config nya.
Pertama backup terlebih dahulu config default nya :
```
sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.initial
```
Buka config nya dengan editor kalian:
```
sudo nano /etc/ssh/sshd_config
```

Cari dan sesuaikan baris-baris di bawah:
```
PubkeyAuthentication yes
PermitRootLogin yes
```

Setelah melakukan pembaruan, jangan lupa restart service nya:
```
sudo systemctl restart ssh
```

<h2>Mengatasi Error remote host identification has changed windows</h2>
Cara nya cukup simple dengan cara melakukan reset :

```
ssh-keygen -R [hostname or IP address]
```
