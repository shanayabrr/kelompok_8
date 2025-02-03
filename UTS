#bagian 1 soal no 5
# Matriks A
A = [
    [11, 80, 21, 10],
    [23, 5, 12, 14],
    [21, 7, 21, 14],
    [13, 44, 32, 15]
]

# Matriks B
B = [
    [1, 0, 0, 1],
    [0, 1, 0, 0],
    [5, 0, 1, 5],
    [1, 0, 0, 1]
]

# Inisialisasi matriks hasil
result = [[0 for _ in range(4)] for _ in range(4)]

# Perkalian matriks secara manual
for i in range(4):  # Baris matriks A
    for j in range(4):  # Kolom matriks B
        for k in range(4):  # Elemen untuk dikalikan
            result[i][j] += A[i][k] * B[k][j]

# Output hasil
print("Hasil perkalian matriks A x B:")
for row in result:
    print(row)

#bagian 2 soal no 5
# Definisi himpunan
A = {3, 4, 5, 17, 2, 3, 5, 14, 3 , 10, 31, 22, 21, 45}
B = {4, 21, 5, 17, 2, 3, 6, 15, 6, 45, 20}

# Fungsi untuk irisan
def irisan(set_A, set_B):
    return set_A.intersection(set_B)

# Fungsi untuk beda setangkup
def beda_setangkup(set_A, set_B):
    return set_A.symmetric_difference(set_B)

# Fungsi peluang
def peluang(himpunan, semesta):
    return len(himpunan) / len(semesta)

# Menghitung irisan dan beda setangkup
irisan_himpunan = irisan(A, B)
beda_setangkup_himpunan = beda_setangkup(A, B)

# Menghitung peluang P(A) dan P(B)
semesta = A.union(B)  # Gabungan himpunan sebagai semesta
peluang_A = peluang(A, semesta)
peluang_B = peluang(B, semesta)

# Output hasil
print("Irisan (A ∩ B):", irisan_himpunan)
print("Beda setangkup (A Δ B):", beda_setangkup_himpunan)
print("Peluang P(A):", peluang_A)
print("Peluang P(B):", peluang_B)

#bagian 3
# Fungsi untuk bubble sort
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        # Loop untuk membandingkan elemen
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                # Tukar elemen jika tidak urut
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
    return arr

# Fungsi untuk mencari nilai x dengan sequential search
def search_value(arr, x):
    for i in range(len(arr)):
        if arr[i] == x:
            return i  # Mengembalikan posisi index jika ditemukan
    return -1  # Mengembalikan -1 jika tidak ditemukan

# Himpunan A
A = [109, 222, 120, 150, 200, 321, 410, 120, 230, 300, 111, 89, 70, 45, 57, 
     31, 39, 900, 21, 378, 400, 101, 201, 301, 1]

# Soal 1: Mengurutkan himpunan A
print("Himpunan A sebelum diurutkan:")
print(A)

A_sorted = bubble_sort(A.copy())
print("\nHimpunan A setelah diurutkan (Bubble Sort):")
print(A_sorted)

# Soal 2: Mencari nilai x dalam himpunan A
x = 300  # Contoh nilai yang dicari
posisi = search_value(A_sorted, x)

if posisi != -1:
    print(f"\nNilai {x} ditemukan di posisi index ke-{posisi} (setelah diurutkan).")
else:
    print(f"\nNilai {x} tidak ditemukan dalam himpunan A.")
