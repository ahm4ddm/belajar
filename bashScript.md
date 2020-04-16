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
