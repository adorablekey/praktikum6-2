# praktikum6-2
# Nama : keysia nurhayati br panjaitan
# NIM : 312410350
# Kelas : TI.24.A4
# Mata kuliah : Bahasa Pemograman
# Latihan 1
![WhatsApp Image 2024-12-02 at 22 44 46_ce4879aa](https://github.com/user-attachments/assets/3a144b94-761a-4c99-9fc1-2878aa8f5aa1)
# latihan 1.py

      import math

       a = lambda x: x**2
       b = lambda x, y: math.sqrt(x*2 + y*2)
       c = lambda *args: sum(args)/len(args) if args else 0
       d = lambda s: "".join(set(s)) 

       print("lambda a(5):", a(5))
       print("lambda b(3, 4):", b(3, 4))
       print("lambda c(1, 2, 3, 4, 5):", c(1, 2, 3, 4, 5))
       print("lambda d('hello keysia'):", d("keysia"))
# code program
![Screenshot 2024-12-02 224253](https://github.com/user-attachments/assets/e92b1c91-8f0e-48b9-af5c-ac4b57ec5d1b)
# hasil program
![Screenshot 2024-12-02 231129](https://github.com/user-attachments/assets/833aaa67-d1a8-4f0d-9ecf-7406fdfbeb3d)
# tugas praktikum
![image](https://github.com/user-attachments/assets/ee751d3c-83df-4f0a-a2bc-67adc58f8cb9)
# tugas praktikum.py

       def tambah():
        """Menambahkan data mahasiswa baru ke dalam daftar."""
        nama = input("Masukkan nama mahasiswa: ")
       if not nama.strip():
        print("Nama tidak boleh kosong.")
        return
    try:
        nilai = int(input("Masukkan nilai mahasiswa: "))
    except ValueError:
        print("Nilai harus berupa angka.")
        return
    daftar_mahasiswa[nama] = nilai
    print("Data mahasiswa berhasil ditambahkan.")

      def tampilkan():
          """Menampilkan semua data mahasiswa."""
        if not daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
    else:
        print("Daftar Mahasiswa:")
        for nama, nilai in daftar_mahasiswa.items():
            print(f"{nama}: {nilai}")

def hapus(nama):
    """Menghapus data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        del daftar_mahasiswa[nama]
        print(f"Data mahasiswa {nama} berhasil dihapus.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")

def ubah(nama):
    """Mengubah data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        try:
            nilai_baru = int(input(f"Masukkan nilai baru untuk {nama}: "))
            daftar_mahasiswa[nama] = nilai_baru
            print(f"Data mahasiswa {nama} berhasil diubah.")
        except ValueError:
            print("Nilai harus berupa angka.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")

daftar_mahasiswa = {}

if __name__ == "__main__":
    while True:
        print("\nMenu:")
        print("1. Tambah data")
        print("2. Tampilkan data")
        print("3. Hapus data")
        print("4. Ubah data")
        print("5. Keluar")

        pilihan = input("Pilih menu (1-5): ")

        if pilihan == '1':
            tambah()
        elif pilihan == '2':
            tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            ubah(nama)
        elif pilihan == '5':
            print("Terima kasih!")
            break
        else:
            print("Pilihan tidak valid.")






