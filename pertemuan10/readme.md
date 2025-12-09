# Pertemuan 10
# Turunan Fungsi (Derivatives)


**Materi:** Kalkulus Diferensial

---
[Slide](https://anindito.github.io/kalkulus1/pertemuan10/)
## Daftar Isi

1. [Pendahuluan](#pendahuluan)
2. [Konsep Turunan Fungsi](#konsep-turunan-fungsi)
3. [Turunan Fungsi Konstan](#turunan-fungsi-konstan)
4. [Sifat-Sifat Turunan Fungsi](#sifat-sifat-turunan-fungsi)
5. [Aturan Rantai untuk Fungsi Komposisi](#aturan-rantai-untuk-fungsi-komposisi)
6. [Contoh Soal dan Pembahasan](#contoh-soal-dan-pembahasan)
7. [Latihan Soal](#latihan-soal)
8. [Rangkuman](#rangkuman)

---

## 1. Pendahuluan

Turunan fungsi adalah salah satu konsep fundamental dalam kalkulus yang memiliki aplikasi luas dalam berbagai bidang seperti fisika, ekonomi, teknik, dan ilmu komputer. Turunan menggambarkan laju perubahan suatu fungsi terhadap variabelnya.

### Aplikasi Turunan dalam Kehidupan:
- **Fisika**: Kecepatan adalah turunan dari posisi terhadap waktu
- **Ekonomi**: Marginal cost dan marginal revenue
- **Teknik**: Optimasi desain dan analisis sistem
- **Biologi**: Laju pertumbuhan populasi

---

## 2. Konsep Turunan Fungsi

### 2.1 Definisi Turunan

Jika sebuah fungsi dimisalkan sebagai **y = f(x)**, maka turunan dari fungsi tersebut dituliskan sebagai **y' = f'(x)** atau dapat juga ditulis sebagai **dy/dx**, yang artinya fungsi y diturunkan terhadap variabel x.

### 2.2 Definisi Formal Menggunakan Limit

Turunan fungsi f yang dinotasikan sebagai f' atau dengan notasi lainnya, merupakan sebuah fungsi yang nilainya pada sebarang nilai c adalah:

```
f'(c) = lim[h→0] [f(c + h) - f(c)] / h
```

Definisi ini menjelaskan bahwa turunan di titik c adalah limit dari rasio perubahan fungsi ketika perubahan variabel independen (h) mendekati nol.

### 2.3 Interpretasi Geometris

Secara geometris, turunan f'(c) merepresentasikan **kemiringan (slope) garis singgung** terhadap kurva y = f(x) pada titik (c, f(c)).

### 2.4 Interpretasi Fisik

Jika f(t) merepresentasikan posisi suatu objek pada waktu t, maka f'(t) merepresentasikan **kecepatan sesaat** objek tersebut pada waktu t.

### 2.5 Notasi Turunan

Ada beberapa notasi yang umum digunakan untuk menyatakan turunan:

1. **Notasi Lagrange**: f'(x), y'
2. **Notasi Leibniz**: dy/dx, df/dx
3. **Notasi Newton**: ẏ (dot notation)
4. **Notasi Euler**: Df, Dₓf

---

## 3. Turunan Fungsi Konstan

### 3.1 Aturan Fungsi Konstan

**Teorema**: Jika f(x) = k dengan k suatu konstanta, maka untuk sebarang x:

```
f'(x) = 0
```

### 3.2 Pembuktian

Menggunakan definisi turunan:

```
f'(x) = lim[h→0] [f(x + h) - f(x)] / h
      = lim[h→0] [k - k] / h
      = lim[h→0] 0 / h
      = 0
```

### 3.3 Contoh

**Contoh 1**: Dengan definisi, tentukan turunan dari f(x) = 10

**Penyelesaian**:
```
f'(x) = lim[h→0] [f(x + h) - f(x)] / h
      = lim[h→0] [10 - 10] / h
      = lim[h→0] 0 / h
      = 0
```

**Kesimpulan**: Turunan dari fungsi konstan f(x) = 10 adalah f'(x) = 0

### 3.4 Interpretasi

Fungsi konstan memiliki grafik berupa garis horizontal. Karena tidak ada perubahan nilai fungsi saat x berubah, maka laju perubahannya (turunan) adalah nol.

---

## 4. Sifat-Sifat Turunan Fungsi

### 4.1 Turunan Fungsi Konstan
```
Jika y = a, maka y' = 0
```

**Penjelasan**: Nilai fungsi tidak berubah terhadap perubahan x.

---

### 4.2 Turunan Fungsi Linear
```
Jika y = ax, maka y' = a
```

**Penjelasan**: Laju perubahan fungsi linear adalah konstan, yaitu koefisien dari x.

**Contoh**:
- Jika y = 5x, maka y' = 5
- Jika y = -3x, maka y' = -3

---

### 4.3 Aturan Pangkat (Power Rule)
```
Jika y = axⁿ, maka y' = an·xⁿ⁻¹
```

**Penjelasan**: Turunkan dengan menurunkan pangkat menjadi koefisien dan mengurangi pangkat sebesar 1.

**Contoh**:
- Jika y = x⁵, maka y' = 5x⁴
- Jika y = 3x⁴, maka y' = 12x³
- Jika y = x², maka y' = 2x
- Jika y = x⁻², maka y' = -2x⁻³

**Pembuktian Aturan Pangkat** (untuk n bilangan bulat positif):

Menggunakan ekspansi binomial:
```
f'(x) = lim[h→0] [(x+h)ⁿ - xⁿ] / h
```

Menggunakan ekspansi binomial Newton untuk (x+h)ⁿ:
```
(x+h)ⁿ = xⁿ + nxⁿ⁻¹h + [n(n-1)/2]xⁿ⁻²h² + ... + hⁿ
```

Maka:
```
f'(x) = lim[h→0] [nxⁿ⁻¹h + [n(n-1)/2]xⁿ⁻²h² + ... + hⁿ] / h
      = lim[h→0] [nxⁿ⁻¹ + [n(n-1)/2]xⁿ⁻²h + ... + hⁿ⁻¹]
      = nxⁿ⁻¹
```

---

### 4.4 Aturan Penjumlahan dan Pengurangan
```
Jika f(x) = u ± v, maka y' = u' ± v'
```

**Penjelasan**: Turunan dari jumlah atau selisih fungsi adalah jumlah atau selisih dari turunan masing-masing fungsi.

**Contoh**:
- Jika f(x) = x³ + 2x², maka f'(x) = 3x² + 4x
- Jika f(x) = 5x⁴ - 3x² + 7, maka f'(x) = 20x³ - 6x

---

### 4.5 Aturan Perkalian (Product Rule)
```
Jika y = u·v, maka y' = u'·v + u·v'
```

**Penjelasan**: Turunan dari perkalian dua fungsi adalah turunan fungsi pertama dikali fungsi kedua, ditambah fungsi pertama dikali turunan fungsi kedua.

**Pembuktian**:
```
f'(x) = lim[h→0] [u(x+h)v(x+h) - u(x)v(x)] / h
```

Tambahkan dan kurangkan u(x)v(x+h):
```
= lim[h→0] [u(x+h)v(x+h) - u(x)v(x+h) + u(x)v(x+h) - u(x)v(x)] / h
= lim[h→0] [v(x+h)·(u(x+h) - u(x))/h + u(x)·(v(x+h) - v(x))/h]
= v(x)·u'(x) + u(x)·v'(x)
```

**Contoh**:
- Jika y = (2x + 1)(x² - 3), maka:
  - u = 2x + 1, u' = 2
  - v = x² - 3, v' = 2x
  - y' = 2(x² - 3) + (2x + 1)(2x) = 2x² - 6 + 4x² + 2x = 6x² + 2x - 6

---

### 4.6 Aturan Pembagian (Quotient Rule)
```
Jika y = u/v, maka y' = (u'·v - u·v') / v²
```

**Penjelasan**: Turunan dari pembagian dua fungsi mengikuti rumus "turunan atas dikali bawah, kurang atas dikali turunan bawah, semua dibagi bawah kuadrat".

**Pembuktian**:

Misalkan f(x) = u(x)/v(x), maka:
```
f(x)·v(x) = u(x)
```

Turunkan kedua ruas (gunakan aturan perkalian):
```
f'(x)·v(x) + f(x)·v'(x) = u'(x)
f'(x)·v(x) = u'(x) - f(x)·v'(x)
f'(x) = [u'(x) - (u(x)/v(x))·v'(x)] / v(x)
f'(x) = [u'(x)·v(x) - u(x)·v'(x)] / v²(x)
```

**Contoh**:
- Jika y = (x² + 1)/(x - 2), maka:
  - u = x² + 1, u' = 2x
  - v = x - 2, v' = 1
  - y' = [2x(x - 2) - (x² + 1)(1)] / (x - 2)²
  - y' = [2x² - 4x - x² - 1] / (x - 2)²
  - y' = [x² - 4x - 1] / (x - 2)²

---

## 5. Aturan Rantai untuk Fungsi Komposisi

### 5.1 Definisi Fungsi Komposisi

Andaikan fungsi y = f(u) dan u = g(x) dengan f sebagai fungsi u dan g sebagai fungsi x.

Maka fungsi komposisi y = f(g(x)) dapat diturunkan di titik x dan berlaku:

```
dy/dx = (dy/du) · (du/dx)
```

### 5.2 Notasi Alternatif

Jika y adalah fungsi komposisi dari u yang merupakan fungsi dari x, maka:

```
y = f(u) dengan u = g(x)
y' = f'(u) · g'(x)
```

Atau dalam notasi yang lebih eksplisit:
```
d/dx[f(g(x))] = f'(g(x)) · g'(x)
```

### 5.3 Pembuktian Aturan Rantai

Misalkan y = f(u) dan u = g(x), maka:

```
dy/dx = lim[Δx→0] Δy/Δx
```

Kalikan dan bagi dengan Δu:
```
dy/dx = lim[Δx→0] (Δy/Δu) · (Δu/Δx)
```

Karena u kontinu di x (asumsi), maka ketika Δx → 0, juga Δu → 0:
```
dy/dx = lim[Δu→0] (Δy/Δu) · lim[Δx→0] (Δu/Δx)
      = (dy/du) · (du/dx)
```

### 5.4 Interpretasi

Aturan rantai memberitahu kita bahwa laju perubahan y terhadap x adalah hasil kali dari:
- Laju perubahan y terhadap u
- Laju perubahan u terhadap x

### 5.5 Contoh Aplikasi Aturan Rantai

**Contoh 1**: Tentukan turunan dari y = (x² + 3x)⁵

**Penyelesaian**:
- Misalkan u = x² + 3x, maka y = u⁵
- dy/du = 5u⁴
- du/dx = 2x + 3
- dy/dx = (dy/du) · (du/dx) = 5u⁴ · (2x + 3) = 5(x² + 3x)⁴ · (2x + 3)

**Contoh 2**: Tentukan turunan dari y = √(2x + 5)

**Penyelesaian**:
- Tulis ulang: y = (2x + 5)^(1/2)
- Misalkan u = 2x + 5, maka y = u^(1/2)
- dy/du = (1/2)u^(-1/2)
- du/dx = 2
- dy/dx = (1/2)u^(-1/2) · 2 = u^(-1/2) = 1/√(2x + 5)

**Contoh 3**: Tentukan turunan dari y = sin(x³)

**Penyelesaian**:
- Misalkan u = x³, maka y = sin(u)
- dy/du = cos(u)
- du/dx = 3x²
- dy/dx = cos(u) · 3x² = 3x² cos(x³)

---

## 6. Contoh Soal dan Pembahasan

### Contoh 1: Turunan Menggunakan Definisi

**Soal**: Jika f(x) = 10x - 5, cari f'(4) menggunakan definisi.

**Penyelesaian**:

Menggunakan definisi turunan:
```
f'(4) = lim[h→0] [f(4 + h) - f(4)] / h
```

Hitung f(4 + h):
```
f(4 + h) = 10(4 + h) - 5 = 40 + 10h - 5 = 35 + 10h
```

Hitung f(4):
```
f(4) = 10(4) - 5 = 40 - 5 = 35
```

Substitusi:
```
f'(4) = lim[h→0] [(35 + 10h) - 35] / h
      = lim[h→0] 10h / h
      = lim[h→0] 10
      = 10
```

**Jawaban**: f'(4) = 10

---

### Contoh 2: Turunan Fungsi Kubik

**Soal**: Jika f(x) = x³ + 5x, cari f'(c)

**Penyelesaian**:

Gunakan aturan pangkat dan penjumlahan:
```
f(x) = x³ + 5x
f'(x) = 3x² + 5
```

Untuk nilai c tertentu:
```
f'(c) = 3c² + 5
```

**Jawaban**: f'(c) = 3c² + 5

---

### Contoh 3: Turunan Fungsi Polinomial

**Soal**: Tentukan turunan dari fungsi y = (x² - 3x⁶ + 21)³

**Penyelesaian**:

Gunakan aturan rantai:
- Misalkan u = x² - 3x⁶ + 21
- Maka y = u³

Hitung du/dx:
```
du/dx = 2x - 18x⁵
```

Hitung dy/du:
```
dy/du = 3u²
```

Gunakan aturan rantai:
```
dy/dx = (dy/du) · (du/dx)
      = 3u² · (2x - 18x⁵)
      = 3(x² - 3x⁶ + 21)² · (2x - 18x⁵)
```

**Jawaban**: dy/dx = 3(x² - 3x⁶ + 21)² · (2x - 18x⁵)

---

### Contoh 4: Turunan Fungsi Komposisi

**Soal**: Tentukan turunan dari fungsi y = (3x + 5)(x² - 3)³

**Penyelesaian**:

Fungsi ini memerlukan kombinasi aturan perkalian dan aturan rantai.

Misalkan:
- u = 3x + 5, dengan u' = 3
- v = (x² - 3)³

Untuk mencari v', gunakan aturan rantai:
- Misalkan w = x² - 3, maka v = w³
- dw/dx = 2x
- dv/dw = 3w²
- v' = 3w² · 2x = 3(x² - 3)² · 2x = 6x(x² - 3)²

Gunakan aturan perkalian:
```
y' = u'·v + u·v'
   = 3·(x² - 3)³ + (3x + 5)·6x(x² - 3)²
   = 3(x² - 3)³ + 6x(3x + 5)(x² - 3)²
```

Faktorkan (x² - 3)²:
```
y' = (x² - 3)²[3(x² - 3) + 6x(3x + 5)]
   = (x² - 3)²[3x² - 9 + 18x² + 30x]
   = (x² - 3)²[21x² + 30x - 9]
   = 3(x² - 3)²[7x² + 10x - 3]
```

**Jawaban**: y' = 3(x² - 3)²(7x² + 10x - 3)

---

## 7. Latihan Soal

### Soal 1
Dengan menggunakan definisi, tentukan turunan dari f(x) = 1/x

**Petunjuk**: Gunakan f'(c) = lim[h→0] [f(c+h) - f(c)]/h

---

### Soal 2
Tentukan turunan dari fungsi y = (x² - 3x⁶ + 21)³

**Petunjuk**: Gunakan aturan rantai dengan u = x² - 3x⁶ + 21

---

### Soal 3
Tentukan turunan dari fungsi: y = (3x + 5)(x² - 3)³

**Petunjuk**: Gunakan aturan perkalian dikombinasikan dengan aturan rantai

---

### Soal 4
Tentukan turunan dari fungsi: y = 3x√(x⁴ - 6x² + 9)

**Petunjuk**: 
- Tulis ulang akar sebagai pangkat 1/2
- Gunakan aturan perkalian dan aturan rantai

---

### Soal 5
Tentukan turunan dari fungsi: y = (x - 3)/(3x + 1)

**Petunjuk**: Gunakan aturan pembagian

---

### Soal 6
Tentukan turunan dari fungsi: y = √(x - 7) + x/(x² - 1) - 9

**Petunjuk**: 
- Pisahkan menjadi tiga bagian
- Gunakan aturan penjumlahan, aturan rantai untuk akar, dan aturan pembagian

---

## 8. Rangkuman

### Konsep Utama

1. **Definisi Turunan**: 
   - f'(c) = lim[h→0] [f(c + h) - f(c)] / h
   - Mengukur laju perubahan instantan fungsi

2. **Turunan Fungsi Konstan**: 
   - Jika f(x) = k, maka f'(x) = 0

3. **Aturan Dasar Turunan**:
   - Konstanta: y = a → y' = 0
   - Linear: y = ax → y' = a
   - Pangkat: y = axⁿ → y' = anxⁿ⁻¹
   - Penjumlahan: (u ± v)' = u' ± v'
   - Perkalian: (u·v)' = u'v + uv'
   - Pembagian: (u/v)' = (u'v - uv')/v²

4. **Aturan Rantai**: 
   - Untuk y = f(u) dan u = g(x)
   - dy/dx = (dy/du) · (du/dx)

### Tips Menyelesaikan Soal Turunan

1. **Identifikasi jenis fungsi** (pangkat, perkalian, pembagian, komposisi)
2. **Pilih aturan yang tepat** berdasarkan struktur fungsi
3. **Sederhanakan ekspresi** sebelum menurunkan jika memungkinkan
4. **Gunakan aturan rantai** untuk fungsi komposisi
5. **Periksa hasil** dengan menyederhanakan jawaban akhir

### Kesalahan Umum yang Harus Dihindari

1. ❌ Menurunkan konstanta menjadi selain nol
2. ❌ Lupa menggunakan aturan rantai pada fungsi komposisi
3. ❌ Salah mengaplikasikan aturan perkalian: (uv)' ≠ u'v'
4. ❌ Salah mengaplikasikan aturan pembagian
5. ❌ Tidak menyederhanakan hasil akhir

### Aplikasi Turunan

- **Menentukan kecepatan dan percepatan** dalam fisika
- **Optimasi** dalam ekonomi dan teknik
- **Analisis perubahan** dalam berbagai fenomena
- **Menentukan titik maksimum dan minimum** fungsi
- **Menggambar grafik** fungsi dengan lebih akurat

---

## Referensi

1. Stewart, J. (2015). *Calculus: Early Transcendentals*. Cengage Learning.
2. Anton, H., Bivens, I., & Davis, S. (2012). *Calculus*. John Wiley & Sons.
3. Thomas, G. B., Weir, M. D., & Hass, J. (2014). *Thomas' Calculus*. Pearson.
4. Purcell, E. J., Varberg, D., & Rigdon, S. E. (2007). *Calculus*. Pearson Prentice Hall.

---

## Tentang Penyusun


Dosen Matematika dan Kalkulus  
Universitas [Nama Universitas]

---

*Materi ini disusun untuk keperluan pembelajaran kalkulus diferensial. Untuk pertanyaan atau diskusi lebih lanjut, silakan hubungi pengajar.*
