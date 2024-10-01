# Chapter 2: Reverse Engineering

## Apa Itu Reverse Engineering?

Reverse engineering adalah proses membongkar dan menganalisis bagaimana sebuah sistem atau software bekerja dengan membalik proses pembuatan atau desain aslinya. Dalam konteks keamanan siber, reverse engineering digunakan untuk menganalisis malware, menemukan kelemahan software, dan memahami bagaimana aplikasi tertentu bekerja.

## Tujuan Reverse Engineering:
1. **Analisis Malware**: Menemukan cara kerja malware dan potensi ancaman yang ditimbulkannya.
2. **Pencarian Vulnerability**: Mengidentifikasi bug atau celah keamanan dalam perangkat lunak.
3. **Interoperability**: Memahami cara kerja sistem sehingga dapat diintegrasikan dengan sistem lain.

## Tools Populer untuk Reverse Engineering

- **IDA Pro**: Disassembler yang banyak digunakan untuk menganalisis executable dan mengonversinya menjadi kode assembly.
- **Ghidra**: Software reverse engineering gratis yang dikembangkan oleh NSA, yang menyediakan fitur analisis program mirip dengan IDA Pro.
- **Radare2**: Framework reverse engineering open-source yang sangat kuat.

## Contoh Dasar: Analisis Binary

Untuk memulai reverse engineering, kita bisa memanfaatkan tools disassembler seperti Ghidra atau IDA Pro untuk membuka file executable (.exe atau .elf) dan melihat kode assembly di balik program tersebut.

Misalnya, ketika kita membuka sebuah program dengan Ghidra, kita akan melihat output seperti ini:

```assembly
main: PUSH RBP MOV RBP, RSP MOV RAX, QWORD PTR FS:[0x28] MOV QWORD PTR [RBP+var_8], RAX XOR EAX, EAXs
```

Kode ini adalah representasi assembly dari instruksi program. Reverse engineering bertujuan untuk mengonversi dan memahami apa yang dilakukan kode ini pada level tinggi.