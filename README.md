==== update 27 Oktober 2022 ===
termux sudah tidak disupport lagi
kemungkinan tutorial yang ada di sini sudah tidak bisa digunakan

# sigit-web-server-termux

==== update 18 September 2021 ====

Pertama-tama lakukan update terlebih dahulu dengan perintah:

<code> pkg update </code> 

install apache2 dengan perintah:

<code>pkg install apache2</code>

setelah berhasil di install, jalankan apache dengan perintah:

<code>apachectl start</code>

hasilnya lihat melalui browser dengan alamat:

<code>http://localhost:8080</code>

secara default apache menggunakan file index.htm yang berlokasi di:

/data/data/com.termux/files/usr/share/apache2/default-site/htdocs

Kemudian lakukan instalasi PHP dengan perintah:

<code>pkg install php</code>

Cek apakah instalasi berhasil dengan perintah: <br>
<code>php -v</code>

Jika berhasil akan muncul keterangan versi PHP

Kemduian lakukan instalasi modul php-apache dengan perintah:

<code>pkg install php-apache</code>

Sampai disini apache biasanya belum bisa menjalankan PHP sehingga perlu dilakukan beberapa pengaturan

Edit konfigurasi apache pada file httpd.conf yagn ada di lokasi:

/data/data/com.termux/files/usr/etc/apache2

Untuk mengedit lakukan perintah:

<code>nano /data/data/com.termux/files/usr/etc/apache2/httpd.conf</code>

Lakukan mencarian dengan menekan tombol <code>Ctrl+w</code>, ketik kata kunci LoadModule, lalu enter
Aktifkan module mod_mpm_prefork.so
Non aktifkan module mod_mpm_worker.so

Tambahkan modul PHP dengan cara menambahkan perintah

<code>LoadModule php_module libexec/apache2/libphp.so</code>

Perintah tersebut apabila menggunakan PHP versi 8, untuk PHP versi lain silahkan disesuaikan




====================================
Setelah itu buat sebuah direktory atau folder bernama www dengan perintah:<br>
<code>mkdir www</code>

Kemudian buat sebuah file uji coba bernama index.php dengan perintah:<br>
<code>nano www/index.php</code>

Ketiklah:
<code>php phpinfo(); </code>

Jalankan PHP dengan perintah:<br>
<code>php -S localhost:8080 -t www</code>

Jika ingin PHP dapat dibuka di HP/komputer/device lain, gunakan perintah:<br>
<code>php -S 0.0.0.0:8080 -t www</code>

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
