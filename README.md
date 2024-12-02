# praktikum6-2
# Nama : keysia nurhayati br panjaitan
# NIM : 312410350
# Kelas : TI.24.A4
# Mata kuliah : Bahasa Pemograman
# Latihan 1
![WhatsApp Image 2024-12-02 at 22 44 46_ce4879aa](https://github.com/user-attachments/assets/3a144b94-761a-4c99-9fc1-2878aa8f5aa1)
latihan 1.py
import math

a = lambda x: x**2
b = lambda x, y: math.sqrt(x*2 + y*2)
c = lambda *args: sum(args)/len(args) if args else 0
d = lambda s: "".join(set(s)) 

print("lambda a(5):", a(5))
print("lambda b(3, 4):", b(3, 4))
print("lambda c(1, 2, 3, 4, 5):", c(1, 2, 3, 4, 5))
print("lambda d('hello sovy'):", d("sovy"))


