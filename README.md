# 🎥 OpenCV Image Processing & Drawing Tools

![Python](https://img.shields.io/badge/Python-3.x-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📌 Deskripsi Project
Project ini merupakan hasil praktik **Machine Learning / Computer Vision menggunakan OpenCV** yang berfokus pada pengolahan gambar dan video menggunakan Python.

Praktikum ini mencakup beberapa konsep dasar **Computer Vision**, seperti:
- Membaca dan menampilkan gambar
- Konversi warna gambar (BGR, RGB, Grayscale)
- Pengolahan video frame
- Menggambar objek (Line, Rectangle, Circle)
- Menambahkan teks pada gambar
- Interaksi mouse untuk menggambar
- Cropping gambar
- Membuat bounding box dan label objek

Project ini dibuat sebagai bagian dari **tugas praktikum Machine Learning**.

---

# 👨‍💻 Anggota Kelompok

**- Alfadrian Januarsyah (231001067)** <br>
**- Tasri Zulfitriyati (231001074)** <br> 
**- M. Irvan Maualana P. (231001071)** <br>
**- Nabila Isnaeni (231001054)** <br>
**- Silvia Fasya Aprilian (231001002)** <br>

---

# 📂 Struktur Project

```

Tugas_Kelompok_3_ML
│
├── OpenCV_3.ipynb
├── results
├── sunflower.jpg
├── video.mp4
└── README.md

````

---

# ⚙️ Teknologi yang Digunakan

- **Python**
- **VsCode**
- **OpenCV (cv2)**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

---

# 📷 Fitur yang Dipelajari

## 1️⃣ Membaca dan Menampilkan Gambar

```python
import cv2

img = cv2.imread("sunflower.jpg")
cv2.imshow("Image", img)
cv2.waitKey(0)
cv2.destroyAllWindows()
````

Fungsi ini digunakan untuk membaca dan menampilkan gambar menggunakan OpenCV.

---

# 🎨 Image Color Conversion

OpenCV menggunakan format warna **BGR**, sedangkan library lain seperti Matplotlib menggunakan **RGB**.

Contoh konversi warna:

```python
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

Jenis konversi yang digunakan:

* BGR → Grayscale
* BGR → RGB
* BGR → BGRA

---

# 🎥 Video Processing

Program juga membaca video dan mengubah setiap frame menjadi grayscale.

```python
cap = cv2.VideoCapture('video.mp4')

while cap.isOpened():
    ret, frame = cap.read()
```

Frame video diproses satu per satu menggunakan loop.

---

# ✏️ Drawing Tools

OpenCV dapat digunakan untuk menggambar berbagai objek pada gambar.

### Line

```python
cv2.line(img, (100,100), (300,300), (0,255,0), 3)
```

### Rectangle

```python
cv2.rectangle(img, (50,50), (200,200), (255,0,0), 2)
```

### Circle

```python
cv2.circle(img, (150,150), 50, (0,255,255), 2)
```

---

# 🖱️ Mouse Interaction

Project ini juga membuat **program interaktif menggunakan mouse** untuk:

* menggambar garis
* menggambar rectangle
* menggambar lingkaran
* melakukan crop gambar

OpenCV menggunakan fungsi:

```python
cv2.setMouseCallback()
```

untuk membaca event mouse.

---

# ✂️ Image Cropping

Gambar dapat dipotong menggunakan koordinat rectangle.

```python
img_crop = img[y1:y2, x1:x2]
```

Hasil crop kemudian disimpan menggunakan:

```python
cv2.imwrite("image.jpg", img_crop)
```

---

# 📦 Bounding Box & Label

Bounding box digunakan untuk menandai objek pada gambar.

Contoh:

```python
cv2.rectangle(img, (50,50), (300,300), (255,127,0), 2)
```

Label objek juga dapat ditambahkan menggunakan:

```python
cv2.putText()
```

Teknik ini sering digunakan pada **Object Detection dalam Computer Vision**.

---

# 🧪 Cara Menjalankan Project

1️⃣ Clone repository ini

```bash
git clone https://github.com/Alfadrian25/Tugas_Kelompok_3_ML.git
```

2️⃣ Masuk ke folder project

```bash
cd Tugas_Kelompok_3_ML
```

3️⃣ Install library yang dibutuhkan

```bash
pip install opencv-python numpy matplotlib
```

4️⃣ Jalankan notebook

```bash
jupyter notebook
```

---

# 🎥 Video Presentasi

Link video presentasi dapat dilihat di:

# https://youtu.be/q5YJyNpMsnw?si=Oe3jfZR5SSMsmevx

---

# 📚 Referensi

* OpenCV Documentation
  [https://opencv.org](https://opencv.org)

* #3 Facerecogition - OpenCV | Image Color Conversion & Drawing Tool https://youtu.be/AI56o4lJETM?si=5-D1vRFGjZ5BPEVS

---

# ⭐ Kesimpulan

Dari praktik ini dapat dipahami bahwa **OpenCV merupakan library yang sangat powerful untuk Computer Vision**, terutama dalam:

* pengolahan gambar
* pemrosesan video
* manipulasi pixel
* serta pembuatan sistem berbasis AI seperti Object Detection.
