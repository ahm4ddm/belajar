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

## 2 *Variable*
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
## 3 User Input
Jika kita akan membuat pertanyaan dari user, kita bisa menggunakan perintah `read`. perintah tersebut digunakan untuk mengambil masukkan dari pengguna dan akan disimpan didalam variabel.
Sintaks:
`read namaVariabel`
contoh:
```
echo "Hallo, Anda siapa?"
read varNama
echo "Senang bertemu dengan kamu $varNama"
```
Anda dapat mengganti perilaku dari `read` dengan berbagai parameter. Terdapat banyak parameter, tapi saya akan menggunakan 2 parameter yang sering digunakan yaitu *-P* dimana digunakan untuk menentukan perintah yang spesifik dan *-s* digunakan untuk membuat masuukan tidak terlihat (input password).
```
read -p 'user: ' userVariable
read -sp 'password: ' passwordVariable
echo "user $userVariable berhasil login" 
```

## 4  Arithmetic
Untuk melakukan aritmatika sederhana, kita bisa menggunakan fungsi bawaan dari Bash yaitu `let`. 
Sintaks:
`let <arithmetic expression>`
contoh:
```
let varA=5+4
echo $varA #Hasil 9

let "varB = 4 + 4"
echo $varB #Hasil 8

let "varC = $2 + 10"
echo $varC #Hasil 10
```
Ada juga yaitu `expr` yang mana mirip dengan `let`. perbedaannya adalah `expr` langsung mencetak jawaban kalau `let` disimpan dahulu hasilnya ke variabel.
Sintaks:
`expr item1 operator item2`
contoh:
```
expr 5+4 #Hasil 5+4

expr 5 + 4 #Hasil 9

expr "5 + 10" #Hasil 5 + 4

a=$(expr 10 - 3)
echo $a #Hasil 7
```
Jika Anda ingin mengetahui panjang variabel (length), Anda bisa menggunakan `${#variabel}`
contoh:
```
x="Hallo World"
echo ${#x} #length = 11

y=404
echo ${#y} #length = 3

