# Belajar Bash Script

## 1 *Shell Script*

*Shell* adalah program yang mana perannya sebagai perantara antara user dengan sistem operasi. beberapa *shell* yang ada pada linux adalah :

* Bourne again shell (bash) ---> nanti saya akan menggunakan ini
* Korn shell (ksh)
* Bourne shell (sh)
* C shell (csh)

*Shell* selalu diawali dengan komentar, yang mana dimulai dengan tanda `#` disambung dengan `!` dan nama shell yang digunakan.
```
#!/bin/sh         1
# Program shell   2
#
var1=x            3
var2=8
```
Penjelasan:	

* Pada nomer 1 merupakan awal dari program shell, dimana komentar awal akan dibaca oleh sistem, lalu sistem mengaktifkan  program *shell* `( /bin/sh)` yang telah dibuat. 

* Pada nomer 2 merupakan komentar, ini sebagai komentar atau dokumentasi saja, baris ini diabaikan oleh program *shell*.

* Pada nomer 3 merupakan variabel, pada penggunaan variabel tidak boleh ada spasi.

## 2 *Variabel*
Variabel shell adalah variabel yang memiliki nilai String.
Sintaks sebagai berikut:
`nama_variabel = nilai_variabel`
nama variabel harus dimulai dengan alfabet, lalu ditambahkan karakter lain. nama variabel dapat ditulis dengan huruf kapital atau huruf kecil atau bisa dengan campuran antara keduanya. Shell termasuk case sensitive, karena huruf kapital dan huruf kecil dianggap berbeda.
contoh:
```
var_saya=bash
var_coba="Hallo Worrld, ini adalah bahasa bash"
```
inisialiasi variabel tidak boleh dipisahkan dengan spasi, karena dianggap sebagai parameter
```
var_saya= bash  #Error
var_saya =bash  #Error
```
tanda *$* untuk mengetahui nilai dari variabel. untuk instruksi bisa menggunakan *echo* untuk menampilkan nilai dari variabel.
```
var_saya=bash
var_coba="Hallo Worrld, ini adalah bahasa bash"
echo $var_saya
echo $var_coba
```
