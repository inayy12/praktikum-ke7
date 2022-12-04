### PRAKTIKUMKE7
### Inayatus Sholekhawati
### 312210200
### TI.22.A2

## LATIAHAN
## Membuat fungsi menggunakan lamda

```
import math
def a(x):
  return x**2
a = lambda x : x**2
print(a(2))
def b(x, y):
  return math.sqrt(x*2 + y*2)
b = lambda x, y : x * 2 + y * 2
print(b(2, 2))
def c(*args):
  return sum(args)/len(args)
c = lambda *args : sum(args)/len(args)
print(c(1,2,3,4,5))
def d(s):
  return "".join(set(s))
d = lambda s: "".join(set(s))
print(d("buku"))
```

### SOURCE COODE
![foto](https://user-images.githubusercontent.com/115867315/205497189-169777a0-1da3-40de-9488-bc9108779f18.png)


### OUTPUT
![foto2](https://user-images.githubusercontent.com/115867315/205497106-1df28f43-59d9-4eae-8666-479ca0e61251.png)


### PRAKTIKUM DICTIONARY

### PENJELASAN PRAKTIKUM

1. MENAMBAHKAN DICTIONARY LALU INPUT DENGAN DATA ```data={}```
2. MEMBUAT PELUANG FUNGSI DENGAN DEF UNTUK MENAMPILKAN FUNGSI
3. LALU MENAMBAHKAN DATA NIM, NAMA, NILAI TUGAS UTS, DAN UAS.
   Data yang diimput akan masuk ke dictionary, data dengan Nama sebagai keys. 
   Sedangkan nim, tugas, san uts, uas akan menjadi data valiu.

```
x = mahasiswa = {}

def tambah():
    print("Tambah Data")
    nama = input("Masukkan Nama Mahasiswa   : ")
    nim = input("Masukkan NIM              : ")
    tugas = int(input("Masukkan Nilai Tugas      : "))
    uts = int(input("Masukkan Nilai UTS        : "))
    uas = int(input("Masukkan Nilai UAS        : "))
    akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
    mahasiswa[nama] = nim , tugas, uts , uas , akhir
```


4.MELIHAT DATA. sebelum melihat data kita harus mengimpu data terlebih dahulu agar data yang udah di imput bisa ditampilkan, jika belum mengimput data otomatis data yang ditampilkan akan bertuliskan tidak ada.

```
def tampilkan():
    if mahasiswa.items():
        print("---------------------------------------------------------------------------------")
        print("\n                               DAFTAR NILAI MAHASISWA                    ")
        print("---------------------------------------------------------------------------------")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("---------------------------------------------------------------------------------")
        i = 0
        for b in mahasiswa.items():
             i += 1
             print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} | {5:7f}   |"
                . format ( b [ 0 ][: 14 ], b [ 1 ][ 0 ], b [ 1 ][ 1 ], b [ 1 ][ 2 ], b [ 1 ][ 3 ], b [ 1 ][ 4 ] , no = i ))
        print("---------------------------------------------------------------------------------")
    else :
        print("---------------------------------------------------------------------------------")
        print("\n                               DAFTAR NILAI MAHASISWA                    ")
        print("---------------------------------------------------------------------------------")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("---------------------------------------------------------------------------------")
        print("|                                TIDAK ADA DATA                                 |")
        print("---------------------------------------------------------------------------------")
```

5. HAPUS DATA. jika ingin menghapus data maka kita akan diminta untuk mengimput nama terlebihdahulu, lalu data yang telah diimput akan dihapus bersama nim, nilai tugas, nilai uts, nilai uas.

```
def hapus():
   print ( "Hapus Data" )
   nama = input("Masukkan Nama Mahasiswa   : ")
   if  nama in  mahasiswa . keys ():
       del  mahasiswa [ nama ]
   else :
       print ( "Nama {0} Tidak Ditemukan" . format ( nama ))

```

6. UBAH DATA. Apabila ingin mengubah data, kita diminta untuk mengimput nama terlebihdahulu, barulah data bisa diubah.

```
def ubah():
   print ( "Ubah Data" )
   nama = input("Masukkan Nama Mahasiswa   : ")
   if nama in  mahasiswa . keys ():
       nim = input("Masukkan NIM              : ")
       tugas = int(input("Masukkan Nilai Tugas      : "))
       uts = int(input("Masukkan Nilai UTS        : "))
       uas = int(input("Masukkan Nilai UAS        : "))
       akhir = tugas * 30/100 + uts * 35/100 + uas * 35/100
       mahasiswa[nama] = nim , tugas, uts , uas , akhir
   else :
       print ( "Nama{0} Tidak Ditemukan" . format(nama ))

```

7. Setelah selesai membuat program data di atas maka kita perlu mengulang statement menggunakan while yang terdapat pilihan menu untuk menjalankan program.

```
while True:
    print("")
    print("===========================")
    print("|   Program Input Nilai   |")
    print("===========================")
    c = input("L)ihat, T)ambah, U)bah, H)apus, K)eluar: ")
    if c.lower() == "l":
        tampilkan()
    elif c.lower() == "t":
        tambah()
    elif c.lower() == "u":
        ubah()
    elif c.lower() == "h":
        hapus()
    elif c.lower() == "k":
        print()
        print("---------------------------------------------------------------------------------")
        print("                                 PROGRAM TELAH SELESAI                    ")
        print("---------------------------------------------------------------------------------")
        print(35*'=')
        print("Nama\t: USWATUN HASANAH\nKelas\t: TI.22.A3\nNIM\t\t: 312210343")
        print(35*'=')
        break

    else:
        print()
        print("Kode yang anda masukkan salah!")
```

### OUOTPUT
![foto3](https://user-images.githubusercontent.com/115867315/205497247-a4a4178b-601a-471e-a18a-a37c17b1f243.png)
![foto4](https://user-images.githubusercontent.com/115867315/205497258-249058e9-c953-4457-9c8a-156fe9fec81c.png)
![foto5](https://user-images.githubusercontent.com/115867315/205497273-e17298d2-7014-4536-ba5c-3c2efb76dace.png)

### FLAWCHART
![Screenshot (164)](https://user-images.githubusercontent.com/115867315/205497297-4e6702b2-7b8f-4e14-a988-f7038800c663.png)
