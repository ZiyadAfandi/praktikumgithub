# Tugas

---
## Dekomposisi matriks

---

kolom matriks dari $4 \times 4$ pilihanmu sebagai vektor awal:


$$a_1 = \begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix}, \quad a_2 = \begin{bmatrix} 2 \\ 3 \\ 4 \\ 1 \end{bmatrix}, \quad a_3 = \begin{bmatrix} 3 \\ 4 \\ 1 \\ 2 \end{bmatrix}, \quad a_4 = \begin{bmatrix} 4 \\ 1 \\ 2 \\ 3 \end{bmatrix}$$

---

## 1. Menghitung $v_1$ dan $q_1$

Sesuai urutan dasar Gram-Schmidt, langkah pertama mengambil langsung nilai dari vektor pertama:


$$v_1 = a_1 = \begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix}$$

### Hitung Norma $|v_1|$:

$$|v_1| = \sqrt{1^2 + 2^2 + 3^2 + 4^2} = \sqrt{1 + 4 + 9 + 16} = \sqrt{30}$$

### Hitung Vektor Satuan $q_1$:

$$q_1 = \frac{v_1}{|v_1|} = \frac{1}{\sqrt{30}} \begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix}$$

---

## 2. Menghitung $v_2$ dan $q_2$

Mengikuti pola rumus umum $v_k$ di papan tulis bagian kanan: $v_2 = a_2 - (a_2 \cdot q_1)q_1$

### Hitung Dot Product $(a_2 \cdot q_1)$:

$$(a_2 \cdot q_1) = \frac{1}{\sqrt{30}} \big((2 \times 1) + (3 \times 2) + (4 \times 3) + (1 \times 4)\big) = \frac{2 + 6 + 12 + 4}{\sqrt{30}} = \frac{24}{\sqrt{30}}$$

### Hitung Vektor $v_2$:

$$v_2 = \begin{bmatrix} 2 \\ 3 \\ 4 \\ 1 \end{bmatrix} - \frac{24}{\sqrt{30}} \cdot \frac{1}{\sqrt{30}} \begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix} = \begin{bmatrix} 2 \\ 3 \\ 4 \\ 1 \end{bmatrix} - \frac{24}{30} \begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix}$$

Karena $\frac{24}{30} = \frac{4}{5}$, maka:


$$v_2 = \begin{bmatrix} 2 \\ 3 \\ 4 \\ 1 \end{bmatrix} - \begin{bmatrix} 4/5 \\ 8/5 \\ 12/5 \\ 16/5 \end{bmatrix} = \begin{bmatrix} 6/5 \\ 7/5 \\ 8/5 \\ -11/5 \end{bmatrix} = \frac{1}{5} \begin{bmatrix} 6 \\ 7 \\ 8 \\ -11 \end{bmatrix}$$

### Hitung Norma $|v_2|$:

$$|v_2| = \sqrt{\left(\frac{6}{5}\right)^2 + \left(\frac{7}{5}\right)^2 + \left(\frac{8}{5}\right)^2 + \left(-\frac{11}{5}\right)^2} = \sqrt{\frac{36 + 49 + 64 + 121}{25}} = \sqrt{\frac{270}{25}} = \frac{\sqrt{270}}{5} = \frac{3\sqrt{30}}{5}$$

### Hitung Vektor Satuan $q_2$:

$$q_2 = \frac{v_2}{|v_2|} = \frac{5}{3\sqrt{30}} \cdot \frac{1}{5} \begin{bmatrix} 6 \\ 7 \\ 8 \\ -11 \end{bmatrix} = \frac{1}{3\sqrt{30}} \begin{bmatrix} 6 \\ 7 \\ 8 \\ -11 \end{bmatrix} = \frac{1}{\sqrt{270}} \begin{bmatrix} 6 \\ 7 \\ 8 \\ -11 \end{bmatrix}$$

---

## 3. Menghitung $v_3$ dan $q_3$

Mengikuti rumus persis di papan tulis bagian kiri atas:


$$v_3 = a_3 - \big((a_3 \cdot q_1)q_1 + (a_3 \cdot q_2)q_2\big)$$

### Hitung Dot Product $(a_3 \cdot q_1)$ dan $(a_3 \cdot q_2)$:

$$(a_3 \cdot q_1) = \frac{1}{\sqrt{30}} \big((3 \times 1) + (4 \times 2) + (1 \times 3) + (2 \times 4)\big) = \frac{3 + 8 + 3 + 8}{\sqrt{30}} = \frac{22}{\sqrt{30}}$$

$$(a_3 \cdot q_2) = \frac{1}{3\sqrt{30}} \big((3 \times 6) + (4 \times 7) + (1 \times 8) + (2 \times -11)\big) = \frac{18 + 28 + 8 - 22}{3\sqrt{30}} = \frac{32}{3\sqrt{30}}$$

### Hitung Vektor $v_3$:

$$v_3 = \begin{bmatrix} 3 \\ 4 \\ 1 \\ 2 \end{bmatrix} - \left( \frac{22}{30} \begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix} + \frac{32}{270} \begin{bmatrix} 6 \\ 7 \\ 8 \\ -11 \end{bmatrix} \right)$$

Sederhanakan pengurangnya ke penyebut $135$:


$$v_3 = \begin{bmatrix} 3 \\ 4 \\ 1 \\ 2 \end{bmatrix} - \left( \begin{bmatrix} 99/135 \\ 198/135 \\ 297/135 \\ 396/135 \end{bmatrix} + \begin{bmatrix} 96/135 \\ 112/135 \\ 128/135 \\ -176/135 \end{bmatrix} \right) = \begin{bmatrix} 3 \\ 4 \\ 1 \\ 2 \end{bmatrix} - \begin{bmatrix} 195/135 \\ 310/135 \\ 425/135 \\ 220/135 \end{bmatrix}$$

$$v_3 = \begin{bmatrix} 3 \\ 4 \\ 1 \\ 2 \end{bmatrix} - \begin{bmatrix} 13/9 \\ 62/27 \\ 85/27 \\ 44/27 \end{bmatrix} = \begin{bmatrix} 81/27 - 39/27 \\ 108/27 - 62/27 \\ 27/27 - 85/27 \\ 54/27 - 44/27 \end{bmatrix} = \begin{bmatrix} 42/27 \\ 46/27 \\ -58/27 \\ 10/27 \end{bmatrix} = \frac{2}{27} \begin{bmatrix} 21 \\ 23 \\ -29 \\ 5 \end{bmatrix}$$

### Hitung Norma $|v_3|$:

$$|v_3| = \frac{2}{27} \sqrt{21^2 + 23^2 + (-29)^2 + 5^2} = \frac{2}{27} \sqrt{441 + 529 + 841 + 25} = \frac{2\sqrt{1836}}{27} = \frac{12\sqrt{51}}{27} = \frac{4\sqrt{51}}{9}$$

### Hitung Vektor Satuan $q_3$:

$$q_3 = \frac{v_3}{|v_3|} = \frac{2}{27} \cdot \frac{27}{12\sqrt{51}} \begin{bmatrix} 21 \\ 23 \\ -29 \\ 5 \end{bmatrix} = \frac{1}{6\sqrt{51}} \begin{bmatrix} 21 \\ 23 \\ -29 \\ 5 \end{bmatrix}$$

---

## 4. Menghitung $v_4$ dan $q_4$

Mengikuti rumus persis di papan tulis bagian kanan atas:


$$v_4 = a_4 - \big((a_4 \cdot q_1)q_1 + (a_4 \cdot q_2)q_2 + (a_4 \cdot q_3)q_3\big)$$

### Hitung Dot Product:

$$(a_4 \cdot q_1) = \frac{1}{\sqrt{30}}\big((4 \times 1) + (1 \times 2) + (2 \times 3) + (3 \times 4)\big) = \frac{24}{\sqrt{30}}$$

$$(a_4 \cdot q_2) = \frac{1}{3\sqrt{30}}\big((4 \times 6) + (1 \times 7) + (2 \times 8) + (3 \times -11)\big) = \frac{24 + 7 + 16 - 33}{3\sqrt{30}} = \frac{14}{3\sqrt{30}}$$

$$(a_4 \cdot q_3) = \frac{1}{6\sqrt{51}}\big((4 \times 21) + (1 \times 23) + (2 \times -29) + (3 \times 5)\big) = \frac{84 + 23 - 58 + 15}{6\sqrt{51}} = \frac{64}{6\sqrt{51}} = \frac{32}{3\sqrt{51}}$$

### Hitung Vektor $v_4$:

$$v_4 = \begin{bmatrix} 4 \\ 1 \\ 2 \\ 3 \end{bmatrix} - \left( \frac{24}{30}\begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix} + \frac{14}{270}\begin{bmatrix} 6 \\ 7 \\ 8 \\ -11 \end{bmatrix} + \frac{32}{1836}\begin{bmatrix} 21 \\ 23 \\ -29 \\ 5 \end{bmatrix} \right)$$

$$v_4 = \begin{bmatrix} 4 \\ 1 \\ 2 \\ 3 \end{bmatrix} - \left( \frac{4}{5}\begin{bmatrix} 1 \\ 2 \\ 3 \\ 4 \end{bmatrix} + \frac{7}{135}\begin{bmatrix} 6 \\ 7 \\ 8 \\ -11 \end{bmatrix} + \frac{8}{459}\begin{bmatrix} 21 \\ 23 \\ -29 \\ 5 \end{bmatrix} \right) = \frac{2}{17} \begin{bmatrix} 9 \\ -9 \\ 3 \\ -3 \end{bmatrix} = \frac{6}{17} \begin{bmatrix} 3 \\ -3 \\ 1 \\ -1 \end{bmatrix}$$

### Hitung Norma $|v_4|$:

$$|v_4| = \frac{6}{17}\sqrt{3^2 + (-3)^2 + 1^2 + (-1)^2} = \frac{6}{17}\sqrt{9 + 9 + 1 + 1} = \frac{6\sqrt{20}}{17} = \frac{12\sqrt{5}}{17}$$

### Hitung Vektor Satuan $q_4$:

$$q_4 = \frac{v_4}{|v_4|} = \frac{1}{\sqrt{20}} \begin{bmatrix} 3 \\ -3 \\ 1 \\ -1 \end{bmatrix} = \frac{1}{2\sqrt{5}} \begin{bmatrix} 3 \\ -3 \\ 1 \\ -1 \end{bmatrix}$$

---

## 5. Menyusun Matriks $R$

Sesuai template penulisan matriks $R$ segitiga atas pada papan tulis sebelah kiri (dengan dot product $a_k \cdot q_i$ di mana $a_k \cdot q_k = |v_k|$):

$$R = \begin{bmatrix}
a_1 \cdot q_1 & a_2 \cdot q_1 & a_3 \cdot q_1 & a_4 \cdot q_1 \
0 & a_2 \cdot q_2 & a_3 \cdot q_2 & a_4 \cdot q_2 \
0 & 0 & a_3 \cdot q_3 & a_4 \cdot q_3 \
0 & 0 & 0 & a_4 \cdot q_4
\end{bmatrix}$$

Memasukkan seluruh komponen eksak pecahan dan akar di atas, kita dapatkan struktur final matriks $R$:

$$R = \begin{bmatrix}
\sqrt{30} & \frac{24}{\sqrt{30}} & \frac{22}{\sqrt{30}} & \frac{24}{\sqrt{30}} \
0 & \frac{3\sqrt{30}}{5} & \frac{32}{3\sqrt{30}} & \frac{14}{3\sqrt{30}} \
0 & 0 & \frac{4\sqrt{51}}{9} & \frac{32}{3\sqrt{51}} \
0 & 0 & 0 & \frac{12\sqrt{5}}{17}
\end{bmatrix}$$