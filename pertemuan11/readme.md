# Turunan Fungsi Trigonometri
## Pertemuan 11


---

## Daftar Isi

1. [Pendahuluan](#pendahuluan)
2. [Konsep Dasar Limit dalam Turunan](#konsep-dasar-limit-dalam-turunan)
3. [Turunan Fungsi Sinus](#turunan-fungsi-sinus)
4. [Turunan Fungsi Cosinus](#turunan-fungsi-cosinus)
5. [Turunan Fungsi Tangen](#turunan-fungsi-tangen)
6. [Turunan Fungsi Cotangen](#turunan-fungsi-cotangen)
7. [Turunan Fungsi Secan](#turunan-fungsi-secan)
8. [Turunan Fungsi Cosecan](#turunan-fungsi-cosecan)
9. [Aturan Rantai pada Fungsi Trigonometri](#aturan-rantai-pada-fungsi-trigonometri)
10. [Contoh Soal dan Pembahasan](#contoh-soal-dan-pembahasan)
11. [Latihan Mandiri](#latihan-mandiri)
12. [Ringkasan Rumus](#ringkasan-rumus)

---

## Pendahuluan

Turunan fungsi trigonometri merupakan salah satu topik fundamental dalam kalkulus diferensial. Pemahaman yang baik tentang turunan fungsi-fungsi trigonometri sangat penting karena:

1. **Aplikasi dalam Fisika:** Analisis gerak harmonik, gelombang, dan osilasi
2. **Teknik Elektro:** Analisis sinyal AC dan rangkaian listrik
3. **Teknik Mesin:** Analisis getaran dan dinamika
4. **Matematika Lanjut:** Dasar untuk integral trigonometri dan persamaan diferensial

### Prasyarat Pengetahuan

Sebelum mempelajari materi ini, pastikan Anda memahami:

- Definisi turunan menggunakan limit
- Identitas trigonometri dasar
- Aturan-aturan turunan (aturan hasil kali, hasil bagi, dan rantai)
- Nilai limit trigonometri khusus

---

## Konsep Dasar Limit dalam Turunan

### Definisi Turunan

Turunan fungsi f(x) didefinisikan sebagai:

$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

### Limit Trigonometri Penting

Dalam menurunkan rumus turunan fungsi trigonometri, kita memerlukan dua limit fundamental:

#### Limit Pertama
$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

**Interpretasi geometris:** Ketika sudut x mendekati nol, panjang busur (sin x) mendekati panjang tali busur (x dalam radian).

#### Limit Kedua
$$\lim_{x \to 0} \frac{\cos x - 1}{x} = 0$$

**Catatan:** Limit ini juga dapat ditulis sebagai:
$$\lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$

### Identitas Trigonometri yang Diperlukan

#### Rumus Penjumlahan Sudut

| Identitas | Rumus |
|-----------|-------|
| sin(A + B) | sin A cos B + cos A sin B |
| sin(A - B) | sin A cos B - cos A sin B |
| cos(A + B) | cos A cos B - sin A sin B |
| cos(A - B) | cos A cos B + sin A sin B |

#### Identitas Pythagoras

$$\sin^2 x + \cos^2 x = 1$$
$$1 + \tan^2 x = \sec^2 x$$
$$1 + \cot^2 x = \csc^2 x$$

---

## Turunan Fungsi Sinus

### Teorema

$$\frac{d}{dx}(\sin x) = \cos x$$

Atau dalam notasi Lagrange:
$$f(x) = \sin x \Rightarrow f'(x) = \cos x$$

### Pembuktian Lengkap

Menggunakan definisi turunan:

**Langkah 1:** Tuliskan definisi turunan
$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$

**Langkah 2:** Substitusi f(x) = sin x
$$f'(x) = \lim_{h \to 0} \frac{\sin(x+h) - \sin x}{h}$$

**Langkah 3:** Gunakan identitas sin(A + B) = sin A cos B + cos A sin B
$$f'(x) = \lim_{h \to 0} \frac{\sin x \cos h + \cos x \sin h - \sin x}{h}$$

**Langkah 4:** Kelompokkan suku-suku yang mengandung sin x
$$f'(x) = \lim_{h \to 0} \frac{\sin x (\cos h - 1) + \cos x \sin h}{h}$$

**Langkah 5:** Pisahkan menjadi dua limit
$$f'(x) = \lim_{h \to 0} \left[ \sin x \cdot \frac{\cos h - 1}{h} + \cos x \cdot \frac{\sin h}{h} \right]$$

**Langkah 6:** Distribusikan limit
$$f'(x) = \sin x \cdot \lim_{h \to 0} \frac{\cos h - 1}{h} + \cos x \cdot \lim_{h \to 0} \frac{\sin h}{h}$$

**Langkah 7:** Substitusi nilai limit yang diketahui
- $\lim_{h \to 0} \frac{\cos h - 1}{h} = 0$
- $\lim_{h \to 0} \frac{\sin h}{h} = 1$

$$f'(x) = \sin x \cdot 0 + \cos x \cdot 1$$

**Langkah 8:** Sederhanakan
$$f'(x) = \cos x$$

### Interpretasi Grafis

Grafik turunan sin x adalah cos x, yang menunjukkan:
- Ketika sin x mencapai maksimum (x = π/2), gradiennya = 0, dan cos(π/2) = 0 ✓
- Ketika sin x = 0 dan naik (x = 0), gradiennya maksimum, dan cos(0) = 1 ✓
- Ketika sin x = 0 dan turun (x = π), gradiennya minimum, dan cos(π) = -1 ✓

---

## Turunan Fungsi Cosinus

### Teorema

$$\frac{d}{dx}(\cos x) = -\sin x$$

Atau dalam notasi Lagrange:
$$f(x) = \cos x \Rightarrow f'(x) = -\sin x$$

### Pembuktian Lengkap

**Langkah 1:** Tuliskan definisi turunan
$$f'(x) = \lim_{h \to 0} \frac{\cos(x+h) - \cos x}{h}$$

**Langkah 2:** Gunakan identitas cos(A + B) = cos A cos B - sin A sin B
$$f'(x) = \lim_{h \to 0} \frac{\cos x \cos h - \sin x \sin h - \cos x}{h}$$

**Langkah 3:** Kelompokkan suku-suku yang mengandung cos x
$$f'(x) = \lim_{h \to 0} \frac{\cos x (\cos h - 1) - \sin x \sin h}{h}$$

**Langkah 4:** Pisahkan menjadi dua limit
$$f'(x) = \cos x \cdot \lim_{h \to 0} \frac{\cos h - 1}{h} - \sin x \cdot \lim_{h \to 0} \frac{\sin h}{h}$$

**Langkah 5:** Substitusi nilai limit
$$f'(x) = \cos x \cdot 0 - \sin x \cdot 1$$

**Langkah 6:** Sederhanakan
$$f'(x) = -\sin x$$

### Catatan Penting

Perhatikan tanda negatif! Ini adalah kesalahan umum yang sering terjadi. Turunan cos x adalah **negatif** sin x.

---

## Turunan Fungsi Tangen

### Teorema

$$\frac{d}{dx}(\tan x) = \sec^2 x$$

### Pembuktian menggunakan Aturan Hasil Bagi

Karena $\tan x = \frac{\sin x}{\cos x}$, kita gunakan aturan hasil bagi:

$$\frac{d}{dx}\left(\frac{u}{v}\right) = \frac{u'v - uv'}{v^2}$$

dengan u = sin x dan v = cos x.

**Langkah 1:** Tentukan u, v, u', dan v'
- u = sin x → u' = cos x
- v = cos x → v' = -sin x

**Langkah 2:** Terapkan aturan hasil bagi
$$\frac{d}{dx}(\tan x) = \frac{(\cos x)(\cos x) - (\sin x)(-\sin x)}{\cos^2 x}$$

**Langkah 3:** Sederhanakan pembilang
$$= \frac{\cos^2 x + \sin^2 x}{\cos^2 x}$$

**Langkah 4:** Gunakan identitas Pythagoras
$$= \frac{1}{\cos^2 x}$$

**Langkah 5:** Ubah ke bentuk secan
$$= \sec^2 x$$

### Bentuk Alternatif

Turunan tan x juga dapat ditulis sebagai:
$$\frac{d}{dx}(\tan x) = 1 + \tan^2 x$$

Ini dapat dibuktikan menggunakan identitas $\sec^2 x = 1 + \tan^2 x$.

---

## Turunan Fungsi Cotangen

### Teorema

$$\frac{d}{dx}(\cot x) = -\csc^2 x$$

### Pembuktian

Karena $\cot x = \frac{\cos x}{\sin x}$, kita gunakan aturan hasil bagi:

**Langkah 1:** Tentukan u, v, u', dan v'
- u = cos x → u' = -sin x
- v = sin x → v' = cos x

**Langkah 2:** Terapkan aturan hasil bagi
$$\frac{d}{dx}(\cot x) = \frac{(-\sin x)(\sin x) - (\cos x)(\cos x)}{\sin^2 x}$$

**Langkah 3:** Sederhanakan pembilang
$$= \frac{-\sin^2 x - \cos^2 x}{\sin^2 x}$$

**Langkah 4:** Faktorkan tanda negatif dan gunakan identitas Pythagoras
$$= \frac{-(\sin^2 x + \cos^2 x)}{\sin^2 x} = \frac{-1}{\sin^2 x}$$

**Langkah 5:** Ubah ke bentuk cosecan
$$= -\csc^2 x$$

---

## Turunan Fungsi Secan

### Teorema

$$\frac{d}{dx}(\sec x) = \sec x \tan x$$

### Pembuktian

Karena $\sec x = \frac{1}{\cos x} = (\cos x)^{-1}$, kita gunakan aturan rantai:

**Langkah 1:** Tuliskan dalam bentuk pangkat
$$\sec x = (\cos x)^{-1}$$

**Langkah 2:** Terapkan aturan rantai
$$\frac{d}{dx}(\sec x) = -1 \cdot (\cos x)^{-2} \cdot \frac{d}{dx}(\cos x)$$

**Langkah 3:** Substitusi turunan cos x
$$= -(\cos x)^{-2} \cdot (-\sin x)$$

**Langkah 4:** Sederhanakan
$$= \frac{\sin x}{\cos^2 x}$$

**Langkah 5:** Pisahkan pecahan
$$= \frac{1}{\cos x} \cdot \frac{\sin x}{\cos x}$$

**Langkah 6:** Ubah ke bentuk secan dan tangen
$$= \sec x \tan x$$

---

## Turunan Fungsi Cosecan

### Teorema

$$\frac{d}{dx}(\csc x) = -\csc x \cot x$$

### Pembuktian

Karena $\csc x = \frac{1}{\sin x} = (\sin x)^{-1}$:

**Langkah 1:** Tuliskan dalam bentuk pangkat
$$\csc x = (\sin x)^{-1}$$

**Langkah 2:** Terapkan aturan rantai
$$\frac{d}{dx}(\csc x) = -1 \cdot (\sin x)^{-2} \cdot \frac{d}{dx}(\sin x)$$

**Langkah 3:** Substitusi turunan sin x
$$= -(\sin x)^{-2} \cdot (\cos x)$$

**Langkah 4:** Sederhanakan
$$= -\frac{\cos x}{\sin^2 x}$$

**Langkah 5:** Pisahkan pecahan
$$= -\frac{1}{\sin x} \cdot \frac{\cos x}{\sin x}$$

**Langkah 6:** Ubah ke bentuk cosecan dan cotangen
$$= -\csc x \cot x$$

---

## Aturan Rantai pada Fungsi Trigonometri

### Prinsip Umum

Jika u adalah fungsi dari x, maka:

| Fungsi | Turunan |
|--------|---------|
| sin u | cos u · (du/dx) |
| cos u | -sin u · (du/dx) |
| tan u | sec² u · (du/dx) |
| cot u | -csc² u · (du/dx) |
| sec u | sec u tan u · (du/dx) |
| csc u | -csc u cot u · (du/dx) |

### Contoh Aplikasi Aturan Rantai

**Contoh 1:** Tentukan turunan dari y = sin(3x²)

**Penyelesaian:**
- Misalkan u = 3x², maka du/dx = 6x
- y = sin u

$$\frac{dy}{dx} = \cos u \cdot \frac{du}{dx} = \cos(3x^2) \cdot 6x = 6x\cos(3x^2)$$

**Contoh 2:** Tentukan turunan dari y = cos³(2x)

**Penyelesaian:**
- y = [cos(2x)]³
- Misalkan v = cos(2x), maka y = v³
- Turunan cos(2x) = -sin(2x) · 2 = -2sin(2x)

$$\frac{dy}{dx} = 3v^2 \cdot \frac{dv}{dx} = 3\cos^2(2x) \cdot (-2\sin(2x)) = -6\cos^2(2x)\sin(2x)$$

---

## Contoh Soal dan Pembahasan

### Soal 1
**Tentukan $\frac{dy}{dx}$ dari $y = \sin^4(x^3 + 5)$**

**Pembahasan:**

Ini adalah fungsi komposit berlapis. Mari kita uraikan:
- Fungsi terluar: u⁴
- Fungsi tengah: sin(v)
- Fungsi terdalam: v = x³ + 5

**Langkah 1:** Identifikasi struktur
$$y = [\sin(x^3 + 5)]^4$$

**Langkah 2:** Terapkan aturan rantai secara bertahap

Misalkan w = x³ + 5, maka dw/dx = 3x²

Misalkan u = sin w, maka du/dw = cos w

y = u⁴, maka dy/du = 4u³

**Langkah 3:** Gunakan aturan rantai
$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dw} \cdot \frac{dw}{dx}$$

$$= 4u^3 \cdot \cos w \cdot 3x^2$$

**Langkah 4:** Substitusi kembali
$$= 4\sin^3(x^3 + 5) \cdot \cos(x^3 + 5) \cdot 3x^2$$

$$\boxed{\frac{dy}{dx} = 12x^2 \sin^3(x^3 + 5) \cos(x^3 + 5)}$$

---

### Soal 2
**Carilah turunan dari $y = \frac{1 - \cos x}{1 + \cos x}$**

**Pembahasan:**

Gunakan aturan hasil bagi dengan u = 1 - cos x dan v = 1 + cos x

**Langkah 1:** Tentukan turunan pembilang dan penyebut
- u = 1 - cos x → u' = sin x
- v = 1 + cos x → v' = -sin x

**Langkah 2:** Terapkan aturan hasil bagi
$$\frac{dy}{dx} = \frac{u'v - uv'}{v^2}$$

$$= \frac{(\sin x)(1 + \cos x) - (1 - \cos x)(-\sin x)}{(1 + \cos x)^2}$$

**Langkah 3:** Jabarkan pembilang
$$= \frac{\sin x + \sin x \cos x + \sin x - \sin x \cos x}{(1 + \cos x)^2}$$

**Langkah 4:** Sederhanakan
$$= \frac{2\sin x}{(1 + \cos x)^2}$$

$$\boxed{\frac{dy}{dx} = \frac{2\sin x}{(1 + \cos x)^2}}$$

---

### Soal 3
**Carilah turunan dari $y = \frac{\sin x \cdot \sec x}{1 + \tan x}$**

**Pembahasan:**

**Langkah 1:** Sederhanakan terlebih dahulu
Karena $\sec x = \frac{1}{\cos x}$:
$$y = \frac{\sin x \cdot \frac{1}{\cos x}}{1 + \tan x} = \frac{\tan x}{1 + \tan x}$$

**Langkah 2:** Gunakan aturan hasil bagi
- u = tan x → u' = sec² x
- v = 1 + tan x → v' = sec² x

$$\frac{dy}{dx} = \frac{(\sec^2 x)(1 + \tan x) - (\tan x)(\sec^2 x)}{(1 + \tan x)^2}$$

**Langkah 3:** Sederhanakan pembilang
$$= \frac{\sec^2 x + \sec^2 x \tan x - \sec^2 x \tan x}{(1 + \tan x)^2}$$

$$= \frac{\sec^2 x}{(1 + \tan x)^2}$$

$$\boxed{\frac{dy}{dx} = \frac{\sec^2 x}{(1 + \tan x)^2}}$$

---

### Soal 4
**Carilah turunan dari $y = \sqrt{\frac{a\cos^2 x + b\sin^2 x}{\cos^2 x}}$ dengan a dan b konstanta**

**Pembahasan:**

**Langkah 1:** Sederhanakan ekspresi dalam akar
$$y = \sqrt{\frac{a\cos^2 x + b\sin^2 x}{\cos^2 x}}$$

$$= \sqrt{\frac{a\cos^2 x}{\cos^2 x} + \frac{b\sin^2 x}{\cos^2 x}}$$

$$= \sqrt{a + b\tan^2 x}$$

**Langkah 2:** Tuliskan dalam bentuk pangkat
$$y = (a + b\tan^2 x)^{1/2}$$

**Langkah 3:** Terapkan aturan rantai
$$\frac{dy}{dx} = \frac{1}{2}(a + b\tan^2 x)^{-1/2} \cdot \frac{d}{dx}(a + b\tan^2 x)$$

**Langkah 4:** Tentukan turunan bagian dalam
$$\frac{d}{dx}(a + b\tan^2 x) = b \cdot 2\tan x \cdot \sec^2 x = 2b\tan x \sec^2 x$$

**Langkah 5:** Gabungkan
$$\frac{dy}{dx} = \frac{1}{2\sqrt{a + b\tan^2 x}} \cdot 2b\tan x \sec^2 x$$

$$\boxed{\frac{dy}{dx} = \frac{b\tan x \sec^2 x}{\sqrt{a + b\tan^2 x}}}$$

---

### Soal 5
**Carilah turunan dari $y = \frac{2\sin^3 2x}{\cos^2 2x}$**

**Pembahasan:**

**Langkah 1:** Sederhanakan ekspresi
$$y = \frac{2\sin^3 2x}{\cos^2 2x} = 2\sin^3 2x \cdot \sec^2 2x$$

Atau tulis sebagai:
$$y = 2 \cdot \frac{\sin^3 2x}{\cos^2 2x} = 2\tan^2 2x \cdot \sin 2x$$

**Pendekatan alternatif - gunakan aturan hasil bagi langsung:**

- u = 2sin³(2x)
- v = cos²(2x)

**Langkah 2:** Tentukan u'
$$u' = 2 \cdot 3\sin^2(2x) \cdot \cos(2x) \cdot 2 = 12\sin^2(2x)\cos(2x)$$

**Langkah 3:** Tentukan v'
$$v' = 2\cos(2x) \cdot (-\sin(2x)) \cdot 2 = -4\sin(2x)\cos(2x)$$

**Langkah 4:** Terapkan aturan hasil bagi
$$\frac{dy}{dx} = \frac{u'v - uv'}{v^2}$$

$$= \frac{12\sin^2(2x)\cos(2x) \cdot \cos^2(2x) - 2\sin^3(2x) \cdot (-4\sin(2x)\cos(2x))}{\cos^4(2x)}$$

**Langkah 5:** Sederhanakan pembilang
$$= \frac{12\sin^2(2x)\cos^3(2x) + 8\sin^4(2x)\cos(2x)}{\cos^4(2x)}$$

$$= \frac{4\sin^2(2x)\cos(2x)[3\cos^2(2x) + 2\sin^2(2x)]}{\cos^4(2x)}$$

$$= \frac{4\sin^2(2x)[3\cos^2(2x) + 2\sin^2(2x)]}{\cos^3(2x)}$$

Menggunakan identitas $\sin^2 + \cos^2 = 1$:
$$= \frac{4\sin^2(2x)[3\cos^2(2x) + 2(1-\cos^2(2x))]}{\cos^3(2x)}$$

$$= \frac{4\sin^2(2x)[\cos^2(2x) + 2]}{\cos^3(2x)}$$

$$\boxed{\frac{dy}{dx} = \frac{4\sin^2(2x)(2 + \cos^2(2x))}{\cos^3(2x)}}$$

---

## Latihan Mandiri

Kerjakan soal-soal berikut untuk mengasah pemahaman Anda:

### Level Dasar

1. Tentukan turunan dari y = sin(5x)
2. Tentukan turunan dari y = cos(x² + 1)
3. Tentukan turunan dari y = tan(3x)

### Level Menengah

4. Tentukan turunan dari y = sin²x · cos x
5. Tentukan turunan dari y = sec(x³)
6. Tentukan turunan dari $y = \frac{\sin x}{x}$

### Level Lanjut

7. Tentukan turunan dari y = sin(cos(tan x))
8. Tentukan turunan dari $y = \sqrt{\sin x + \cos x}$
9. Tentukan turunan dari $y = \frac{\tan x - 1}{\sec x}$
10. Buktikan bahwa turunan dari arcsin(x) adalah $\frac{1}{\sqrt{1-x^2}}$

---

## Ringkasan Rumus

### Tabel Rumus Turunan Trigonometri Dasar

| No | Fungsi f(x) | Turunan f'(x) |
|----|-------------|---------------|
| 1 | sin x | cos x |
| 2 | cos x | -sin x |
| 3 | tan x | sec² x |
| 4 | cot x | -csc² x |
| 5 | sec x | sec x · tan x |
| 6 | csc x | -csc x · cot x |

### Tabel Rumus dengan Aturan Rantai

| No | Fungsi f(u) | Turunan (jika u = u(x)) |
|----|-------------|-------------------------|
| 1 | sin u | cos u · u' |
| 2 | cos u | -sin u · u' |
| 3 | tan u | sec² u · u' |
| 4 | cot u | -csc² u · u' |
| 5 | sec u | sec u · tan u · u' |
| 6 | csc u | -csc u · cot u · u' |

### Limit Penting

$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$

$$\lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$

$$\lim_{x \to 0} \frac{\tan x}{x} = 1$$

### Tips Mengingat

1. **Sin dan Cos:** Sin → Cos (positif), Cos → -Sin (negatif)
2. **Tan dan Cot:** Tan → Sec² (positif), Cot → -Csc² (negatif)
3. **Sec dan Csc:** Keduanya mengandung dirinya sendiri dalam turunan
   - Sec → Sec·Tan (positif)
   - Csc → -Csc·Cot (negatif)
4. **Pola tanda negatif:** Co-fungsi (cos, cot, csc) memiliki turunan negatif

---

## Referensi

1. Stewart, J. (2015). *Calculus: Early Transcendentals*. 8th Edition.
2. Purcell, E. J., Varberg, D., & Rigdon, S. E. (2007). *Kalkulus*. Edisi 9.
3. Materi Pertemuan 11: Turunan Fungsi Trigonometri - Nadiza Lediwara, S.T., M.Eng

---

*Dokumen ini disusun untuk keperluan pembelajaran matematika tingkat perguruan tinggi.*
