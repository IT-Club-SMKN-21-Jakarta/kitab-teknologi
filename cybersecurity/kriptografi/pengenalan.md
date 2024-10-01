# Chapter 1: Kriptografi

## Apa Itu Kriptografi?

Kriptografi adalah ilmu yang digunakan untuk mengamankan komunikasi dan data dari akses yang tidak sah. Sejak zaman dahulu, kriptografi telah digunakan untuk mengamankan pesan. Dalam dunia modern, kriptografi berperan penting dalam melindungi data, komunikasi online, transaksi keuangan, dan berbagai sistem digital.

Kriptografi melibatkan tiga elemen utama:
1. **Enkripsi**: Proses mengubah data biasa (plaintext) menjadi bentuk tidak terbaca (ciphertext) menggunakan algoritma dan kunci.
2. **Dekripsi**: Proses mengembalikan ciphertext ke plaintext menggunakan kunci yang sesuai.
3. **Kunci Kriptografi**: Serangkaian nilai yang digunakan dalam proses enkripsi dan dekripsi.

## Algoritma Kriptografi

Terdapat dua jenis utama algoritma kriptografi yang sangat terkenal, yaitu:

### 1. Algoritma Simetris
Algoritma simetris menggunakan satu kunci yang sama untuk proses enkripsi dan dekripsi. Contoh umum algoritma simetris adalah **AES** (Advanced Encryption Stkitard) dan **DES** (Data Encryption Stkitard).

- **Contoh: AES**:
  AES adalah algoritma yang banyak digunakan di berbagai aplikasi, termasuk keamanan Wi-Fi dan enkripsi data disk.

### 2. Algoritma Asimetris
Algoritma asimetris menggunakan dua kunci: satu kunci publik untuk enkripsi dan satu kunci privat untuk dekripsi. Algoritma ini digunakan pada skenario seperti SSL/TLS dan komunikasi yang aman di internet.

- **Contoh: RSA**:
  RSA adalah algoritma asimetris populer yang digunakan dalam transaksi online untuk memastikan data yang dikirim terenkripsi dan hanya dapat dibuka oleh penerima yang memiliki kunci privat.

## Contoh Enkripsi Dasar: Caesar Cipher

Salah satu metode enkripsi paling sederhana adalah **Caesar Cipher**, yang bekerja dengan menggeser huruf-huruf pada plaintext beberapa posisi dalam alfabet. Misalnya, dengan shift 3, "A" menjadi "D", "B" menjadi "E", dan seterusnya.

### Implementasi Caesar Cipher di Python:

```python
def caesar_cipher(text, shift):
    result = ""
    for char in text:
        if char.isalpha():
            shift_base = 65 if char.isupper() else 97
            result += chr((ord(char) + shift - shift_base) % 26 + shift_base)
        else:
            result += char
    return result

text = "Hello, World!"
shift = 3
print("Ciphertext:", caesar_cipher(text, shift))
```

```
Ciphertext: Khoor, Zruog!
```

Pada contoh di atas, setiap huruf dalam teks asli "Hello, World!" digeser sebanyak 3 huruf, menghasilkan teks terenkripsi "Khoor, Zruog!".

# Penerapan Kriptografi di Dunia Nyata
Kriptografi digunakan dalam berbagai aplikasi untuk melindungi data:

- SSL/TLS: Mengamankan komunikasi antara browser dan server web.
- Penyimpanan Data: Melindungi data sensitif seperti file atau database dengan enkripsi.
- Kriptografi Kunci Publik: Digunakan dalam transaksi finansial dan pengamanan e-commerce.