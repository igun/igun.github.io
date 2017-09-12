---
categories:
  - Others
tags:
  - hugo
  - syntax highlighting
  - prism.js
title: "Test-Code-Syntax-Highlight"
slug: "Test syntax highlight"
date: "2017-09-12T22:50:59+07:00"
draft: false
---

## Percobaan Syntax Highlighting

Saya mencoba mengikuti tutorial untuk syntax highlighting menggunakan prim.js. Langsung saja kita tampilkan hasilnya adalah sebagai berikut:

Ini code untuk CSS

<pre>
  <code class="language-css">
  body {
    font-family: "Noto Sans", sans-serif;
  }
  </code>
</pre>


Ini code untuk Python

<pre>
  <code class="language-python">
  >>> from pygments.styles import get_all_styles
  >>> styles = list(get_all_styles())
  >>> print styles
  </code>
</pre>


Sekarang adalah code untuk MySQL yang belum ada di daftar prism saya:

<pre>
  <code class="language-sql">
  CREATE DATABASE testing;
  USE testing;
  CREATE TABLE coba (
  	id int,
  	nama varchar(255)
  );
  SELECT * from coba;
  </code>
</pre>


Apakah berhasil?
