# -Belajar-Nested-Loop-C---Membuat-Pohon-ASCII

🌲 Belajar Nested Loop C++ - Membuat Pohon ASCII

Pendahuluan

Program ini menggunakan nested loop (perulangan bersarang) untuk membuat gambar pohon menggunakan karakter "*".

Kode:

#include <iostream>
using namespace std;

int main() {
    for(int i = 1; i <= 13; i++) {

        for(int s = 1; s <= 13 - i; s++)
            cout << " ";

        for(int j = 1; j <= i; j++)
            cout << "**";

        cout << endl;
    }

    cout << "\t    | |" << endl;
    cout << "\t    | |" << endl;
    cout << "\t    | |" << endl;
    cout << "\t    | |" << endl;
    cout << "\t    | |" << endl;

    return 0;
}

---

Cara Kerja Program

Program terdiri dari tiga bagian utama.

1. Loop Luar ("i")

for(int i = 1; i <= 13; i++)

Loop ini menentukan jumlah baris daun pohon.

Karena batas akhirnya "13", maka pohon memiliki 13 tingkat.

---

2. Loop Spasi ("s")

for(int s = 1; s <= 13 - i; s++)
    cout << " ";

Loop ini mencetak spasi di depan karakter "*".

Tujuannya agar daun berada di tengah.

Contoh:

Ketika

i = 1

Maka

13 - 1 = 12

Program mencetak 12 spasi.

Ketika

i = 10

Maka

13 - 10 = 3

Program hanya mencetak 3 spasi.

Semakin besar nilai "i", semakin sedikit spasi yang dicetak.

---

3. Loop Daun ("j")

for(int j = 1; j <= i; j++)
    cout << "**";

Loop ini mencetak daun pohon.

Mengapa menggunakan ""**""?

Supaya bentuk pohon terlihat lebih lebar dan proporsional.

Contoh:

Jika

i = 1

Output:

**

Jika

i = 2

Output:

****

Jika

i = 5

Output:

**********

Semakin besar nilai "i", semakin lebar daun pohon.

---

Batang Pohon

Setelah semua daun selesai dicetak, program membuat batang pohon.

cout << "\t    | |" << endl;

Baris tersebut diulang beberapa kali sehingga batang tampak memanjang.

Outputnya seperti:

      | |
      | |
      | |
      | |
      | |

---

Bentuk Akhir

Program menghasilkan bentuk seperti berikut.

            **
           ****
          ******
         ********
        **********
       ************
      **************
     ****************
    ******************
   ********************
  **********************
 ************************
**************************
        | |
        | |
        | |
        | |
        | |

---

Kesimpulan

- "i" menentukan tinggi pohon.
- "s" menentukan jumlah spasi agar pohon berada di tengah.
- "j" menentukan jumlah daun ("**") yang dicetak.
- Semakin besar nilai "i", semakin sedikit spasi dan semakin banyak daun.
- Batang pohon dibuat setelah seluruh daun selesai dicetak menggunakan beberapa "cout".

«💡 Latihan ini sangat baik untuk memahami nested loop karena setiap loop memiliki tugas yang berbeda: ada yang mengatur tinggi, posisi, dan lebar gambar.»
