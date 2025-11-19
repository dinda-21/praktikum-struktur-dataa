### **Implementasi Queue di Python**
---

**Apa itu Queue?**
Queue itu struktur data yang cara kerjanya mirip antrean. Yang masuk duluan bakal keluar duluan juga. Jadi urutannya rapi, dari depan ke belakang. Konsep utamanya: **FIFO — First In First Out.**

### **Penjelasan Coding**

**1. Bikin tempat antrian**

```python
queue = []
```
List kosong disiapkan buat naro data antrian.


---

**2. Enqueue (masukin data ke belakang)**

```python
queue.append('A')
queue.append('B')
queue.append('C')
print("Queue: ", queue)
```

`append()` kaya orang baru masuk antrean. Jadi isi antreannya jadi `['A', 'B', 'C']`.


---

**3. Dequeue (ngeluarin data yang paling depan)**

```python
element = queue.pop(0)
print("Dequeue: ", element)
```

`pop(0)` ngambil elemen yang paling depan yang pertama datang, dialah yang keluar duluan. Yang keambil: `'A'`.



---
**4. Peek (ngintip siapa yang paling depan)**

```python
frontElement = queue[0]
print("Peek: ", frontElement)
```

Kita cuma lihat elemen terdepan tanpa ngapus. Hasilnya `'B'`.



---
**5. Cek antrian kosong atau nggak**

```python
isEmpty = not bool(queue)
print("isEmpty: ", isEmpty)
```

Kalau masih ada isi, hasilnya tentu **False**.



---
**6. Ngitung berapa isi antrian**

```python
print("Size: ", len(queue))
```

Karena udah ngeluarin satu, sisanya tinggal 2 elemen.



---
**Output Program**

```
Queue:  ['A', 'B', 'C']
Dequeue:  A
Peek:  B
isEmpty:  False
Size:  2
```



---
### **Kesimpulan**

1. Queue bekerja dengan prinsip **FIFO (First In First Out)**: data yang masuk duluan akan keluar duluan.
2. Operasi **enqueue** menambahkan elemen ke bagian belakang antrian.
3. Operasi **dequeue** menghapus elemen dari bagian depan antrian.
4. Pengecekan kondisi queue dilakukan dengan melihat apakah list kosong atau tidak.
5. Ukuran queue dapat diketahui menggunakan fungsi len().
6. Program menunjukkan bagaimana queue memproses data secara teratur, dari depan ke belakang.



---

### **Implementasi Stack di Python**
Stack itu gampangnya kayak **tumpukan barang**. Contoh paling simpel: tumpukan buku di atas meja.
Buku yang kita taruh paling atas, ya itu juga yang bakal kita ambil duluan.
Nah, di pemrograman stack juga kerja dengan cara yang sama: yang masuk terakhir, keluar duluan, **Last In, First Out (LIFO).**

---

### **Penjelasan Coding**

**1. Bikin Stack Kosong**

```python
stack = []
```

Ini cuma bikin tempat kosong buat naro data, bentuknya list.

---

**2. Masukin Data (Push)**

```python
stack.append('A')
stack.append('B')
stack.append('C')
print("Stack: ", stack)
```

`append` itu kayak bilang *"tambahin ke atas tumpukan"*.

Urutan masuk:

* A
* B
* C
  Jadi isi stack nya : `['A', 'B', 'C']`.

---

**3. Ngambil Data Teratas (Pop)**

```python
element = stack.pop()
print("Pop: ", element)
```

`pop()` itu ngambil data paling atas.
Karena yang paling atas C, ya yang keluar C.

---

**4. Liat Data Teratas Tanpa Ngapus (Peek)**

```python
topElement = stack[-1]
print("Peek: ", topElement)
```

Ini cuma ngecek “atasnya sekarang apa?”, tanpa ngilangin.
Karena C udah di-pop, yang paling atas sekarang B.

---

**5. Cek Stack Kosong atau Nggak**

```python
isEmpty = not bool(stack)
print("isEmpty: ", isEmpty)
```

> Kalau stack masih ada isinya → False.
> Kalau kosong → True.
Karena masih ada A dan B, hasilnya **False** (alias belum kosong).

---

**6. Cek Jumlah Isi Stack**

```python
print("Size :", len(stack))
```

`len()` buat tau ada berapa data di stack.
Hasilnya: **2**.

---

**Output yang Keluar**

```
Stack:  ['A', 'B', 'C']
Pop:  C
Peek:  B
isEmpty:  False
Size :  2
```

---

## **Kesimpulan**

1. Stack bekerja dengan konsep **LIFO (Last In, First Out)**.
2. Elemen yang terakhir dimasukkan akan menjadi yang pertama diambil.
3. Operasi **push** digunakan untuk menambah data ke bagian atas stack.
4. Operasi **pop** digunakan untuk mengambil dan menghapus data teratas.
5. Operasi **peek** dipakai untuk melihat data teratas tanpa menghapusnya.
6. Stack bisa dicek apakah kosong menggunakan pengecekan **boolean (isEmpty)**.
7. Jumlah elemen di dalam stack dapat diketahui menggunakan **len()**.
8. Stack mudah dibuat di Python menggunakan list, dengan .append() dan .pop() sebagai fungsi utamanya.

---
