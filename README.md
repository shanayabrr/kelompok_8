#soal nomor 3.buatlah program untuk fungsi menghitung perkalian matrix 
## Perkalian Matriks 4x4
matriksA = [ 
    [10, 55, 54, 10], 
    [23, 5, 23, 14],
    [21, 7, 13, 11],
    [11, 88, 14, 15], 
]

matriksB = [
    [3, 0, 0, 1],
    [3, 1, 0, 3],
    [3, 0, 1, 3],
    [1, 0, 0, 3]
]
# Perkalian matriks
hasil = [[sum(matriksA[i][k] * matriksB[k][j] for k in range(4)) for j in range(4)] for i in range(4)]

# Menampilkan hasil perkalian
print("Hasil perkalian matriks:")
for baris in hasil:
    print(baris)

# Soal nomor 2. Buatlah fungsi untuk mengambil irisan dan beda setangkup dari dua himpunan ini
# Definisi himpunan A dan B
A = {33, 47, 50, 18, 22, 3, 23, 14, 3, 19}
B = {23, 12, 56, 21, 21, 33, 51,15, 6, 4, 21}

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

# Soal bagian 3, nomor 1. Buat fungsi untuk mengurutkan himpunan A dengan menggunakan buble sort
def bubble_sort(A):
    # Mengubah himpunan menjadi list agar bisa diurutkan
    A = list(A)

    n = len(A)
    for i in range(n):
        # Flag untuk mengecek jika ada perubahan dalam iterasi ini
        swapped = False
        
        # Loop untuk perbandingan elemen yang bersebelahan
        for j in range(0, n-i-1):
            # Jika elemen lebih besar dari elemen berikutnya, tukar
            if A[j] > A[j+1]:
                A[j], A[j+1] = A[j+1], A[j]
                swapped = True
        
        # Jika tidak ada yang ditukar, berarti sudah terurut
        if not swapped:
            break
    
    return A
# Himpunan A
A = {109, 222, 120, 150, 200, 321, 410, 120, 230, 300, 111, 89, 70, 45, 57, 31, 39, 900, 21, 378, 400, 101, 201, 301, 1}

# Mengurutkan himpunan A menggunakan Bubble Sort
sorted_A = bubble_sort(A)
print(sorted_A)





# Soal bagian 3, nomor 2. Buat fungsi untuk melakukan pencarian nilai x pada himpunan A. misalkan mencari x = 300, ada di posisi index ke i
def cari_nilai(A, x):
    # Melakukan pencarian linear
    for i in range(len(A)):
        if A[i] == x:
            # Kembalikan indeks jika ditemukan
            return i
    # Kembalikan -1 jika x tidak ditemukan
 return -1

# Contoh penggunaan
A = [109, 222, 120, 150, 200, 321, 410, 120, 230, 300, 111, 89, 70, 45, 57, 31, 39, 900, 21, 378, 400, 101, 201, 301, 1]
x = 300
index = cari_nilai(A, x)

if index != -1:
    print(f"Nilai {x} ditemukan di posisi index ke-{index}.")
else:
    print(f"Nilai {x} tidak ditemukan.")
