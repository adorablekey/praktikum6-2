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
# penjelasan code
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

Meminta pengguna untuk memasukkan nama mahasiswa. Jika nama kosong (hanya spasi), program akan mencetak pesan kesalahan dan keluar dari fungsi, menggunakan try-except untuk mencoba mengonversi nilai yang dimasukkan menjadi integer. Jika gagal, program mencetak pesan kesalahan, jika semua input valid, data mahasiswa (nama dan nilai) ditambahkan ke dalam dictionary daftar_mahasiswa, dan program mencetak pesan konfirmasi  dan Secara keseluruhan, kode ini bertujuan untuk memastikan bahwa data mahasiswa yang dimasukkan valid (nama tidak kosong, nilai berupa angka), dan jika valid, data akan disimpan dalam dictionary dan program akan mengonfirmasi keberhasilan penambahan data tersebut.

       def tampilkan():
          """Menampilkan semua data mahasiswa."""
    if not daftar_mahasiswa:
        print("Daftar mahasiswa kosong.")
    else:
        print("Daftar Mahasiswa:")
          for nama, nilai in daftar_mahasiswa.items():
            print(f"{nama}: {nilai}")
Fungsi tampilkan() yang Anda berikan berfungsi untuk menampilkan semua data mahasiswa yang ada dalam sebuah struktur data, yaitu daftar_mahasiswa

      def hapus(nama):
         """Menghapus data mahasiswa berdasarkan nama."""
    if nama in daftar_mahasiswa:
        del daftar_mahasiswa[nama]
        print(f"Data mahasiswa {nama} berhasil dihapus.")
    else:
        print(f"Data mahasiswa {nama} tidak ditemukan.")

Fungsi hapus(nama) ini memeriksa apakah nama yang diberikan ada dalam dictionary daftar_mahasiswa. Jika ada, fungsi menghapus data mahasiswa tersebut, dan jika tidak ada, fungsi akan memberitahukan bahwa data mahasiswa tersebut tidak ditemukan

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
        
Fungsi ubah(nama) yang Anda berikan berfungsi untuk mengubah nilai mahasiswa berdasarkan nama yang diberikan. Fungsi ini mencari nama mahasiswa dalam dictionary daftar_mahasiswa, dan jika nama tersebut ditemukan, pengguna diminta untuk memasukkan nilai baru. Berikut penjelasan rinci tentang bagian-bagian dari fungsi tersebut:

       daftar_mahasiswa = {}
       
adalah pernyataan untuk mendeklarasikan sebuah dictionary kosong di Python yang diberi nama daftar_mahasiswa. Dalam konteks program Anda, dictionary ini digunakan untuk menyimpan data mahasiswa, di mana nama mahasiswa menjadi kunci (key) dan nilai mahasiswa (misalnya nilai ujian atau IPK) menjadi nilai (value).

       if __name__ == "__main__":
    while True:

if __name__ == "__main__" memastikan bahwa kode di dalam blok ini hanya dijalankan jika file ini dieksekusi langsung, bukan ketika diimpor sebagai modul oleh program lain. while True loop tak terbatas yang akan terus berjalan sampai perintah break dijalankan.

        print("\nMenu:")
           print("1. Tambah data")
           print("2. Tampilkan data")
           print("3. Hapus data")
           print("4. Ubah data")
           print("5. Keluar")

Program mencetak menu dengan lima opsi yang dapat dipilih pengguna tersebut:

1. Tambah data: untuk menambahkan data mahasiswa baru
2. Tampilkan data: untuk menampilkan semua data mahasiswa yang telah dimasukkan
3. Hapus data: Menghapus data mahasiswa berdasarkan nama
4. Ubah data: Mengubah nilai mahasiswa berdasarkan nama
5. Keluar: Keluar dari program

          pilihan = input("Pilih menu (1-5): ")
   
 Program meminta input dari pengguna untuk memilih salah satu menu (1-5). 

          if pilihan == '1':
    tambah()
           elif pilihan == '2':
    tampilkan()

Jika pengguna memilih 1, maka fungsi akan tambah(), Jika pengguna memilih 2, maka fungsi akan tampilkan() untuk menampilkan semua data mahasiswa yang ada dalam daftar_mahasiswa

        elif pilihan == '3':
             nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
elif pilihan == '4':
    nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
          ubah(nama)
          
Jika pengguna memilih 3, program akan meminta input nama mahasiswa yang ingin dihapus, Jika pengguna memilih 4, program akan meminta input nama mahasiswa yang ingin diubah.


