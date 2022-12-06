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
  
```python
file_name = []
tag = []
full_path = []

for path, subdirs, files in os.walk(mypath):
    for name in files:
        full_path.append(os.path.join(path, name)) 
        tag.append(path.split('/')[-1])        
        file_name.append(name) 
df = pd.DataFrame({"path":full_path,'file_name':file_name,"Nama":tag})
df.groupby(['Nama']).size()

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
