# 🐼 Learn Pandas in 1 hour! (Python Pandas Tutorial)<br>[Learn Pandas From Channel Bro Code](https://youtu.be/VXtjG_GzO7Q?utm_source=chatgpt.com)

---

## 🧠 1. Apa itu Pandas dan Kenapa Penting?

📍 Pandas adalah library Python yang digunakan untuk mengolah dan menganalisis data secara efisien.

- Struktur data utama: Series dan DataFrame.

- Sangat penting untuk data science, machine learning, statistik, dan analisis data.

👉 **Series** = satu kolom data (mirip list/array satu dimensi).
👉 **DataFrame** = tabel data dua dimensi, mirip spreadsheet.

---

## 📥 2. Instalasi & Setup

**2.1 Contoh perintah di terminal:**

```bash
pip install pandas
```

**2.2 Lalu di python:**

```python
import pandas as pd
```

---

## 🧩 3. Membaca / Mengimpor Data

**3.1 Contoh file CSV atau Excel:**

```python
df = pd.read_csv("data.csv")
df_excel = pd.read_excel("data.xlsx")
```

📌 Ini adalah langkah paling awal dalam workflow analisis data: membaca dataset.

---

## 🔍 4. Eksplorasi Data (EDA Basic)

### 📌 Menampilkan kolom dan ukuran data

```python
df.head()       # lihat 5 baris pertama
df.tail()       # lihat baris terakhir
df.shape        # ukuran (baris, kolom)
df.columns      # daftar nama kolom
```

---

## 📊 5. Seleksi dan Filtering Kolom / Baris

**🔹 Filter dengan kondisi:**

```python
df_filtered = df[df["Age"] > 30]
```

**🔹 Seleksi kolom tertentu:**

```python
df_names = df[["Name", "Salary"]]
```

📌 Intinya: Pandas memungkinkan kita memilih subset data berdasarkan kondisi logis.

---

## 🛠 6. Operasi Dasar pada DataFrame

**✨ Mengurutkan Data**

```python
df.sort_values("Salary", ascending=False)
```

**✨ Mengisi nilai hilang**

```python
df.fillna(0)
```

**✨ Menghapus nilai hilang**

```python
df.dropna()
```

📍 Kamu belajar bagaimana membersihkan dataset sebelum analisis lebih lanjut.

---

## 📈 7. Agregasi & Grouping Data

### Contoh: Total gaji berdasarkan jabatan

```python
df.groupby("Job")["Salary"].sum()
```

👉 Ini sangat berguna untuk menganalisis statistik per kelompok (statistik deskriptif).

---

## 🧮 8. Operasi Statistik Dasar

```python
df.mean()       # rata-rata
df.median()     # median
df.describe()   # ringkasan statistik (count, mean, std, dll.)
```

📌 describe() sering dipakai untuk cepat mengetahui gambaran umum dataset.

---

## 🧾 9. Menyimpan / Mengekspor Data

```python
df.to_csv("hasil.csv")
df.to_excel("hasil.xlsx")
```

📌 Ini penting ketika kamu sudah selesai membersihkan atau memproses data dan ingin menyimpannya.

---

## 💡 10. Tips Praktis dari Video

**Berdasar struktur tutorial Pandas yang umum:** [`YouTube`](https://www.youtube.com/watch%3Fv%3DVXtjG_GzO7Q?utm_source=chatgpt.com)

✅ Mulai selalu dengan `import pandas as pd`.<br>
✅ Pahami perbedaan Series vs DataFrame.<br>
✅ Lakukan eksplorasi awal data (`head()`, `shape`).<br>
✅ Gunakan operasi seleksi/filter sebelum analisis kompleks.<br>
✅ Coba groupby dan agregasi untuk insight cepat.

## 🧪 Contoh Implementasi Praktik Pandas (Ringkas)

**Misalkan kamu punya file `employees.csv`:**

```csv
Name,Age,Job,Salary
Alice,30,Engineer,70000
Bob,25,Designer,65000
Charlie,35,Engineer,80000
```

**👉 Contoh read, filter, dan group:**

```python
import pandas as pd

# Load data
df = pd.read_csv("employees.csv")

# EDA dasar
print(df.head())
print(df.describe())

# Filter: usia > 30
older_than_30 = df[df["Age"] > 30]
print(older_than_30)

# Group by pekerjaan → rata-rata gaji
avg_salary_by_job = df.groupby("Job")["Salary"].mean()
print(avg_salary_by_job)
```
