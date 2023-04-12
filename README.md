# Basis Data
# tugas basis data
### 1.Membuat data base latihan2
```
CRATE DATABASE Latihan2
```
![image](https://user-images.githubusercontent.com/115862112/230727331-95d36346-69e2-428c-a44b-dab6c34cdc07.png)
### menampilkan daftar basisdata
![image](https://user-images.githubusercontent.com/115862112/230727398-d6243cb4-380a-44f6-9e2b-eee022dad27e.png)

### 2.Membuat tabel biodata di dalam database latihan2
```
USE latihan2; CREATE TABLE biodata (nama VARCHAR(15),alamat VARCHAR(15));
```
![image](https://user-images.githubusercontent.com/115862112/230727493-b303606c-5588-4cc7-b623-8b1479dec6be.png)
### 3.Menambahkan kolom keterangan
```
 ALTER TABLE biodata ADD keterangan VARCHAR(15);
```
![229923774-aafc34d6-1d18-4739-ab69-d0216d5387ee](https://user-images.githubusercontent.com/115862112/230727709-cc161916-45d5-4c2f-8d06-735e6b7f600f.png)


### 4.Menambahkan kolom id di awal:
```
ALTER TABLE biodata ADD id INT(11) FIRST;
```
![229924635-f622f0ac-7525-4aa3-9d5e-c40585641669](https://user-images.githubusercontent.com/115862112/230727783-493d870c-b6f2-4f58-b23b-fa0a2607d7a8.png)
### 5.Menambahkan kolom phone setelah kolom alamat:
```
 ALTER TABLE biodata ADD phone VARCHAR(15) AFTER alamat;
```
![229924689-57741e36-0215-4408-a0d3-e3a5429f353b](https://user-images.githubusercontent.com/115862112/230727875-b41bcea8-43d3-4f7e-9247-8ef87932a978.png)
### 6.Mengubah tipe data kolom id menjadi char(11):
```
ALTER TABLE biodata MODIFY id CHAR(11);
```
![image](https://user-images.githubusercontent.com/115862112/230728053-0136d156-72fa-4b20-b87f-a81659be8290.png)
### 7.Mengubah nama kolom phone menjadi hp (varchar 20):
```
 ALTER TABLE biodata CHANGE phone hp VARCHAR(20);
```
![image](https://user-images.githubusercontent.com/115862112/230728096-20526d0e-002c-4fba-963a-240dcd2b9541.png)
### 8.Menambahkan kolom email setelah kolom hp:
```
ALTER TABLE biodata ADD email VARCHAR(15) AFTER hp;
```
![image](https://user-images.githubusercontent.com/115862112/230728163-a9246061-fb1e-4a4e-b453-7080d156b432.png)
### 9 Menghapus kolom keterangan:
```
ALTER TABLE biodata DROP COLUMN keterangan;
```
![229924870-98e06689-9b9f-4463-ad65-97c58daf071f](https://user-images.githubusercontent.com/115862112/230745923-a4439e0b-6894-45d4-9677-956c6de8f001.png)

### 10.Mengganti nama tabel menjadi data_mahasiswa:
```
ALTER TABLE biodata RENAME TO data_mahasiswa; 
```
![image](https://user-images.githubusercontent.com/115862112/230745992-b8f603f2-7322-450b-ab09-eb7e63c3f945.png)

### 11. Mengganti nama field id menjadi nim:
```
ALTER TABLE data_mahasiswa CHANGE id nim CHAR(11);
```
![229924957-0196bda8-ad3a-4d8f-9e02-3a4d7a1ef278](https://user-images.githubusercontent.com/115862112/230746027-2742d4d1-b264-496d-9bc0-8b642dd0c44f.png)

### 12. Menjadikan nim sebagai PRIMARY KEY:
```
ALTER TABLE data_mahasiswa ADD PRIMARY KEY (nim);
```
![229924997-bff61b23-f7d0-40b8-9275-2d2a481017bd](https://user-images.githubusercontent.com/115862112/230746032-d3363946-b6de-434d-9f1c-a8c7002119ff.png)

### 13. Menjadikan kolom email sebagai UNIQUE KEY:
```
ALTER TABLE data_mahasiswa ADD UNIQUE KEY (email);
```
HASIL OUTPUT AKHIR
![image](https://user-images.githubusercontent.com/115862112/230746054-ea5e4868-6abc-42eb-86f9-8a1a7e74b169.png)


=======================================================================================================================================================================================================================================

### 1. Membuat Data Base Lathian1

![229927909-f167b637-2226-41c0-80ce-e802998dc382](https://user-images.githubusercontent.com/115862112/230746065-e3dfa3be-285f-49e9-8e43-1a68eef10335.png)

### 2. Membuat Tabel
```
CREATE TABLE siswa (nama VARCHAR(100),alamat TEXT);
```
![229928072-d756fe74-cc49-46ac-b96b-2800e1bfdc05](https://user-images.githubusercontent.com/115862112/230746120-898c58c1-1a12-4475-84e4-92dd77a03c73.png)

### 3. Menambahkan Kolom Di Awal
```
ALTER TABLE siswa ADD COLUMN id INT FIRST;
```
![229929010-a24d5d02-8e78-4757-8d0b-c57901582c6d](https://user-images.githubusercontent.com/115862112/230746133-bdf9ff2d-134a-4164-96fc-a5ef60d8adf0.png)

### 4. Mengubah Nama Kolom
```
ALTER TABLE siswa CHANGE keterangan kelas VARCHAR(10);
```
![229929193-ed8f6bd3-9cf0-4487-916a-eaed4b66e454](https://user-images.githubusercontent.com/115862112/230746156-035399ab-b7ca-40f0-baeb-1aa9633c3190.png)

### 5. Mengubah Tipe Data
```
VARCHAR(10) menjadi VARCHAR(11)
```
![image](https://user-images.githubusercontent.com/115862112/230746165-e1d165e8-32ed-4b2e-b82a-2ec9f0700dad.png)

### 6. Menghapus Kolom
```
ALTER TABLE siswa DROP COLUMN kelas;
```
![image](https://user-images.githubusercontent.com/115862112/230746195-579d06e8-b1b2-4a78-9f72-e8c5e6da0a68.png)

### 7. Menambahkan Primary Key Id
```
ALTER TABLE siswa ADD PRIMARY KEY(id);
```
![image](https://user-images.githubusercontent.com/115862112/230746197-2ede73fa-2a5f-4108-9ffd-b1645d8e60b6.png)

### 8. Menghapus Primary Key
```
ALTER TABLE siswa DROP PRIMARY KEY;
```
![image](https://user-images.githubusercontent.com/115862112/230746199-bf41b479-f7eb-4675-b20b-59ccf180b43f.png)

### 9. Menambahkan Constraint
```
ALTER TABLE siswa ADD CONSTRAINT PK_siswa PRIMARY KEY(id);
```
![image](https://user-images.githubusercontent.com/115862112/230746204-698c2c8f-5766-4f51-a3a0-b3f1e1c3fee2.png)

### 10. Menghapus Constraint Primary Key juga Bisa Seperti Ini:
```
ALTER TABLE siswa DROP PRIMARY KEY;
```
![image](https://user-images.githubusercontent.com/115862112/230746210-767417cb-7c91-430d-83d2-5e128dc6fa14.png)

Apa maksud dari int (11)? Yang dimaksud int(11) artinya suatu data yang dipakai atau digunakan menggunakan tipe data int atau integer dengan length atau panjang karakter 11.
Ketika kita melihat struktur tabel dengan perintah desc, ada kolom Null yang berisi Yes dan No. Apa maksudnya? Apabila Null berisi no, maka data tersebut nantinya akan dilakukan pengisian atau penginputan. Sedangkan apabila Null berisi yes, maka artinya data tersebut akan dikosongkan atau tidak dilakukan penginputan.
