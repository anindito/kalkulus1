# Penggunaan Turunan (Applications of Derivatives)

**Penulis:** Anindito, S.Kom., S.S., S.H., M.TI., CHFI.

---
[Slide](https://anindito.github.io/kalkulus1/pertemuan14/)
## Daftar Isi

1. [Pendahuluan](#1-pendahuluan)
2. [Dalil L'Hôpital](#2-dalil-lhôpital)
   - 2.1 [Pengertian](#21-pengertian)
   - 2.2 [Bentuk-Bentuk Tak Tentu](#22-bentuk-bentuk-tak-tentu)
   - 2.3 [Contoh Penerapan](#23-contoh-penerapan)
3. [Aplikasi Turunan](#3-aplikasi-turunan)
   - 3.1 [Garis Singgung dan Garis Normal](#31-garis-singgung-dan-garis-normal)
   - 3.2 [Kemonotonan Fungsi](#32-kemonotonan-fungsi)
   - 3.3 [Kecekungan Kurva](#33-kecekungan-kurva)
   - 3.4 [Titik Stasioner](#34-titik-stasioner)
   - 3.5 [Nilai Maksimum dan Minimum](#35-nilai-maksimum-dan-minimum)
4. [Latihan Soal](#4-latihan-soal)
5. [Referensi](#5-referensi)

---

## 1. Pendahuluan

Turunan merupakan salah satu konsep fundamental dalam kalkulus yang memiliki berbagai aplikasi praktis dalam matematika, fisika, ekonomi, dan berbagai bidang ilmu lainnya. Materi ini membahas secara komprehensif penggunaan turunan dalam menyelesaikan berbagai permasalahan matematika, mulai dari perhitungan limit dengan bentuk tak tentu hingga optimasi fungsi.

### Tujuan Pembelajaran

Setelah mempelajari materi ini, mahasiswa diharapkan mampu:

1. Memahami dan menerapkan Dalil L'Hôpital untuk menghitung limit bentuk tak tentu
2. Menentukan persamaan garis singgung dan garis normal pada suatu kurva
3. Menganalisis kemonotonan dan kecekungan fungsi menggunakan turunan
4. Menemukan titik stasioner dan menentukan jenisnya
5. Menghitung nilai maksimum dan minimum fungsi pada interval tertentu

---

## 2. Dalil L'Hôpital

### 2.1 Pengertian

**Dalil L'Hôpital** (L'Hôpital's Rule) merupakan metode untuk menghitung limit yang menghasilkan **bentuk tak tentu** (*indeterminate form*). Dalil ini dikembangkan oleh matematikawan Prancis Guillaume de l'Hôpital (1661-1704) berdasarkan karya Johann Bernoulli.

#### Pernyataan Dalil L'Hôpital

Misalkan $f$ dan $g$ adalah fungsi-fungsi yang terdiferensiasi pada interval terbuka $I$ yang memuat titik $a$ (kecuali mungkin di $a$ sendiri). Jika:

$$\lim_{x \to a} f(x) = 0 \quad \text{dan} \quad \lim_{x \to a} g(x) = 0$$

atau

$$\lim_{x \to a} f(x) = \pm\infty \quad \text{dan} \quad \lim_{x \to a} g(x) = \pm\infty$$

dan $g'(x) \neq 0$ untuk semua $x$ dalam $I$ (kecuali mungkin di $a$), maka:

$$\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}$$

asalkan limit di ruas kanan ada (atau sama dengan $\pm\infty$).

#### Interpretasi

Dalil L'Hôpital menyatakan bahwa untuk bentuk tak tentu $\frac{0}{0}$ atau $\frac{\infty}{\infty}$, kita dapat menghitung limit dengan cara **membagi turunan pembilang dengan turunan penyebut**.

### 2.2 Bentuk-Bentuk Tak Tentu

Selain bentuk dasar $\frac{0}{0}$ dan $\frac{\infty}{\infty}$, terdapat beberapa bentuk tak tentu lain yang dapat diselesaikan dengan Dalil L'Hôpital setelah dilakukan transformasi:

| Bentuk Tak Tentu | Transformasi ke Bentuk L'Hôpital |
|------------------|----------------------------------|
| $\frac{0}{0}$ | Langsung gunakan L'Hôpital |
| $\frac{\infty}{\infty}$ | Langsung gunakan L'Hôpital |
| $0 \cdot \infty$ | Ubah ke $\frac{0}{1/\infty}$ atau $\frac{\infty}{1/0}$ |
| $\infty - \infty$ | Ubah ke bentuk pecahan tunggal |
| $0^0$ | Gunakan logaritma natural: $y = f^g \Rightarrow \ln y = g \ln f$ |
| $1^\infty$ | Gunakan logaritma natural |
| $\infty^0$ | Gunakan logaritma natural |
| $0^\infty$ | Perlu analisis lebih lanjut |

#### Penjelasan Detail Setiap Bentuk

**1. Bentuk $0 \cdot \infty$**

Jika $\lim_{x \to a} f(x) = 0$ dan $\lim_{x \to a} g(x) = \infty$, maka:
$$\lim_{x \to a} f(x) \cdot g(x) = \lim_{x \to a} \frac{f(x)}{1/g(x)} = \frac{0}{0}$$

**2. Bentuk $\infty - \infty$**

Ubah ke bentuk pecahan dengan menyamakan penyebut atau faktorisasi.

**3. Bentuk Eksponensial ($0^0$, $1^\infty$, $\infty^0$)**

Untuk $y = [f(x)]^{g(x)}$, ambil logaritma natural:
$$\ln y = g(x) \ln f(x)$$

Kemudian hitung $\lim_{x \to a} \ln y$, dan hasilnya adalah $y = e^{\lim \ln y}$.

### 2.3 Contoh Penerapan

#### Contoh 1: Bentuk $\frac{0}{0}$

**Soal:** Hitung $\displaystyle\lim_{x \to 9} \frac{\sqrt{x+7} - 4}{x - 9}$

**Penyelesaian:**

Substitusi langsung: $\frac{\sqrt{9+7} - 4}{9-9} = \frac{\sqrt{16} - 4}{0} = \frac{4-4}{0} = \frac{0}{0}$ (bentuk tak tentu)

Terapkan Dalil L'Hôpital:

- Pembilang: $f(x) = \sqrt{x+7} - 4$, maka $f'(x) = \frac{1}{2\sqrt{x+7}}$
- Penyebut: $g(x) = x - 9$, maka $g'(x) = 1$

$$\lim_{x \to 9} \frac{\sqrt{x+7} - 4}{x - 9} = \lim_{x \to 9} \frac{\frac{1}{2\sqrt{x+7}}}{1} = \lim_{x \to 9} \frac{1}{2\sqrt{x+7}}$$

Substitusi $x = 9$:
$$= \frac{1}{2\sqrt{9+7}} = \frac{1}{2\sqrt{16}} = \frac{1}{2 \cdot 4} = \frac{1}{8}$$

**Jawaban:** $\boxed{\frac{1}{8}}$

#### Contoh 2: Bentuk $\frac{\infty}{\infty}$

**Soal:** Hitung $\displaystyle\lim_{x \to \infty} \frac{3x^2 + 2x}{5x^2 - x + 1}$

**Penyelesaian:**

Substitusi langsung menghasilkan $\frac{\infty}{\infty}$, maka gunakan L'Hôpital:

$$\lim_{x \to \infty} \frac{3x^2 + 2x}{5x^2 - x + 1} = \lim_{x \to \infty} \frac{6x + 2}{10x - 1}$$

Masih bentuk $\frac{\infty}{\infty}$, terapkan L'Hôpital lagi:

$$= \lim_{x \to \infty} \frac{6}{10} = \frac{3}{5}$$

**Jawaban:** $\boxed{\frac{3}{5}}$

#### Contoh 3: Bentuk $0 \cdot \infty$

**Soal:** Hitung $\displaystyle\lim_{x \to 0^+} x \ln x$

**Penyelesaian:**

Bentuk $0 \cdot (-\infty)$, ubah ke:
$$\lim_{x \to 0^+} x \ln x = \lim_{x \to 0^+} \frac{\ln x}{1/x} = \frac{-\infty}{\infty}$$

Terapkan L'Hôpital:
$$= \lim_{x \to 0^+} \frac{1/x}{-1/x^2} = \lim_{x \to 0^+} \frac{x^2}{-x} = \lim_{x \to 0^+} (-x) = 0$$

**Jawaban:** $\boxed{0}$

---

## 3. Aplikasi Turunan

### 3.1 Garis Singgung dan Garis Normal

#### Definisi Garis Singgung

**Garis singgung** pada kurva $y = f(x)$ di titik $(x_0, y_0)$ adalah garis yang hanya memiliki satu titik singgung dengan kurva di titik tersebut dan memiliki gradien sama dengan nilai turunan fungsi di titik itu.

**Rumus Gradien Garis Singgung:**
$$m = f'(x_0)$$

**Persamaan Garis Singgung:**
$$y - y_0 = m(x - x_0)$$

atau
$$y - f(x_0) = f'(x_0)(x - x_0)$$

#### Definisi Garis Normal

**Garis normal** adalah garis yang tegak lurus dengan garis singgung di titik singgung. Hubungan antara gradien garis singgung ($m_1$) dan gradien garis normal ($m_2$) adalah:

$$m_1 \cdot m_2 = -1$$

atau
$$m_2 = -\frac{1}{m_1} = -\frac{1}{f'(x_0)}$$

**Persamaan Garis Normal:**
$$y - y_0 = -\frac{1}{f'(x_0)}(x - x_0)$$

#### Contoh Soal

**Soal:** Tentukan gradien garis singgung kurva $y = x^2 - 8x + 12$ di titik $(1, 5)$.

**Penyelesaian:**

1. Tentukan turunan fungsi:
   $$f(x) = x^2 - 8x + 12$$
   $$f'(x) = 2x - 8$$

2. Hitung gradien di $x = 1$:
   $$m = f'(1) = 2(1) - 8 = 2 - 8 = -6$$

**Jawaban:** Gradien garis singgung adalah $\boxed{-6}$

#### Contoh Soal Lanjutan

**Soal:** Tentukan persamaan garis singgung dan garis normal pada kurva $y = x^3 - 2x + 1$ di titik $(1, 0)$.

**Penyelesaian:**

1. Turunan: $f'(x) = 3x^2 - 2$
2. Gradien di $x = 1$: $m_1 = f'(1) = 3(1)^2 - 2 = 1$
3. Persamaan garis singgung:
   $$y - 0 = 1(x - 1) \Rightarrow y = x - 1$$
4. Gradien garis normal: $m_2 = -\frac{1}{1} = -1$
5. Persamaan garis normal:
   $$y - 0 = -1(x - 1) \Rightarrow y = -x + 1$$

### 3.2 Kemonotonan Fungsi

#### Teorema Kemonotonan

Misalkan $f(x)$ adalah fungsi yang memiliki turunan pada interval tertutup $[a, b]$.

**Fungsi Naik (Increasing):**
Jika $f'(x) > 0$ untuk semua $x \in [a, b]$, maka fungsi $f$ **naik** pada interval $[a, b]$.

*Interpretasi:* Nilai fungsi meningkat seiring bertambahnya nilai $x$.

**Fungsi Turun (Decreasing):**
Jika $f'(x) < 0$ untuk semua $x \in [a, b]$, maka fungsi $f$ **turun** pada interval $[a, b]$.

*Interpretasi:* Nilai fungsi menurun seiring bertambahnya nilai $x$.

**Fungsi Konstan:**
Jika $f'(x) = 0$ untuk semua $x \in [a, b]$, maka fungsi $f$ **konstan** pada interval $[a, b]$.

#### Langkah Menentukan Interval Kemonotonan

1. Tentukan turunan pertama $f'(x)$
2. Cari titik-titik kritis (nilai $x$ di mana $f'(x) = 0$ atau tidak terdefinisi)
3. Buat garis bilangan dan uji tanda $f'(x)$ pada setiap interval
4. Tentukan interval naik ($f'(x) > 0$) dan turun ($f'(x) < 0$)

#### Contoh Soal

**Soal:** Jika $f(x) = 2x^3 - 3x^2 - 12x + 7$, tentukan interval di mana fungsi naik dan turun.

**Penyelesaian:**

1. **Turunan pertama:**
   $$f'(x) = 6x^2 - 6x - 12 = 6(x^2 - x - 2) = 6(x + 1)(x - 2)$$

2. **Titik kritis:** $f'(x) = 0$
   $$6(x + 1)(x - 2) = 0$$
   $$x = -1 \quad \text{atau} \quad x = 2$$

3. **Uji tanda pada interval:**

   | Interval | Tanda $(x+1)$ | Tanda $(x-2)$ | Tanda $f'(x)$ | Kesimpulan |
   |----------|---------------|---------------|---------------|------------|
   | $x < -1$ | $-$ | $-$ | $+$ | Naik |
   | $-1 < x < 2$ | $+$ | $-$ | $-$ | Turun |
   | $x > 2$ | $+$ | $+$ | $+$ | Naik |

**Jawaban:**
- Fungsi **naik** pada interval $(-\infty, -1)$ dan $(2, \infty)$
- Fungsi **turun** pada interval $(-1, 2)$

### 3.3 Kecekungan Kurva

#### Teorema Kecekungan

Misalkan $f(x)$ adalah fungsi yang memiliki turunan kedua pada interval terbuka $I$.

**Cekung ke Atas (Concave Up):**
Jika $f''(x) > 0$ untuk semua $x \in [a, b]$, maka grafik fungsi $f$ **cekung ke atas** pada interval $I$.

*Karakteristik:* Kurva berbentuk seperti mangkuk terbuka ke atas. Garis singgung berada di bawah kurva.

**Cekung ke Bawah (Concave Down):**
Jika $f''(x) < 0$ untuk semua $x \in [a, b]$, maka grafik fungsi $f$ **cekung ke bawah** pada interval $I$.

*Karakteristik:* Kurva berbentuk seperti mangkuk terbuka ke bawah. Garis singgung berada di atas kurva.

#### Titik Belok (Inflection Point)

**Titik belok** adalah titik pada kurva di mana kecekungan berubah (dari cekung ke atas menjadi cekung ke bawah, atau sebaliknya).

Titik $(c, f(c))$ adalah titik belok jika $f''(c) = 0$ dan $f''(x)$ berubah tanda di sekitar $x = c$.

#### Contoh Soal

**Soal:** Tentukan interval kecekungan dari fungsi $f(x) = \frac{1}{3}x^3 - x^2 - 3x + 4$.

**Penyelesaian:**

1. **Turunan pertama:**
   $$f'(x) = x^2 - 2x - 3$$

2. **Turunan kedua:**
   $$f''(x) = 2x - 2$$

3. **Titik belok potensial:** $f''(x) = 0$
   $$2x - 2 = 0 \Rightarrow x = 1$$

4. **Uji tanda $f''(x)$:**

   - Untuk $x < 1$: $f''(x) = 2x - 2 < 0$ → Cekung ke bawah
   - Untuk $x > 1$: $f''(x) = 2x - 2 > 0$ → Cekung ke atas

**Jawaban:**
- Fungsi **cekung ke atas** pada interval $(1, \infty)$
- Fungsi **cekung ke bawah** pada interval $(-\infty, 1)$
- **Titik belok** di $x = 1$

### 3.4 Titik Stasioner

#### Definisi

**Titik stasioner** (disebut juga **titik kritis** atau **titik ekstrim** atau **titik balik**) adalah titik pada kurva di mana gradien garis singgung bernilai nol.

Secara matematis, jika fungsi $f(x)$ kontinu dan terdiferensiasi, maka $f(a)$ dikatakan **nilai stasioner** dari $f(x)$ **jika dan hanya jika:**

$$f'(a) = 0$$

#### Jenis-Jenis Titik Stasioner

1. **Titik Maksimum Lokal:** Titik di mana fungsi mencapai nilai tertinggi di sekitarnya
2. **Titik Minimum Lokal:** Titik di mana fungsi mencapai nilai terendah di sekitarnya
3. **Titik Belok (Inflection Point):** Titik di mana fungsi tidak mencapai ekstrem tetapi kecekungan berubah

#### Uji Turunan Pertama

Untuk menentukan jenis titik stasioner di $x = c$:

| Kondisi | Jenis Titik Stasioner |
|---------|----------------------|
| $f'(x)$ berubah dari $+$ ke $-$ | Maksimum lokal |
| $f'(x)$ berubah dari $-$ ke $+$ | Minimum lokal |
| $f'(x)$ tidak berubah tanda | Titik belok |

#### Uji Turunan Kedua

Jika $f'(c) = 0$, maka:

| Kondisi | Jenis Titik Stasioner |
|---------|----------------------|
| $f''(c) < 0$ | Maksimum lokal |
| $f''(c) > 0$ | Minimum lokal |
| $f''(c) = 0$ | Tidak dapat ditentukan (gunakan uji turunan pertama) |

#### Contoh Soal

**Soal:** Tentukan titik stasioner dari $f(x) = 2x^2 - 12x + 20$.

**Penyelesaian:**

1. **Turunan pertama:**
   $$f'(x) = 4x - 12$$

2. **Titik stasioner:** $f'(x) = 0$
   $$4x - 12 = 0$$
   $$4x = 12$$
   $$x = 3$$

3. **Nilai stasioner:**
   $$f(3) = 2(3)^2 - 12(3) + 20 = 2(9) - 36 + 20 = 18 - 36 + 20 = 2$$

4. **Verifikasi dengan turunan kedua:**
   $$f''(x) = 4 > 0$$
   
   Karena $f''(3) = 4 > 0$, maka titik $(3, 2)$ adalah titik **minimum lokal**.

**Jawaban:** Titik stasioner adalah $(3, 2)$ yang merupakan titik minimum lokal.

### 3.5 Nilai Maksimum dan Minimum

#### Definisi

Misalkan $S$ adalah suatu himpunan tak kosong, dan fungsi $f$ mengandung titik $c$.

**Nilai Maksimum:**
$f(c)$ adalah **nilai maksimum** $f$ pada $S$ jika $f(c) \geq f(x)$ untuk semua $x \in S$.

**Nilai Minimum:**
$f(c)$ adalah **nilai minimum** $f$ pada $S$ jika $f(c) \leq f(x)$ untuk semua $x \in S$.

#### Maksimum/Minimum Global vs Lokal

- **Maksimum/Minimum Global (Absolut):** Nilai tertinggi/terendah pada seluruh domain
- **Maksimum/Minimum Lokal (Relatif):** Nilai tertinggi/terendah pada suatu interval terbatas

#### Teorema Nilai Ekstrem

Jika $f$ adalah fungsi kontinu pada interval tertutup $[a, b]$, maka $f$ memiliki nilai maksimum dan minimum absolut pada $[a, b]$.

#### Langkah Mencari Nilai Maksimum dan Minimum pada $[a, b]$

1. Tentukan turunan $f'(x)$
2. Cari semua titik kritis di dalam interval $(a, b)$ dengan menyelesaikan $f'(x) = 0$
3. Hitung nilai fungsi di:
   - Semua titik kritis di dalam interval
   - Titik-titik ujung interval ($x = a$ dan $x = b$)
4. Nilai terbesar adalah **maksimum**, nilai terkecil adalah **minimum**

#### Contoh Soal

**Soal:** Tentukan nilai maksimum dan minimum dari fungsi $f(x) = x^2 - 6x + 5$ pada interval $0 \leq x \leq 5$.

**Penyelesaian:**

1. **Turunan pertama:**
   $$f'(x) = 2x - 6$$

2. **Titik kritis:**
   $$f'(x) = 0 \Rightarrow 2x - 6 = 0 \Rightarrow x = 3$$
   
   Titik kritis $x = 3$ berada dalam interval $[0, 5]$ ✓

3. **Evaluasi nilai fungsi:**
   
   - Di titik kritis $x = 3$:
     $$f(3) = (3)^2 - 6(3) + 5 = 9 - 18 + 5 = -4$$
   
   - Di ujung interval $x = 0$:
     $$f(0) = (0)^2 - 6(0) + 5 = 5$$
   
   - Di ujung interval $x = 5$:
     $$f(5) = (5)^2 - 6(5) + 5 = 25 - 30 + 5 = 0$$

4. **Perbandingan:**

   | $x$ | $f(x)$ |
   |-----|--------|
   | $0$ | $5$ |
   | $3$ | $-4$ |
   | $5$ | $0$ |

**Jawaban:**
- **Nilai maksimum** = $5$ (dicapai di $x = 0$)
- **Nilai minimum** = $-4$ (dicapai di $x = 3$)

---

## 4. Latihan Soal

### Soal 1: Sketsa Grafik
Sketsakan grafik fungsi:
$$f(x) = \frac{x^2 - 2x + 4}{x - 2}$$

*Petunjuk:* Tentukan domain, asimtot, titik potong sumbu, kemonotonan, kecekungan, dan titik stasioner.

### Soal 2: Limit dengan L'Hôpital
Tentukan nilai limit berikut:

**a.** $\displaystyle\lim_{x \to 1} \frac{x^3 - 1}{x^3 - 2x^2 + 2x - 1}$

**b.** $\displaystyle\lim_{x \to 0} \frac{\ln(\tan x)}{\ln(\tan 2x)}$

**c.** $\displaystyle\lim_{x \to 0} x \cdot \cot 2x$

**d.** $\displaystyle\lim_{x \to 0} x^x$

---

## 5. Referensi

1. Stewart, J. (2015). *Calculus: Early Transcendentals* (8th ed.). Cengage Learning.
2. Purcell, E. J., Varberg, D., & Rigdon, S. E. (2007). *Kalkulus* (9th ed.). Erlangga.
3. Thomas, G. B., Weir, M. D., & Hass, J. (2018). *Thomas' Calculus* (14th ed.). Pearson.
4. Anton, H., Bivens, I., & Davis, S. (2012). *Calculus: Early Transcendentals* (10th ed.). Wiley.

---

**© 2024 - Anindito, S.Kom., S.S., S.H., M.TI., CHFI.**

*Materi ini disusun untuk keperluan pembelajaran mata kuliah Kalkulus.*
