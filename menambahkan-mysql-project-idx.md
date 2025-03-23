# Cara menambahkan MySQL di Project IDX

tambahkan kode di bawah ini ke dalam file .idx/dev.nix
tambahkan di block scope pkgs.
```
services.mysql = {
  enable = true;
  package = pkg.mariadb;
}
```

kemudian Rebuild Environment.
jika sudah maka siap digunakan.

untuk user dan password nya default.
```
mysql -u root
```
