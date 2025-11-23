### Implementasi Linked List Sederhana dengan Python

Linked List adalah struktur data yang menyimpan kumpulan elemen secara berurutan, namun cara penyimpanannya tidak harus bersebelahan dalam memori seperti array. Struktur ini terdiri dari beberapa node, dan setiap node memiliki dua informasi utama:
1. Data yang ingin disimpan
2. Pointer atau penunjuk yang mengarah ke node berikutnya

Karena setiap node terhubung melalui pointer, bentuk Linked List dapat dianalogikan sebagai rantai yang tersusun dari banyak mata rantai. Struktur seperti ini membuat proses menambah atau menghapus data menjadi lebih fleksibel, karena cukup mengubah sambungan antarnode tanpa perlu menggeser elemen lainnya.

Kode ini mengimplementasikan struktur data **Linked List** secara manual menggunakan bahasa Python. Linked List terdiri dari dua kelas utama, yaitu:

* **Node** → menyimpan data dan pointer ke node berikutnya
* **LinkedList** → menyediakan berbagai operasi untuk memanipulasi list

Di bawah ini adalah penjelasan setiap fungsinya.

---

##  class Node

```python
class Node:
    def __init__(self, data=None, pointer=None):
        self.data = data
        self.next = pointer
```

**Penjelasan:**
Node digunakan sebagai elemen penyusun Linked List.
Setiap node menyimpan:

* **data** → nilai yang ingin disimpan
* **next** → alamat node berikutnya

---

##  class LinkedList

### 1. ****init**(self)**

```python
def __init__(self):
    self.head = None
```

Mengatur linked list dalam keadaan kosong dengan `head = None`.

---

## 2. **insert_at_first(self, data)**

```python
def insert_at_first(self, data):
    node = Node(data, self.head)
    self.head = node
```

Menambahkan node baru di **bagian depan** Linked List.

Cara kerjanya:

* Node baru dibuat dengan pointer menuju head lama
* Head diganti menjadi node baru

---

## 3. **insert_at_last(self, data)**

```python
def insert_at_last(self, data):
    if self.head is None:
        self.head = Node(data)
    else:
        node_sekarang = self.head
        while node_sekarang.next :
            node_sekarang = node_sekarang.next
        node_sekarang.next = Node(data)
```

Menambahkan node di **bagian akhir** list.

Alurnya:

* Jika list kosong → langsung jadi head
* Jika tidak → cari node terakhir → sambungkan node baru di ujung

---

## 4. **insert_at_(self, index, data)**

```python
def insert_at_(self, index, data):
    ...
```

Menambahkan node di posisi tertentu.

Aturannya:

* Jika index < 0 atau lebih besar dari panjang list → invalid
* Jika index = 0 → sama seperti insert_at_first
* Selain itu → cari node pada posisi sebelum `index`, lalu selipkan node baru

---

## 5. **remove_first(self)**

```python
def remove_first(self):
    if self.head is None:
        print("tidak ada data yang bisa dihapus")
    else:
        self.head = self.head.next
```

Menghapus node **paling depan** (head).

* Jika kosong → tampilkan peringatan
* Jika tidak → head digeser ke node berikutnya

---

## 6. **remove_last(self)**

```python
def remove_last(self):
    ...
```

Menghapus node **paling akhir**.

Proses:

* Jika list kosong → tampilkan pesan
* Jika hanya 1 node → head dihapus
* Jika lebih → cari node sebelum terakhir, lalu putuskan koneksinya

---

## 7. **remove_at_(self, index)**

```python
def remove_at_(self, index):
    ...
```

Menghapus node pada posisi tertentu.

* Jika index tidak valid → tampilkan pesan
* Jika index = 0 → gunakan remove_first
* Jika lebih → lompat sampai node sebelum index, lalu putuskan node tersebut

---

## 8. **print(self)**

```python
def print(self):
    ...
```

Menampilkan seluruh data di Linked List.

Output dalam bentuk:

```
data1 -> data2 -> data3 ->
```

Jika kosong → menampilkan `"data kosong"`.

---

## 9. **length(self)**

```python
def length(self):
    ...
```

Menghitung jumlah total node dalam linked list.

Cara kerja:

* Mulai dari head
* Iterasi hingga node terakhir
* Tambahkan penghitung setiap langkah

---

##  Contoh penggunaan (driver code)

```python
LL = LinkedList()
LL.insert_at_first("jeruk")
LL.insert_at_first("mangga")
LL.insert_at_first("manggis")
LL.insert_at_last("apel")
LL.insert_at_(2, "anggur")

LL.remove_first()
LL.remove_last()
LL.remove_at_(2)

LL.print()
print(LL.length())
```

---

**Kesimpulan**

Implementasi Linked List ini menyediakan operasi dasar seperti **menambah**, **menghapus**, dan **menampilkan** node. Semua fungsi bekerja dengan prinsip dasar Linked List, yaitu menggunakan pointer `next` untuk menghubungkan setiap node. Dengan struktur seperti ini, Linked List menjadi fleksibel untuk manipulasi data tanpa harus menggeser elemen seperti pada array. Kode ini juga cocok sebagai contoh pembelajaran dasar struktur data dan dapat dikembangkan lebih lanjut sesuai kebutuhan.

---

