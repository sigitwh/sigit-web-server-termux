# sigit-web-server-termux

Pertama-tama lakukan update terlebih dahulu dengan perintah:<br>
<code>
  pkg update
  </code><br>&nbsp;<br>
Kemudian lakukan instalasi PHP dengan perintah: <br>
<code>pkg install php</code><br>&nbsp;<br>

Cek apakah instalasi berhasil dengan perintah: <br>
<code>php -v</code>

Jika berhasil akan muncul keterangan

Install web server apache dengan perintah: <br>
<code>pkg install apache2</code>

Setelah itu buat sebuah direktory atau folder bernama www dengan perintah:<br>
<code>mkdir www</code>

Kemudian buat sebuah file uji coba bernama index.php dengan perintah:<br>
<code>nano www/index.php</code>

Ketiklah:
<code>php phpinfo(); </code>

Jalankan PHP dengan perintah:
<code>php -S localhost:8080 -t www</code>

