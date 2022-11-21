# Praktikum5

# LATIHAN MEMBUAT LIST

# Membuat list sebanyak 5 element dengan nilai bebas

Repository ini di buat untuk memenuhi tugas Bahasa Pemrograman Pertemuan-9

Nama : Raudah Musrifa

NIM : 312210020

Matkul : Bahasa Pemrograman

Kelas : TI.22.B1

1. Buatlah Folder Praktikum5 dan didalamnya diisi File List.py & Praktikum5.py seperti berikut :

![prak5 1](https://user-images.githubusercontent.com/115474431/202962570-d2be830f-fa73-42c9-8a4d-eb7205ff9582.PNG)

2. Buka file List.py lalu masukan code dibawah ini :

        # membuat 5 list dengan type data yang berbeda

        listData = ["Teknik Informatika", "UPB", 450000, True, "Fakultas Teknik"]

        ##########################
        # mengakses element list #
        ########################

        # menampilkan element ke-3 pada sebuah list
        print(listData[2])

        # menampilkan element ke-2 sampai ke-4
        print(listData[1:4])

        # menampilkan element terakhir
        print(listData[4])
        # atau bisa juga seperti ini
        print(listData[-1])

        ##########################
        # Mengubah element list #
        ########################

        # Mengubah element ke-4 dengan nilai lain
        listData[3] = False
        print(listData)

        # Mengubah element ke-4 sampai dengan terakhir dengan nilai lain
        listData[3:5] = [True, "TI22B1"]
        print(listData)

        #############################
        # Menambahkan element list #
        ###########################

        # membuat list A dan diisi oleh element yang ada di listData
        listA = listData

        # membuat list B dengan element masih kosong
        listB = [] 

        # mengambil 2 nilai dari listA lalu simpan ke listB
        listB = list[0:2]
        print(listB)

        # Menambahakan list B dengan nilai string
        listB.append("Fakultas Teknik")
        print(listB)

        # Menambahakan list B dengan 3 nilai
        listB.extend(["Teknik Sipil", "Teknik Industri", "Teknik lingkungan"])
        print(listB)

        # Menggabungkan list B dengan list A
        listGabungan = listA + listB
        print(listGabungan)
        
3. Jalankan file maka akan muncul hasilnya sebagai berikut :

![prak5 2](https://user-images.githubusercontent.com/115474431/202963089-1319fafe-7440-485f-a6d3-31173e5404a0.PNG)

# Membuat program untuk menambahkan data mahasiswa beserta nilainya kedalam sebuah list

1. Buka file Praktikum5.py kemudian masukan code berikut :

        # import package tabulate
        from tabulate import tabulate

        # membuat list kosong untuk menampung data
        dataMahasiswa = []
        no = 0
        # melakukan perulangan input sesuai keinginan sampai pertanyaan tambah data dimunculkan kembali
        while(True):
            # membuat variable untuk menampung inputan
            no += 1
            nama = input("Masukan Nama : ")
            nim = input("Masukan NIM : ")
            kelas = input("Masukan Kelas : ")
            matkul = input("Masukan Mata Kuliah : ")

            # mengkonversi string ke integer
            tugas = int(input("Masukan Nilai Tugas : "))
            uts = int(input("Masukan Nilai UTS : "))
            uas = int(input("Masukan Nilai UAS : "))

            # menjumlahkan nilai dari tugas,uts dan uas
            nilai_akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)

            # lakukan pengecekan jika nilai_akhir lebih besar dari 50 maka Lulus selain itu tidak lulus dan mengulang mata kuliah
            if (nilai_akhir > 50):
                keterangan = "Lulus"
            else:
                keterangan = "Tidak Lulus, Mengulang Mata kuliah"
            # menambahkan data input ke list dataMahasiswa
            dataMahasiswa.append(
                [no, nama, nim, kelas, matkul, tugas, uts, uas, nilai_akhir, keterangan])

            # input tambah data jika tekan y maka input kembali, selain itu berhenti dan tampilkan data
            tambah_data_lagi = input("Tambah Data lagi ? (y/t) : ")
            if(tambah_data_lagi == "t"):
                break

            # tampilkan dataMahasiswa menggunakan tabulate package agar tampilan berbentuk table
            print(tabulate(dataMahasiswa, headers=[
                "No", "Nama", "Nim", "Kelas", "Mata Kuliah", "Tugas", "UTS", "UAS", "Nilai Akhir", "Keterangan"], tablefmt="fancy_grid"))
                
2. Jalankan file maka akan muncul hasilnya sebagai berikut :

![prak5 3](https://user-images.githubusercontent.com/115474431/202964398-315b298d-167d-467e-9409-f0e66e1a93f2.PNG)

Perlu diketahui sebelum menjalankan file pastikan sudah menginstall pip, pip bisa di instal di command pro dengan cara ketik pip install tabulate

Flowchart program di atas sebagai berikut :

![flowchart adam5](https://user-images.githubusercontent.com/115474431/202964842-b2160fb6-383c-4afe-8795-41adebd53dd2.png)

Selesai

Terima Kasih








