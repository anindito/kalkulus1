# Pertemuan 13: Turunan Eksponen, Turunan Tingkat Tinggi, dan Turunan Implisit

**Mata Kuliah:** Kalkulus  
**Penyusun:** Anindito, S.Kom., S.S., S.H., M.TI., CHFI.  
**Topik:** Turunan Lanjutan

---

## Daftar Isi

1. [Pendahuluan](#1-pendahuluan)
2. [Turunan Fungsi Eksponen](#2-turunan-fungsi-eksponen)
   - 2.1 [Turunan Eksponen Berbasis e](#21-turunan-eksponen-berbasis-e)
   - 2.2 [Turunan Eksponen Umum (Basis a)](#22-turunan-eksponen-umum-basis-a)
3. [Turunan Tingkat Tinggi (Orde Tinggi)](#3-turunan-tingkat-tinggi-orde-tinggi)
   - 3.1 [Konsep Dasar](#31-konsep-dasar)
   - 3.2 [Notasi Turunan Tingkat Tinggi](#32-notasi-turunan-tingkat-tinggi)
   - 3.3 [Contoh Perhitungan](#33-contoh-perhitungan)
4. [Turunan Fungsi Implisit](#4-turunan-fungsi-implisit)
   - 4.1 [Fungsi Eksplisit vs Implisit](#41-fungsi-eksplisit-vs-implisit)
   - 4.2 [Metode Diferensiasi Implisit](#42-metode-diferensiasi-implisit)
   - 4.3 [Langkah-langkah Penyelesaian](#43-langkah-langkah-penyelesaian)
   - 4.4 [Contoh Penerapan](#44-contoh-penerapan)
5. [Latihan Soal](#5-latihan-soal)
6. [Rangkuman](#6-rangkuman)

---

## 1. Pendahuluan

Pada pertemuan ini, kita akan mempelajari tiga topik penting dalam diferensiasi:

1. **Turunan Eksponen** - Bagaimana menurunkan fungsi yang memiliki bentuk eksponensial
2. **Turunan Tingkat Tinggi** - Menurunkan fungsi secara berulang untuk mendapatkan turunan kedua, ketiga, dan seterusnya
3. **Turunan Implisit** - Teknik untuk menurunkan fungsi yang tidak dapat dinyatakan secara eksplisit

Pemahaman ketiga konsep ini sangat penting untuk aplikasi kalkulus dalam fisika, teknik, dan bidang ilmu lainnya.

---

## 2. Turunan Fungsi Eksponen

Fungsi eksponen adalah fungsi yang memiliki variabel pada pangkatnya. Ada dua jenis utama yang akan kita bahas:

### 2.1 Turunan Eksponen Berbasis e

Bilangan Euler **e ≈ 2.71828...** memiliki sifat istimewa: turunan dari e^x adalah dirinya sendiri.

#### Rumus Dasar

Jika $y = e^u$ dimana $u$ adalah fungsi dari $x$, maka:

$$\boxed{y' = e^u \cdot u'}$$

Atau dalam notasi Leibniz:

$$\frac{dy}{dx} = e^u \cdot \frac{du}{dx}$$

#### Penjelasan Konsep

- Ketika $u = x$ (fungsi identitas), maka $u' = 1$, sehingga $\frac{d}{dx}(e^x) = e^x$
- Ini adalah satu-satunya fungsi yang turunannya sama dengan dirinya sendiri
- Untuk fungsi komposit, kita menerapkan **aturan rantai (chain rule)**

#### Contoh 2.1.1

**Tentukan turunan dari** $y = e^{\sin x}$

**Penyelesaian:**

Identifikasi:
- $u = \sin x$
- $u' = \cos x$

Menggunakan rumus:
$$y' = e^u \cdot u' = e^{\sin x} \cdot \cos x$$

$$\boxed{y' = e^{\sin x} \cos x}$$

#### Contoh 2.1.2

**Tentukan turunan dari** $y = e^{3x^2 + 2x}$

**Penyelesaian:**

Identifikasi:
- $u = 3x^2 + 2x$
- $u' = 6x + 2$

Menggunakan rumus:
$$y' = e^{3x^2 + 2x} \cdot (6x + 2)$$

$$\boxed{y' = (6x + 2)e^{3x^2 + 2x}}$$

#### Contoh 2.1.3

**Tentukan turunan dari** $y = x^2 \cdot e^{x}$

**Penyelesaian:**

Menggunakan aturan perkalian (product rule):
$$y' = (x^2)' \cdot e^x + x^2 \cdot (e^x)'$$
$$y' = 2x \cdot e^x + x^2 \cdot e^x$$
$$\boxed{y' = e^x(2x + x^2) = xe^x(2 + x)}$$

---

### 2.2 Turunan Eksponen Umum (Basis a)

Untuk fungsi eksponen dengan basis selain e, kita memerlukan faktor koreksi berupa logaritma natural dari basis tersebut.

#### Rumus Dasar

Jika $y = a^u$ dimana $a > 0$, $a \neq 1$, dan $u$ adalah fungsi dari $x$, maka:

$$\boxed{y' = a^u \cdot u' \cdot \ln a}$$

Atau dalam notasi Leibniz:

$$\frac{dy}{dx} = a^u \cdot \ln a \cdot \frac{du}{dx}$$

#### Mengapa Ada Faktor ln a?

Kita dapat membuktikan rumus ini dengan mengubah ke basis e:
$$y = a^u = e^{u \ln a}$$

Menurunkan:
$$y' = e^{u \ln a} \cdot (u \ln a)' = e^{u \ln a} \cdot u' \cdot \ln a = a^u \cdot u' \cdot \ln a$$

#### Contoh 2.2.1

**Tentukan turunan dari** $y = 2^{\sin x}$

**Penyelesaian:**

Identifikasi:
- Basis: $a = 2$
- $u = \sin x$
- $u' = \cos x$

Menggunakan rumus:
$$y' = 2^{\sin x} \cdot \cos x \cdot \ln 2$$

$$\boxed{y' = 2^{\sin x} \cdot \cos x \cdot \ln 2}$$

#### Contoh 2.2.2

**Tentukan turunan dari** $y = 3^{x^2}$

**Penyelesaian:**

Identifikasi:
- Basis: $a = 3$
- $u = x^2$
- $u' = 2x$

Menggunakan rumus:
$$y' = 3^{x^2} \cdot 2x \cdot \ln 3$$

$$\boxed{y' = 2x \cdot 3^{x^2} \cdot \ln 3}$$

#### Contoh 2.2.3

**Tentukan turunan dari** $y = 5^{\cos x}$

**Penyelesaian:**

Identifikasi:
- Basis: $a = 5$
- $u = \cos x$
- $u' = -\sin x$

Menggunakan rumus:
$$y' = 5^{\cos x} \cdot (-\sin x) \cdot \ln 5$$

$$\boxed{y' = -5^{\cos x} \cdot \sin x \cdot \ln 5}$$

---

## 3. Turunan Tingkat Tinggi (Orde Tinggi)

### 3.1 Konsep Dasar

Turunan suatu fungsi, yang juga merupakan suatu fungsi, masih dapat diturunkan lagi asalkan memenuhi syarat-syarat turunan, yaitu masih memiliki faktor yang akan diturunkan.

**Definisi:**
- **Turunan pertama** dari fungsi $f$ adalah $f'(x)$
- **Turunan kedua** dari fungsi $f$ didefinisikan sebagai turunan dari fungsi turunan pertama
- **Turunan ke-n** dari fungsi $f$ didefinisikan sebagai turunan dari fungsi turunan ke-(n-1)

### 3.2 Notasi Turunan Tingkat Tinggi

Ada beberapa cara untuk menuliskan turunan tingkat tinggi:

| Orde | Notasi Lagrange | Notasi Leibniz | Notasi Operator |
|------|-----------------|----------------|-----------------|
| Pertama | $f'(x)$ atau $y'$ | $\frac{dy}{dx}$ | $D_x y$ |
| Kedua | $f''(x)$ atau $y''$ | $\frac{d^2y}{dx^2}$ | $D^2_x y$ |
| Ketiga | $f'''(x)$ atau $y'''$ | $\frac{d^3y}{dx^3}$ | $D^3_x y$ |
| Keempat | $f^{(4)}(x)$ atau $f^{iv}(x)$ | $\frac{d^4y}{dx^4}$ | $D^4_x y$ |
| ke-n | $f^{(n)}(x)$ | $\frac{d^ny}{dx^n}$ | $D^n_x y$ |

**Catatan:**
- Untuk turunan orde 4 ke atas, digunakan angka dalam kurung: $f^{(4)}(x)$, $f^{(5)}(x)$, dst.
- Notasi dengan tanda prima (') hanya praktis hingga orde 3

### 3.3 Contoh Perhitungan

#### Contoh 3.3.1

**Untuk fungsi** $f(x) = 2x^4$, **tentukan** $f'(x)$, $f''(x)$, $f'''(x)$, **dan** $f^{(4)}(x)$

**Penyelesaian:**

$$f(x) = 2x^4$$

**Turunan pertama:**
$$f'(x) = 2 \cdot 4x^3 = 8x^3$$

**Turunan kedua:**
$$f''(x) = 8 \cdot 3x^2 = 24x^2$$

**Turunan ketiga:**
$$f'''(x) = 24 \cdot 2x = 48x$$

**Turunan keempat:**
$$f^{(4)}(x) = 48$$

**Turunan kelima dan seterusnya:**
$$f^{(5)}(x) = 0$$

#### Contoh 3.3.2

**Untuk fungsi** $f(x) = e^{2x}$, **tentukan** $f''(x)$

**Penyelesaian:**

$$f(x) = e^{2x}$$

**Turunan pertama:**
$$f'(x) = 2e^{2x}$$

**Turunan kedua:**
$$f''(x) = 2 \cdot 2e^{2x} = 4e^{2x}$$

**Pola umum:**
$$f^{(n)}(x) = 2^n e^{2x}$$

#### Contoh 3.3.3

**Untuk fungsi** $f(x) = \sin x$, **tentukan turunan hingga orde 4**

**Penyelesaian:**

$$f(x) = \sin x$$
$$f'(x) = \cos x$$
$$f''(x) = -\sin x$$
$$f'''(x) = -\cos x$$
$$f^{(4)}(x) = \sin x$$

**Perhatikan:** Turunan fungsi trigonometri bersifat siklis dengan periode 4!

---

## 4. Turunan Fungsi Implisit

### 4.1 Fungsi Eksplisit vs Implisit

#### Fungsi Eksplisit

Jika hubungan antara $y$ dan $x$ dapat dituliskan dalam bentuk $y = f(x)$, maka $y$ disebut **fungsi eksplisit** dari $x$.

**Contoh fungsi eksplisit:**
- $y = x^2 + 3x - 5$
- $y = \sin x + \cos x$
- $y = e^x + \ln x$

#### Fungsi Implisit

Bila hubungan antara $y$ dan $x$ tidak dapat (atau sulit) dinyatakan dalam bentuk $y = f(x)$, maka dikatakan $y$ adalah **fungsi implisit dari $x$**.

**Syarat:** $F(x, y) = 0$

**Contoh fungsi implisit:**
- $x^3y^2 + x^2 + y = 10$
- $\sin(xy) + x^2 + y^2 + 1 = 0$
- $x^2 + y^2 = 25$ (persamaan lingkaran)

### 4.2 Metode Diferensiasi Implisit

Untuk mencari turunan dari fungsi implisit, kita menggunakan **diferensiasi implisit** dengan prinsip:

1. **Menurunkan tiap suku terhadap $x$ dan $y$ secara bergantian**
2. Bila diturunkan terhadap $x$, maka $y$ dianggap sebagai **konstanta**
3. Bila diturunkan terhadap $y$, maka $x$ dianggap sebagai **konstanta**
4. **Penting:** Ketika menurunkan terhadap $y$, hasil harus dikalikan dengan $y'$ (atau $\frac{dy}{dx}$)

#### Mengapa Perlu Dikalikan y'?

Berdasarkan aturan rantai (chain rule), karena $y$ adalah fungsi dari $x$:
$$\frac{d}{dx}[f(y)] = f'(y) \cdot \frac{dy}{dx} = f'(y) \cdot y'$$

### 4.3 Langkah-langkah Penyelesaian

1. **Turunkan** setiap suku dalam persamaan terhadap $x$
2. **Ingat:** Setiap kali menurunkan suku yang mengandung $y$, kalikan dengan $y'$
3. **Kumpulkan** semua suku yang mengandung $y'$ di satu ruas
4. **Faktorkan** $y'$
5. **Selesaikan** untuk mendapatkan $y'$

### 4.4 Contoh Penerapan

#### Contoh 4.4.1

**Tentukan** $\frac{dy}{dx}$ **dari bentuk implisit berikut:**
$$xy + x^3 + y^2x^2 = 0$$

**Penyelesaian:**

Turunkan setiap suku terhadap $x$:

| Suku | Turunan thd x | Turunan thd y |
|------|---------------|---------------|
| $xy$ | $y$ | $x \cdot y'$ |
| $x^3$ | $3x^2$ | $0$ |
| $y^2x^2$ | $2y^2x$ | $2yx^2 \cdot y'$ |

Gabungkan:
$$(y + 3x^2 + 2y^2x) + (x + 0 + 2yx^2) \cdot y' = 0$$

Pindahkan dan selesaikan:
$$(x + 2yx^2) \cdot y' = -(y + 3x^2 + 2y^2x)$$

$$\boxed{y' = -\frac{y + 3x^2 + 2y^2x}{x + 2yx^2}}$$

#### Contoh 4.4.2

**Tentukan** $\frac{dy}{dx}$ **dari:**
$$x^2 + y^2 = 25$$

**Penyelesaian:**

Turunkan kedua ruas terhadap $x$:
$$2x + 2y \cdot y' = 0$$

Selesaikan untuk $y'$:
$$2y \cdot y' = -2x$$

$$\boxed{y' = -\frac{x}{y}}$$

**Interpretasi Geometris:** Ini adalah gradien garis singgung pada lingkaran dengan pusat (0,0) dan jari-jari 5.

#### Contoh 4.4.3

**Tentukan** $\frac{dy}{dx}$ **dari:**
$$e^{xy} = x + y$$

**Penyelesaian:**

Turunkan kedua ruas:
$$e^{xy} \cdot (y + x \cdot y') = 1 + y'$$

Ekspansi:
$$ye^{xy} + xe^{xy} \cdot y' = 1 + y'$$

Kumpulkan suku $y'$:
$$xe^{xy} \cdot y' - y' = 1 - ye^{xy}$$

Faktorkan:
$$y'(xe^{xy} - 1) = 1 - ye^{xy}$$

$$\boxed{y' = \frac{1 - ye^{xy}}{xe^{xy} - 1}}$$

---

## 5. Latihan Soal

### Turunan Implisit

**Soal 1.** Tentukan turunan implisit dari persamaan berikut:
$$(x + 2y - 3)(2x - 3y + 4) = 10$$

**Soal 2.** Tentukan turunan implisit dari persamaan berikut pada titik $(2, 3)$:
$$25x^2 + 9y^2 - 70x - 30y = -49$$

**Soal 3.** Tentukan turunan implisit dari persamaan berikut:
$$x \cos y + y \cos x = 1$$

### Turunan Tingkat Tinggi

**Soal 4.** Tentukan turunan kedua dari fungsi berikut:
$$y = x^2 \cos 2x$$

**Soal 5.** Tentukan turunan kelima dari:
$$y = \sin 2x$$

### Turunan Eksponen

**Soal 6.** Tentukan turunan dari:
$$y = x^2 \cdot 3^x$$

**Soal 7.** Tentukan turunan dari:
$$y = e^{x \cos \theta} \cdot \cos(x \sin \theta)$$

*(Catatan: θ adalah konstanta)*

---

## 6. Rangkuman

### Rumus-rumus Penting

| Jenis | Rumus |
|-------|-------|
| Turunan $e^u$ | $\frac{d}{dx}(e^u) = e^u \cdot u'$ |
| Turunan $a^u$ | $\frac{d}{dx}(a^u) = a^u \cdot u' \cdot \ln a$ |
| Turunan ke-n | $f^{(n)}(x) = \frac{d^ny}{dx^n}$ |
| Diferensiasi Implisit | Turunkan tiap suku, kalikan $y'$ untuk suku $y$ |

### Poin-poin Kunci

1. **Turunan Eksponen Basis e**: Selalu kalikan dengan turunan dari eksponen (aturan rantai)

2. **Turunan Eksponen Basis a**: Jangan lupa faktor $\ln a$

3. **Turunan Tingkat Tinggi**: 
   - Turunkan secara bertahap
   - Perhatikan pola yang muncul (terutama untuk fungsi trigonometri)

4. **Diferensiasi Implisit**:
   - Setiap turunan suku $y$ harus dikalikan $y'$
   - Kumpulkan semua $y'$ di satu ruas
   - Faktorkan dan selesaikan

---

### Referensi

1. Stewart, J. (2015). *Calculus: Early Transcendentals*. 8th Edition. Cengage Learning.
2. Anton, H., Bivens, I., & Davis, S. (2012). *Calculus*. 10th Edition. Wiley.
3. Purcell, E. J., Varberg, D., & Rigdon, S. E. (2007). *Kalkulus Jilid 1*. Edisi 9. Erlangga.

---

*Materi disusun untuk keperluan pembelajaran Kalkulus - Pertemuan 13*
