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

Jalankan PHP dengan perintah:<br>
<code>php -S localhost:8080 -t www</code>

Jika ingin PHP dapat dibuka di HP/komputer/device lain, gunakan perintah:<br>
<code>php -S 0.0.0.0:8080 -t www<code>

  <h1>Instalasi MariaDB</h1>
  
 Install MariaDb dengan perintah: <br>
  <code>pkg install madiadb</code>
  
  Ketikkan perintah: <br>
  <code>mysqld_safe -u root &</code>
  
  Ubah password root: <br>
  <code>mysql -u $(whoami)
  
  use mysql;
set password for 'root'@'localhost' = password('1234');
flush privileges;
quit;</code>
