# Anime vs Cartoon vs Human
<a href="https://www.kaggle.com/datasets/hadiepratamatulili/anime-vs-cartoon-vs-human"> Link Dataset Anime VS Cartoon VS Human</a>

## Perkenalkan Kami dari kelompok 3 kelas A2 2021, project ini dibuat guna untuk memenuhi tugas proyek akhir Pratikum Kecerdasan Buatan :computer::robot:	:gear:

### Anggota Kelompok

[o] <a href="https://github.com/Hadieee" target="_blank"> Hadie Pratama Tulili </a> [2109106043]

* Ketua Kelompok
* Preprocessing dan Modelling :microscope:

[o] <a href="https://github.com/Firdaus1223" target="_blank"> Muhammad Firdaus </a> [2109106052]

* Anggota Kelompok
* Metadata dan Analyst :memo:

[o] <a href="https://github.com/rafiizdhr" target="_blank"> Rafi Izdihaar </a> [2109106053]

* Anggota Kelompok
* Visualization :framed_picture:

## CONTOH CNN :link:
![CNN](https://user-images.githubusercontent.com/92103598/205533611-c5808f12-4762-4537-b138-bd590506b542.gif)

## Deskripsi Dataset :mag_right:
  Ukuran Gambar dari dataset ini cukup beragam. Untuk Folder Anime ukuran gambar bervariasi dari 25 x 25 hingga 186 x 186. Untuk Folder Cartoon ukuran gambar bervariasi dari 74 x 200 hingga 519 x 97. Untuk Folder Human memiliki ukuran gambar yang sama semua yaitu 1024 x 1024. Dataset Ini memiliki 3 class yaitu anime, cartoon dan human yang masing-masing class memiliki jumlah gambar yang berbeda. banyak data di class anime adalah sebesar 3004 gambar, cartoon sebesar 2913 gambar, dan untuk human sebesar 3000 gambar.
 
### Data Pada Semua Class
```python
plt.figure(figsize=(15, 35))
sns.set_theme()
plt.subplot(3, 1, 1)
sns.countplot(x=tag)
plt.xlabel('Anime VS Cartoon VS Human')
plt.ylabel('Jumlah')
plt.title('Jumlah Data semua class')
plt.show()
```
![alldata](https://user-images.githubusercontent.com/92103598/205793979-20758163-9e5e-44fd-9eae-dd20632d997c.jpg)

### Jumlah Data setiap kelas dalam **Training**, **Testing** dan **Validation**
```python
# Diagram bar untuk masing2 datasplit

plt.figure(figsize=(15, 35))

sns.set_theme()

plt.subplot(3, 1, 1)
sns.countplot(x=TR)
plt.xlabel('Anime VS Cartoon VS Human')
plt.ylabel('Jumlah')
plt.title('Jumlah Data Per Kelas Yang Ada di Train Set')

plt.subplot(3, 1, 2)
sns.countplot(x=TS)
plt.xlabel('Anime VS Cartoon VS Human')
plt.ylabel('Jumlah')
plt.title('Jumlah Data Per Kelas Yang Ada di Testing Set')

plt.subplot(3, 1, 3)
sns.countplot(x=VL)
plt.xlabel('Anime VS Cartoon VS Human')
plt.ylabel('Jumlah')
plt.title('Jumlah Data Per Kelas Yang Ada di Validation Set')

plt.show()
```
![Train](https://user-images.githubusercontent.com/92103598/205794979-8e0e4cbe-2e9c-447a-8cab-9152fa6014ac.jpg)
![Test](https://user-images.githubusercontent.com/92103598/205795029-61a81a1b-25fc-4ed4-ab3c-998858a0a160.jpg)
![Validation](https://user-images.githubusercontent.com/92103598/205795058-8cd01de2-01a3-4a59-b589-b8b58e2631b4.jpg)


