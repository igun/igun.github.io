---
categories:
  - Sysadmin
tags:
  - linux
  - centos
  - quickie
title: "Mencari File di Linux menggunakan find"
slug: "linux find"
date: "2018-01-02T12:55:32+07:00"
draft: false
---

Mencari file-file di operating system linux (command line) merupakan suatu pekerjaan yang membutuhkan trik khusus, yaitu menggunakan perintah "find". Beberapa perintah yang bisa dilakukan dengan **find** adalah sebagai berikut: 

1 . Mencari berdasar nama file:

```
# find -name nama_file
```

2 . Mencari berdasar ukuran file:

file berukuran tepat 50 Megabytes
```
# find -size 50M
```

file berukuran kurang dari 100 Megabytes
```
# find -size -100M
```

file berukuran lebih dari 200 Megabytes
```
# find -size +200M
```


3 . Mencari berdasar data waktu sebuah file:

Operating system Linux menyimpan data waktu berupa:

- Access Time: waktu terakhir file dibaca atau ditulis
- Modification Time: waktu terakhir isi dari file diubah
- Change Time: waktu terakhir inode metadata dari sebuah file diubah

file yang mempunyai modification time sehari yang lalu
```
# find -mtime 1
```

file yang mempunyai access time kurang dari sehari
```
# find -atime -1
```

file yang mempunyai perubahan metadata lebih dari tiga hari
```
# find -ctime +3
```

Bisa juga menggunakan patokan menit
```
# find -mmin -30
```


4 . Mencari berdasar pemilik dan permission dari file:

file berdasarkan user syslog
```
# find -user syslog
```

file berdasarkan group shadow
```
# find -group shadow
```

file berdasarkan mempunyai set permission 644
```
# find -perm 644
```

file berdasarkan mempunyai set permission minimal 644
```
# find -perm -644
```

### Mencari file lalu mengkombinasikan dengan perintah lain

```
# find find_parameters -exec command_and_params {} \;
```

Contohnya:

Mencari file yang mempunyai set permission 644 kemudian diganti menjadi 664
```
# find . -type f -perm 644 -exec chmod 664 {} \;
```
