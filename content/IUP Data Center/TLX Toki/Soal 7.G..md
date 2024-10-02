---
title: Soal 7.G.
draft: false
tags:
  - TLX_Toki
---
```

#include <iostream>
using namespace std;

int total_kandang = 10;

// bebek[i] menyatakan banyaknya bebek pada kandang nomor i.
int bebek[11];

// Fungsi untuk mengosongkan kandang
void kosongkan_kandang() {
    for (int i = 1; i <= total_kandang; i++) {
        bebek[i] = 0;
    }
}

// Fungsi untuk mengisi bebek ke dalam kandang
void isi_bebek_ke_dalam_kandang(int start_kandang, int end_kandang, int jumlah_bebek) {
    for (int i = start_kandang; i <= end_kandang; i++) {
        bebek[i] += jumlah_bebek;  // Tambahkan jumlah bebek ke setiap kandang dalam rentang
    }
}

// Fungsi untuk mencari kandang dengan bebek terbanyak
int bebek_terbanyak_dalam_suatu_kandang() {
    int bebek_terbanyak = bebek[1];
    for (int i = 2; i <= total_kandang; i++) {
        bebek_terbanyak = max(bebek_terbanyak, bebek[i]);  // Cari jumlah terbesar
    }
    return bebek_terbanyak;
}

int main() {
    kosongkan_kandang();

    // Pengisian bebek ke kandang sesuai dengan perintah
    isi_bebek_ke_dalam_kandang(1, 8, 2);
    isi_bebek_ke_dalam_kandang(2, 9, 10);
    isi_bebek_ke_dalam_kandang(5, 6, 2);
    isi_bebek_ke_dalam_kandang(9, 10, 3);
    isi_bebek_ke_dalam_kandang(1, 4, 7);
    isi_bebek_ke_dalam_kandang(1, 4, 2);
    isi_bebek_ke_dalam_kandang(4, 8, 6);

    // Menampilkan jumlah bebek terbanyak dalam suatu kandang
    cout << bebek_terbanyak_dalam_suatu_kandang() << endl;
}


```