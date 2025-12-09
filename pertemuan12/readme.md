# Turunan Fungsi Logaritma

**Materi Pertemuan 12 - Kalkulus**  


---

## Daftar Isi

1. [Pendahuluan](#1-pendahuluan)
2. [Konsep Dasar Logaritma](#2-konsep-dasar-logaritma)
3. [Turunan Logaritma Natural (ln)](#3-turunan-logaritma-natural-ln)
4. [Turunan Logaritma Umum (basis a)](#4-turunan-logaritma-umum-basis-a)
5. [Penerapan Aturan Rantai](#5-penerapan-aturan-rantai)
6. [Kombinasi dengan Aturan Turunan Lainnya](#6-kombinasi-dengan-aturan-turunan-lainnya)
7. [Aplikasi Logaritma dalam Statistik](#7-aplikasi-logaritma-dalam-statistik)
8. [Latihan Soal Bertingkat](#8-latihan-soal-bertingkat)
9. [Rangkuman](#9-rangkuman)

---

## 1. Pendahuluan

Turunan fungsi logaritma merupakan salah satu topik fundamental dalam kalkulus diferensial. Pemahaman yang baik tentang turunan logaritma sangat penting karena fungsi logaritma banyak digunakan dalam berbagai bidang seperti fisika, ekonomi, statistik, dan ilmu komputer.

### Tujuan Pembelajaran

Setelah mempelajari materi ini, mahasiswa diharapkan mampu:

1. Memahami konsep dasar logaritma natural dan logaritma umum
2. Menurunkan fungsi logaritma natural menggunakan rumus dasar
3. Menurunkan fungsi logaritma dengan basis sembarang
4. Menerapkan aturan rantai pada turunan fungsi logaritma
5. Mengkombinasikan turunan logaritma dengan aturan turunan lainnya
6. Memahami aplikasi transformasi logaritma dalam analisis data

---

## 2. Konsep Dasar Logaritma

### 2.1 Definisi Logaritma

Logaritma adalah operasi kebalikan (invers) dari eksponensial. Jika $a^b = c$, maka $\log_a c = b$.

### 2.2 Jenis-Jenis Logaritma

#### Logaritma Natural (ln)

Logaritma natural adalah logaritma dengan basis bilangan Euler $e \approx 2.71828$. Notasi yang digunakan adalah $\ln(x)$ atau kadang ditulis $\log_e(x)$.

**Sifat penting bilangan Euler:**
- $e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n$
- $e \approx 2.71828182845...$
- $e$ adalah bilangan irasional dan transenden

#### Logaritma Umum (Common Logarithm)

Logaritma umum adalah logaritma dengan basis 10, dinotasikan sebagai $\log(x)$ atau $\log_{10}(x)$.

#### Logaritma Basis Sembarang

Logaritma dengan basis $a$ (dimana $a > 0$ dan $a \neq 1$) dinotasikan sebagai $^a\log(x)$ atau $\log_a(x)$.

### 2.3 Sifat-Sifat Logaritma

1. **Logaritma Perkalian:** $\log_a(xy) = \log_a(x) + \log_a(y)$
2. **Logaritma Pembagian:** $\log_a\left(\frac{x}{y}\right) = \log_a(x) - \log_a(y)$
3. **Logaritma Pangkat:** $\log_a(x^n) = n \cdot \log_a(x)$
4. **Perubahan Basis:** $\log_a(x) = \frac{\ln(x)}{\ln(a)} = \frac{\log_b(x)}{\log_b(a)}$
5. **Identitas:** $\log_a(a) = 1$ dan $\log_a(1) = 0$

---

## 3. Turunan Logaritma Natural (ln)

### 3.1 Rumus Dasar

Jika $y = \ln(u)$, dimana $u$ adalah fungsi dari $x$, maka turunannya adalah:

$$\boxed{y' = \frac{1}{u} \cdot u'}$$

Atau dalam notasi Leibniz:

$$\frac{d}{dx}[\ln(u)] = \frac{1}{u} \cdot \frac{du}{dx}$$

**Kasus khusus:** Jika $u = x$, maka $u' = 1$, sehingga:

$$\frac{d}{dx}[\ln(x)] = \frac{1}{x}$$

### 3.2 Pembuktian

Turunan $\ln(x)$ dapat dibuktikan menggunakan definisi limit turunan:

$$\frac{d}{dx}[\ln(x)] = \lim_{h \to 0} \frac{\ln(x+h) - \ln(x)}{h}$$

$$= \lim_{h \to 0} \frac{1}{h} \ln\left(\frac{x+h}{x}\right)$$

$$= \lim_{h \to 0} \frac{1}{h} \ln\left(1 + \frac{h}{x}\right)$$

$$= \lim_{h \to 0} \ln\left(1 + \frac{h}{x}\right)^{\frac{1}{h}}$$

Dengan substitusi $n = \frac{x}{h}$, saat $h \to 0$, maka $n \to \infty$:

$$= \frac{1}{x} \ln\left(\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n\right) = \frac{1}{x} \ln(e) = \frac{1}{x}$$

### 3.3 Contoh Penerapan

#### Contoh 1: Turunan Sederhana

**Soal:** Tentukan turunan dari $y = \ln(2x)$

**Penyelesaian:**

Diketahui: $y = \ln(2x)$

Misalkan $u = 2x$, maka $u' = 2$

Menggunakan rumus: $y' = \frac{1}{u} \cdot u'$

$$y' = \frac{1}{2x} \cdot 2 = \frac{2}{2x} = \frac{1}{x}$$

**Jawaban:** $y' = \frac{1}{x}$

#### Contoh 2: Turunan dengan Fungsi Kuadrat

**Soal:** Tentukan turunan dari $y = \ln(x^2 + 1)$

**Penyelesaian:**

Diketahui: $y = \ln(x^2 + 1)$

Misalkan $u = x^2 + 1$, maka $u' = 2x$

$$y' = \frac{1}{x^2 + 1} \cdot 2x = \frac{2x}{x^2 + 1}$$

**Jawaban:** $y' = \frac{2x}{x^2 + 1}$

#### Contoh 3: Turunan dengan Fungsi Trigonometri

**Soal:** Tentukan turunan dari $y = \ln(\sin 3x)$

**Penyelesaian:**

Diketahui: $y = \ln(\sin 3x)$

Misalkan $u = \sin 3x$

Turunan $u$: $u' = \cos 3x \cdot 3 = 3\cos 3x$ (aturan rantai)

$$y' = \frac{1}{\sin 3x} \cdot 3\cos 3x = \frac{3\cos 3x}{\sin 3x} = 3\cot 3x$$

**Jawaban:** $y' = 3\cot 3x$

---

## 4. Turunan Logaritma Umum (Basis a)

### 4.1 Rumus Dasar

Jika $y = {^a}\log(u)$ atau $y = \log_a(u)$, dimana $u$ adalah fungsi dari $x$ dan $a > 0, a \neq 1$, maka turunannya adalah:

$$\boxed{y' = \frac{1}{u} \cdot u' \cdot \frac{1}{\ln a}}$$

Atau dapat ditulis:

$$\frac{d}{dx}[\log_a(u)] = \frac{u'}{u \cdot \ln a}$$

### 4.2 Pembuktian

Dengan menggunakan rumus perubahan basis:

$$\log_a(u) = \frac{\ln(u)}{\ln(a)}$$

Karena $\ln(a)$ adalah konstanta, maka:

$$\frac{d}{dx}[\log_a(u)] = \frac{1}{\ln(a)} \cdot \frac{d}{dx}[\ln(u)] = \frac{1}{\ln(a)} \cdot \frac{u'}{u} = \frac{u'}{u \cdot \ln a}$$

### 4.3 Contoh Penerapan

#### Contoh 1: Logaritma Basis 2

**Soal:** Tentukan turunan dari $y = {^2}\log(3x + 1)$

**Penyelesaian:**

Diketahui: $y = {^2}\log(3x + 1)$

Misalkan $u = 3x + 1$, maka $u' = 3$

Basis $a = 2$, sehingga $\ln a = \ln 2$

$$y' = \frac{1}{3x + 1} \cdot 3 \cdot \frac{1}{\ln 2} = \frac{3}{(3x + 1) \cdot \ln 2}$$

**Jawaban:** $y' = \frac{3}{(3x + 1) \ln 2}$

#### Contoh 2: Logaritma Basis 10

**Soal:** Tentukan turunan dari $y = \log_{10}(x^2 - 4)$

**Penyelesaian:**

Diketahui: $y = \log_{10}(x^2 - 4)$

Misalkan $u = x^2 - 4$, maka $u' = 2x$

$$y' = \frac{2x}{(x^2 - 4) \cdot \ln 10}$$

**Jawaban:** $y' = \frac{2x}{(x^2 - 4) \ln 10}$

#### Contoh 3: Logaritma Basis Sembarang

**Soal:** Tentukan turunan dari $y = {^a}\log(3x^2 - 5)$

**Penyelesaian:**

Diketahui: $y = {^a}\log(3x^2 - 5)$

Misalkan $u = 3x^2 - 5$, maka $u' = 6x$

$$y' = \frac{6x}{(3x^2 - 5) \cdot \ln a}$$

**Jawaban:** $y' = \frac{6x}{(3x^2 - 5) \ln a}$

---

## 5. Penerapan Aturan Rantai

### 5.1 Konsep Aturan Rantai pada Logaritma

Aturan rantai (chain rule) sangat penting ketika fungsi di dalam logaritma merupakan fungsi komposit. Jika $y = \ln(f(g(x)))$, maka:

$$y' = \frac{1}{f(g(x))} \cdot f'(g(x)) \cdot g'(x)$$

### 5.2 Contoh Penerapan

#### Contoh 1: Logaritma Pangkat

**Soal:** Tentukan turunan dari $y = \ln(x + 3)^2$

**Penyelesaian:**

**Metode 1: Menggunakan sifat logaritma**

$$y = \ln(x + 3)^2 = 2\ln(x + 3)$$

$$y' = 2 \cdot \frac{1}{x + 3} = \frac{2}{x + 3}$$

**Metode 2: Langsung dengan aturan rantai**

Misalkan $u = (x + 3)^2$, maka $u' = 2(x + 3)$

$$y' = \frac{1}{(x + 3)^2} \cdot 2(x + 3) = \frac{2(x + 3)}{(x + 3)^2} = \frac{2}{x + 3}$$

**Jawaban:** $y' = \frac{2}{x + 3}$

#### Contoh 2: Logaritma dengan Fungsi Trigonometri Komposit

**Soal:** Tentukan turunan dari $y = \ln(\sin^2 x)$

**Penyelesaian:**

$$y = \ln(\sin^2 x) = 2\ln(\sin x)$$

$$y' = 2 \cdot \frac{1}{\sin x} \cdot \cos x = \frac{2\cos x}{\sin x} = 2\cot x$$

**Jawaban:** $y' = 2\cot x$

---

## 6. Kombinasi dengan Aturan Turunan Lainnya

### 6.1 Turunan Perkalian dengan Logaritma

Jika $y = f(x) \cdot \log_a(g(x))$, gunakan aturan perkalian:

$$y' = f'(x) \cdot \log_a(g(x)) + f(x) \cdot \frac{g'(x)}{g(x) \cdot \ln a}$$

#### Contoh:

**Soal:** Tentukan turunan dari $y = x \cdot \log(3x^2 - 5)$

**Penyelesaian:**

Diketahui: $y = x \cdot \log(3x^2 - 5)$

Misalkan $f(x) = x$ dan $g(x) = \log(3x^2 - 5)$

$f'(x) = 1$

$g'(x) = \frac{6x}{(3x^2 - 5) \ln 10}$

$$y' = 1 \cdot \log(3x^2 - 5) + x \cdot \frac{6x}{(3x^2 - 5) \ln 10}$$

$$y' = \log(3x^2 - 5) + \frac{6x^2}{(3x^2 - 5) \ln 10}$$

### 6.2 Turunan Pembagian dengan Logaritma

Jika $y = \frac{\ln(f(x))}{g(x)}$, gunakan aturan pembagian:

$$y' = \frac{g(x) \cdot \frac{f'(x)}{f(x)} - \ln(f(x)) \cdot g'(x)}{[g(x)]^2}$$

#### Contoh:

**Soal:** Tentukan turunan dari $y = \frac{\ln x}{\sin x}$

**Penyelesaian:**

Misalkan $f(x) = \ln x$ dan $g(x) = \sin x$

$f'(x) = \frac{1}{x}$

$g'(x) = \cos x$

Menggunakan aturan pembagian:

$$y' = \frac{\sin x \cdot \frac{1}{x} - \ln x \cdot \cos x}{\sin^2 x}$$

$$y' = \frac{\frac{\sin x}{x} - \ln x \cdot \cos x}{\sin^2 x}$$

$$y' = \frac{\sin x - x \ln x \cdot \cos x}{x \sin^2 x}$$

---

## 7. Aplikasi Logaritma dalam Statistik

### 7.1 Transformasi Data

Transformasi logaritma sering digunakan dalam statistik untuk:

1. **Mengubah distribusi miring (skewed)** menjadi lebih simetris
2. **Menstabilkan varians** pada data heteroskedastis
3. **Memenuhi asumsi normalitas** dalam analisis statistik parametrik

### 7.2 Contoh Kasus: Uji Normalitas

Berikut contoh penerapan transformasi logaritma menggunakan R:

**Data Asli:**
```r
data <- c(2, 3, 3, 4, 4, 5, 6, 7, 25, 30, 40)
shapiro.test(data)
```

**Hasil:**
```
Shapiro-Wilk normality test
data: data
W = 0.72049, p-value = 0.0008595
```

Karena p-value < α (0,05), maka data **tidak berdistribusi normal**.

**Setelah Transformasi Logaritma:**
```r
data_log <- log(data)
shapiro.test(data_log)
```

**Hasil:**
```
Shapiro-Wilk normality test
data: data_log
W = 0.86995, p-value = 0.0774
```

Karena p-value > α (0,05), maka data yang ditransformasi **berdistribusi normal**.

### 7.3 Interpretasi

Transformasi logaritma berhasil mengubah data yang awalnya tidak normal menjadi berdistribusi normal. Hal ini sangat penting ketika akan melakukan analisis statistik yang mensyaratkan asumsi normalitas, seperti:

- Uji-t
- ANOVA
- Regresi linear
- Analisis korelasi Pearson

---

## 8. Latihan Soal Bertingkat

### Tingkat Dasar

**Soal 1:** Tentukan turunan dari $y = \ln(5x)$

<details>
<summary><b>Lihat Jawaban</b></summary>

$u = 5x$, $u' = 5$

$y' = \frac{1}{5x} \cdot 5 = \frac{1}{x}$

</details>

**Soal 2:** Tentukan turunan dari $y = \ln(x^3)$

<details>
<summary><b>Lihat Jawaban</b></summary>

Cara 1: $y = 3\ln x$, maka $y' = \frac{3}{x}$

Cara 2: $u = x^3$, $u' = 3x^2$, maka $y' = \frac{3x^2}{x^3} = \frac{3}{x}$

</details>

**Soal 3:** Tentukan turunan dari $y = {^{10}}\log(2x)$

<details>
<summary><b>Lihat Jawaban</b></summary>

$y' = \frac{2}{2x \cdot \ln 10} = \frac{1}{x \ln 10}$

</details>

### Tingkat Menengah

**Soal 4:** Tentukan turunan dari $y = \ln(\sin 3x)$

<details>
<summary><b>Lihat Jawaban</b></summary>

$u = \sin 3x$, $u' = 3\cos 3x$

$y' = \frac{3\cos 3x}{\sin 3x} = 3\cot 3x$

</details>

**Soal 5:** Tentukan turunan dari $y = x \cdot \log(3x^2 - 5)$

<details>
<summary><b>Lihat Jawaban</b></summary>

Gunakan aturan perkalian:

$y' = 1 \cdot \log(3x^2 - 5) + x \cdot \frac{6x}{(3x^2 - 5) \ln 10}$

$y' = \log(3x^2 - 5) + \frac{6x^2}{(3x^2 - 5) \ln 10}$

</details>

**Soal 6:** Tentukan turunan dari $y = {^a}\log(3x^2 - 5)$

<details>
<summary><b>Lihat Jawaban</b></summary>

$u = 3x^2 - 5$, $u' = 6x$

$y' = \frac{6x}{(3x^2 - 5) \ln a}$

</details>

### Tingkat Lanjut

**Soal 7:** Tentukan turunan dari $y = \ln(x + 3)^2$

<details>
<summary><b>Lihat Jawaban</b></summary>

$y = 2\ln(x + 3)$

$y' = \frac{2}{x + 3}$

</details>

**Soal 8:** Tentukan turunan dari $y = \frac{\ln x}{\sin x}$

<details>
<summary><b>Lihat Jawaban</b></summary>

Gunakan aturan pembagian:

$y' = \frac{\sin x \cdot \frac{1}{x} - \ln x \cdot \cos x}{\sin^2 x}$

$y' = \frac{\sin x - x\ln x \cos x}{x\sin^2 x}$

</details>

**Soal 9:** Tentukan turunan dari $y = \ln\left(\frac{x^2 + 1}{x^2 - 1}\right)$

<details>
<summary><b>Lihat Jawaban</b></summary>

$y = \ln(x^2 + 1) - \ln(x^2 - 1)$

$y' = \frac{2x}{x^2 + 1} - \frac{2x}{x^2 - 1}$

$y' = 2x\left(\frac{1}{x^2 + 1} - \frac{1}{x^2 - 1}\right)$

$y' = 2x\left(\frac{x^2 - 1 - x^2 - 1}{(x^2 + 1)(x^2 - 1)}\right)$

$y' = \frac{-4x}{x^4 - 1}$

</details>

**Soal 10:** Tentukan turunan dari $y = \ln(\ln x)$

<details>
<summary><b>Lihat Jawaban</b></summary>

Misalkan $u = \ln x$, maka $u' = \frac{1}{x}$

$y' = \frac{1}{\ln x} \cdot \frac{1}{x} = \frac{1}{x \ln x}$

</details>

---

## 9. Rangkuman

### Rumus-Rumus Penting

| Fungsi | Turunan |
|--------|---------|
| $y = \ln x$ | $y' = \frac{1}{x}$ |
| $y = \ln u$ | $y' = \frac{u'}{u}$ |
| $y = \log_a x$ | $y' = \frac{1}{x \ln a}$ |
| $y = \log_a u$ | $y' = \frac{u'}{u \ln a}$ |

### Poin-Poin Penting

1. **Logaritma natural** menggunakan basis $e \approx 2.71828$
2. **Aturan rantai** selalu diperlukan ketika argument logaritma bukan variabel sederhana
3. **Sifat logaritma** dapat menyederhanakan perhitungan turunan
4. **Transformasi logaritma** berguna untuk normalisasi data dalam statistik
5. Selalu perhatikan **domain fungsi**: logaritma hanya terdefinisi untuk argumen positif

### Tips Mengerjakan Soal

1. Identifikasi jenis logaritma (natural atau basis a)
2. Tentukan fungsi $u$ yang ada di dalam logaritma
3. Hitung turunan dari $u$
4. Terapkan rumus yang sesuai
5. Sederhanakan hasil akhir jika memungkinkan

---

**Referensi:**
- Stewart, James. *Calculus: Early Transcendentals*
- Purcell, Edwin J., Dale Varberg, Steven E. Rigdon. *Kalkulus*
- Materi Kuliah Matematika Teknik, Universitas Pertahanan

---

*Materi ini disusun untuk keperluan pembelajaran mata kuliah Kalkulus.*
