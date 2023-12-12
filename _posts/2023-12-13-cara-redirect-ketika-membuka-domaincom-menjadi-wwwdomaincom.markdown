---
layout: post
title:  "Cara redirect ketika membuka domain.com menjadi www.domain.com"
date:   2023-12-13
categories: Tutorial
---

# Cara redirect ketika membuka domain.com menjadi www.domain.com


Pertama-tama ini mungkin sebuah artikel untuk mewakili semua artikel
yang akan kami posting selanjutnya di EDGE Zine, dan semoga artikel ini
juga menjadi awal baik untuk kedepannya. ^_^

# Content


Pada artikel ini mungkin sebagian dari kalian sudah pada tau caranya
dan memang ada banyak sekali cara untuk melakukannya. Disini kami
menjelaskan ulang cara untuk melakukan redirect domain.com ke www.domain.com


Sebenarnya cara yang paling mudah adalah setting melalui cpanel bagi yang
hostingnya menggunakan cpanel dan dijamin anti gagal kalau setting dari cpanel.
Nah sedangkan cara yang akan kami jelaskan pada artikel ini adalah setting redirect
domain melalui .htaccess


Masukan code dibawah ini kedalam file .htaccess di folder public_html :

```ruby
RewriteEngine On
Options +FollowSymlinks
RewriteCond %{HTTP_HOST} ^domain\.com
RewriteRule ^(.*)$ http://www.domain.com/$1 [R=permanent,L]
```


Untuk penulisan nama domain silahkan sesuaikan dengan nama domain kalian ya sob.
