# Recap Week 1

* [Terminal & Git](#terminal-and-git)
* [Algorithm and Pseudocode](#algorithm-and-pseudocode)
* [Conditional and Primitive Data Types](#conditional-and-primitive-data-types-es6)
* [Advanced Conditional](#advanced-conditional)
* [Iterasi](#iterasi)
* [Nested Loop](#nested-loop)
* [References for Self-Taught](#references-for-self-taught)

![](https://media.giphy.com/media/3oKIPnAiaMCws8nOsE/giphy.gif)

## Terminal and Git

## Terminal

Sebuah interface berupa command-line yang bisa digunakan untuk mengoperasikan komputer
beberapa command terminal antara lain :

 * `cd` : untuk berpindah directory (`cd <path directory>`)
 * `pwd` : untuk menampilkan status directory yang sedang aktif
 * `ls` : untuk menampilkan list dari folder atau file yang tersedia pada directory yang aktif
 * `touch` : untuk membuat file baru (`touch <nama_file dan extensionnya>`)
 * `cp` : untuk mencopy file (`cp <file_origin> <file_copy_name>`)
 * `cp -rf` : untuk mencopy folder
 * `mv` : untuk memindahkan file atau folder (`mv <file_origin> <path>`)
 * `rm` : untuk menghapus file (`rm <file_name>`)
 * `mkdir` : untuk membuat folder baru (`mkdir <folder_name>`) 
 * `rm -rf` : untuk menghapus folder (`rm -rf <folder_name>`)
 * kalian bisa membuat file dan folder sekaligus dengan syntax (`touch <nama_file1 dan extensionnya> <nama_file2 dan extensionnya> <nama_file3 dan extensionnya>`)
 

## Git

Version Control System (VCS), sebuah system yang bisa mencatat setiap update dalam sebuah source code
Beberapa command git yang biasa digunakan : 
 * Git !== Github
 
 * `git config` : digunakan untuk configurasi ke github (`git config --global user.name “<name>”`) dan (`git config --global user.email “<email>”`)
 setelah itu bisa dicek ke `git config --list`

 * `git clone` : digunakan untuk menclone repository git (`git clone <url_repository>`)
 * `git pull` : digunakan untuk mendownload data dari repository (`git pull origin <nama_branch>`)

 lalu ini adalah urutan command git yang biasa digunakan dalam pengerjaan challenge hacktiv pada github :
 * `git checkout` : digunakan untuk membuat branch baru (`git checkout -b <nama_branch>`)
 * `git add` : digunakan untuk menambahkan file yang akan diupload pada git bisa secara spesifik ataupun seluruh file (`git add .` default yg digunakan untuk menambahkan semua filenya)
 * `git commit -m` : digunakan untuk memberikan pesan pada file yang akan diupload (`git commit -m <pesan_yang diberikan>`) 
 * `git status` : digunakan untuk memeriksa status dari folder git pada pc kalian 
 * `git push` : digunakan untuk mengupload data dari pc ke repository hosting git (`git push origin <nama_branch>`)



## Algorithm and Pseudocode

- Algoritma adalah langkah-langkah atau setiap step yang dibuat untuk menyelesaikan suatu permasalahan.
- Pseudocode adalah penjabaran deskriptif dari sebuah algoritma yang terstruktur sesuai dengan konvensi/kesepakatan antara developer.

contoh algoritma dan pseudocode pada perhitungan keliling persegi: 
Algoritma :
- ketahui rumus dari keliling persegi terlebih dulu
- untuk menghitung keliling butuh panjang dari persegi sehingga langkah selanjutnya
- siapkan panjang dari persegi yang berisi angka
- se`telah panjang diketahui lakukan perhitungan keliling persegi
- tampilkan hasil perhitungannya

Pseudocode :
- Store panjangPersegi with Number
- Store kelilingPersegi with 0 
- Calculate panjangPersegi times 4
- Set kelilingPersegi with result Calculate
- Display kelilingPersegi

## Minisheet Pseudocode 

- STORE > digunakan membuat variable baru
- SET > digunakan untuk mereassign atau merubah isi dari variable yang ada
- CALCULATE > digunakan untuk melakukan matematika operator
- DISPLAY > digunakan untuk menampilkan variable
- IF, ELSE IF, dan ELSE > digunakan untuk case kondisi 
- SWITCH CASE > bentuk lain IF 
- FOR, WHILE, DO WHILE dan BREAK > digunakan pada pengulangan atau iterasi
- LENGTH > digunakan untuk menghitung panjang dari variable, hanya bisa digunakan jika type data "STRING" dan "ARRAY"
- PUSH > memasukan data kedalam data lain yang bertype "ARRAY"

> References
>
> <https://github.com/ideaspaper/p0-class-notes/blob/master/notes/pseudocode-note-1.md>
>
> <https://github.com/ideaspaper/p0-class-notes/blob/master/notes/pseudocode-note-2.md>
>
> <https://github.com/ideaspaper/p0-class-notes/blob/master/notes/pseudocode-note-3.md>


## Conditional and Primitive Data Types (ES6)

    Data Types

    - Number (integer) :
        * bisa dilakukan math operator
        * tidak memiliki panjang / length

    - String
        * tidak bisa dilakukan math operator
        * memiliki panjang / length

    - Boolean
        * hanya terdiri dari false or true  

  > Build in function Datatype
  > 
  > ## Typeof
  > Untuk mengecek type data bisa menggunakan build in function **typeof** dengan penggunaan typeof ```<space><variable>``` 
  >
  > ## Convert Data from string to Number
  > Untuk mengubah datatype dari string menjadi number ada beberapa cara, diantaranya :
  >   - Number(`<variable>`)
  >   - +`<variable>`
  >   - parseInt(`<variable>`)
  >   - parseFloat(`<variable>`)
  >
  > ## Convert Data from any type data primitif to string
  > Untuk mengubah datatype dari berbagai macam data type menjadi string kalian bisa menggunakan **.toString()** dengan cara `<variable>.toString()`
  >
  > ## membulatkan bilangan desimal 
  > ada beberapa cara yang bisa digunakan ketika kita akan membulatkan bilangan desimal pada javascript:
  > - Math.round(`<variable>`) > membulatkan sesuai dengan kaidah math jika diatas 0.5 akan naik jika dibwh 0.5 akan dibulatkan kebawah.
  > - Math.floor(`variable`) > membulatkan kebawah
  > - Math.ceil(`variable`) > membulatkan keatas
  > - `<variable>`.toFixed(<`num`>) > membulatkan variable sesuai dengan num (berapa angka dblkg koma)
  >
  > ## build in function lainnya yang sering digunakan
  > - **isNan()** biasa digunakan untuk mengecek apakah data adalah number atau bukan dengan cara isNan(`<variable>`)
  >

```js
Variables > menampung sebuah data

Declaration > membuat sebuah variable tanpa meng-assign sebuah value
let x;

Assigment > meng-assign sebuah variable dengan sebuah value (menggunakan `=`)
x = 10

Declaration + assigment
let z = 666  

Reassignment > mengganti value dari variable yang sudah ada nilai valuenya.
let number = 10
number = 0
```

MATH OPERATOR 

    - PLUS (+) > menambahkan 
    - MINUS (-) > mengurangi
    - DEVIDE BY (/) > pembagian
    - TIMES (*) > perkalian
    - MODULUS BY (%) > sisa bagi  


COMPARASION OPERATOR 

    (>)
    - lebih dari
    - GREATER THAN
    - diatas

    (>=)
    - lebih dari sama dengan
    - GREATER THAN EQUAL
    - keatas
    - minimal

    (<)
    - lebih kecil
    - LOWER THAN
    - dibawah

    (<=)
    - lebih kecil sama dengan
    - LOWER THAN EQUAL
    - kebawah
    - maksimal

    (===)
    - perbandingan absolut ( yang dibandingkan value dan type datanya )
    example : 10 === 10 atau "sepuluh" === "sepuluh"

    (==)
    - perbandingan abstrak ( yang dibandingkan hanya value nya saja )
    example : "10" == 10 > disini 10 string dengan 10 number dianggap sama

    (!==)
    - tidak sama absolut

    (!=)
    - tidak sama abstrak
 




 CONDITIONAL 

- Terdapat kondisi didalam if/else if, sedangkan else tidak ada kondisi.

- Truthy & Falsy values adalah values yang bisa menjadi true/false sesuai kondisi

- Truthy adalah value yang tidak false
- Falsy adalah value yang tidak true

contoh bentuk if-else, if-elseif-else

```js
if (condition) {
  statement1
} else {
  statement2
}

if (condition1) {
  statement1
} else if (condition2) {
  statement2
} else {
  statement3
}
```

## Advanced Conditional

- Switch Case

contoh bentuk switch case

```js
switch (expression) {
  case value1:
    //Statements executed when the
    //result of expression matches value1
    [break;]
  case value2:
    //Statements executed when the
    //result of expression matches value2
    [break;]
  ...
  case valueN:
    //Statements executed when the
    //result of expression matches valueN
    [break;]
  [default:
    //Statements executed when none of
    //the values match the value of the expression
    [break;]]
}
```
- `default` dalam switch case adalah opsional, seperti halnya `else` dalam if-else, `default` akan berjalan jika **tidak** ada case yang sesuai dengan ekspresi yang diberikan

- `break` dalam switch case adalah opsional, namun perlu diingat jika dalam sebuah switch case tidak dikasih break, maka statement-statement dari case lain dibawahnya akan tereksekusi juga.

- Nested Conditional -> ada if-else didalam sebuah if-else

contoh bentuk nested conditional

```js
if (condition) {
  if (condition1) {
    statement1
  } else {
    statement3
  }
} else {
  statement2
}
```

## Iterasi

- DRY -> Don't Repeat Yourself.
- Iterasi dipakai agar kita tidak mengulang proses yang sama
- Iterasi akan membuat code menjadi dinamis

- Struktur iterasi

  - inisialisasi
  - batas/kondisi
  - eksekusi (increment/decrement)
  - aksi/statement

- Macam-macam iterasi: For, While, Do-While

contoh bentuk iterasi:

```js
for (initialization; condition; eksekusi) {
  statement
}

while (condition) {
  statement
}

do {
  statement
}
while (condition)
```

> Referensi
>
> Pseudocode: <https://github.com/ideaspaper/p0-class-notes/blob/master/notes/pseudocode-note-2.md>

## Nested Loop

- Ada loop di dalam loop

contoh bentuk nested for-for

```js
for (initialization1; condition1; eksekusi1) {
  for (initialization2; condition2; eksekusi2) {
    statement
  }
}
```

contoh bentuk nested loop while-for

```js
while (condition) {
  for (initialization; condition; eksekusi) {
    statement
  }
}
```

- `break` berfungsi untuk menghentikan proses perulangan yang sedang berjalan

- `continue` berfungsi untuk melewati/skip 1 proses perulangan saja

## References for Self-Taught


Lecture Materials

- [Algoritma & Pseudocode](https://docs.google.com/document/d/10VEx7QfFPNtS_089m8Pd-BFteiB55-Uj/edit?usp=sharing&ouid=101901749413551476666&rtpof=true&sd=true)
- [Algorithm & Pseudocode: Iteration](https://docs.google.com/document/d/1-DwunE1r_3mDnRuZ8sOtIykZnQ_sSw1Z/edit?usp=sharing&ouid=101901749413551476666&rtpof=true&sd=true)
- [Conditional & Primitive Data Types](https://docs.google.com/document/d/1vUi2rczwUN1SDsnhZfAKygjobMP2yWjIBKPr2e8Ylsw/edit?usp=sharing)
- [Conditional Switch-Case](https://docs.google.com/document/d/1F4_sZzvRZdmEyp_g-m1Z2Qfx7uHBR-ui/edit?usp=sharing&ouid=101901749413551476666&rtpof=true&sd=true)
- [String in JS](https://docs.google.com/document/d/1pM1CP-ZbkXqdQlQwB90G-IJNbeOc4Uh9/edit?usp=sharing&ouid=101901749413551476666&rtpof=true&sd=true)
- [ES6](https://docs.google.com/document/d/1qwzD4nF843dfLiF0GFiGQ0_3I6dBL2V_/edit?usp=sharing&ouid=101901749413551476666&rtpof=true&sd=true)
- [Built-in Function: Math](https://docs.google.com/document/d/1TzWrC4zWh4zmt6wUz98_96woUKEikU1Z/edit?usp=sharing&ouid=101901749413551476666&rtpof=true&sd=true)

Reading Materials

- [What is an algorithm and why should you care?](https://www.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/v/what-are-algorithms)
- [A guessing game](https://www.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/a/a-guessing-game)
- [Route Finding](https://www.khanacademy.org/computing/computer-science/algorithms/intro-to-algorithms/a/route-finding)

Documentations

- [JS variables, data types, literals, etc.](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_Types)
- [assignment operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#assignment_operators)
- [comparison operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#comparison_operators)
- [artihmethic operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#arithmetic_operators)
- [logical operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#logical_operators)
- [string operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#string_operators)
- [if...else](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#if...else_statement)
- [switch...case](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Control_flow_and_error_handling#switch_statement)
- [for loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#for_statement)
- [do...while](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#do...while_statement)
- [while](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#while_statement)
- [break statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#break_statement)
- [continue statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration#continue_statement)

Exercises

- [Hello, World!](https://www.learn-js.org/en/Hello%2C_World%21)
- [Variables and Types](https://www.learn-js.org/en/Variables_and_Types)
- [Operartors](https://www.learn-js.org/en/Operators)
- [Conditions](https://www.learn-js.org/en/Conditions)
- [Loops](https://www.learn-js.org/en/Loops)

External Links

- [Programmer Zaman Now](https://www.youtube.com/watch?v=SDROba_M42g)
- [Web Programming Unpas](https://www.youtube.com/watch?v=RUTV_5m4VeI&list=PLFIM0718LjIWXagluzROrA-iBY9eeUt4w&ab_channel=WebProgrammingUNPAS)
- [FreeCodeCamp.org](https://www.freecodecamp.org/)
- [FreeCodeCamp Youtube Channel](https://www.youtube.com/watch?v=PkZNo7MFNFg)
