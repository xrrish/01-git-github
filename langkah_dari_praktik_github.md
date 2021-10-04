# Langkah Langkah Github dari Praktik diatas

## Membuat Akun & Install
1. Membuat akun github terlebih dahulu bisa klik [disini](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwj7hZaIu63zAhXE8HMBHZEgChUQFnoECAsQAQ&url=https%3A%2F%2Fgithub.com%2Fsignup&usg=AOvVaw0a6qEmIZVdziwPUb-hFApr)
2. Instal Github bisa klik [disini](https://git-scm.com/downloads), lalu instal seperti biasa
3. Untuk mengecek github sudah terpasang atau belum bisa dengan menuliskan `git --version` di command prompt atau di git bash

## Konfigurasi Github
tuliskan seperti ini di command prompt atau di git bash anda

```
git config --global user.name "Nama Anda di GitHub"
git config --global user.email "email@domain.com"
```

lalu untuk mengeceknya bisa dengan menuliskan    `git config --list`

## Membuat Repository
1. Klik tanda + pada bagian atas setelah login, pilih **New Repository**\
![1](/img/1.png)
2. Isikan nama, keterangan, serta lisensi. Jika dikehendaki, bisa membuat Repo Private\
![2](/img/1.2.png)
3. Lalu klik Create **Repository**

## Clone Repo
Proses clone adalah proses untuk menduplikasikan remote repo di GitHub ke komputer lokal. Untuk melakukan proses clone, gunakan perintah berikut:

`git clone "isi dengan link repo kalian"`

Lalu ubah Repo menjadi Master/Utama dengan cara menuliskan :
```
cd "namarepo"
git branch -m main`
```
## Perintah Dasar Github
##### GIT CONFIG
Salah satu perintah git yang paling banyak digunakan adalah git config, yang bisa digunakan untuk mengatur konfigurasi tertentu sesuai keinginan pengguna, seperti email, algoritma untuk diff, username, format file, dll. Contohnya, perintah berikut bisa digunakan untuk mengatur email:\
`git config --global user.email sam@google.com`

##### GIT INIT
Perintah ini digunakan untuk membuat repositori baru. Caranya:\
`git init`

##### GIT ADD
Perintah git add bisa digunakan untuk menambahkan file ke index. Contohnya, perintah berikut ii akan menambahkan file bernama temp.txt yang ada di direktori lokal ke index:\
`git add temp.txt`

##### GIT CLONE
Perintah git clone digunakan untuk checkout repositori. Jia repositori berada di remove server, gunakan: `git clone alex@93.188.160.58:/path/to/repository`
Jika salinan repositori lokal ingin dibuat, gunakan : `git clone/path/to/repository` 

##### GIT COMMIT
Perintah git commit digunakan untuk melakukan commit pada perubahan ke head. Ingat bahwa perubahan apapun yang di-commit tidak akan langsung ke remote repository. Gunakan:\
`git commit –m “Isi dengan keterangan untuk commit”`

##### GIT STATUS
Perintah git status menampilkan daftar file yang berubah bersama dengan file yang ingin di tambahkan atau di-commit. Gunakan: `git status`

##### GIT PUSH
git push adalah perintah git dasar lainnya. Push akan mengirimkan perubahan ke master branch dari remote repository yang berhubungan dengan direktori kerja Anda. Misalnya:\
`git push origin master`

##### GIT CHECKOUT
Perintah git checkout bisa digunakan untuk membuat branch atau untuk berpindah diantaranya. Misalnya, perintah berikut ini akan membuat branch baru dan berpindah ke dalamnya: `command git checkout -b <nama-branch>`
Untuk berpindah dari branch satu ke lainnya, gunakan: \
`git checkout <branch-name>`

##### GIT REMOTE
Perintah git remote akan membuat user terhubung ke remote repository. Perintah berikut ini akan menampilkan repository yang sedang dikonfigurasi:\
`git rmote -v` \
Perintah ini membuat user bisa menghubungkan repository lokal ke remote server:\
`git remote add origin <93.188.160.58>`

##### GIT BRANCH
Perintah git branch bisa digunakan untuk me-list, membuat atau menghapus branch. Untuk menampilkan semua branch yang ada di repository, gunakan:\
`git branch` \
Untuk menghapus branch: \
`git branch -d <branch-name>`

##### GIT PULL
Untuk menggabungkan semua perubahan yang ada di remote repository ke direktori lokal, gunakan perintah pull: \
`git pull`

##### GIT MARGE
Perintah merge digunakan untuk menggabungkan sebuah branch ke branch aktif. Gunakan:\
`git merge <nama-branch>`

##### GIT DIFF
Perintah git diff digunakan untuk menampilkan conflicts. Untuk melihat conflicts dengan file dasar, gunakan:\
`git diff --base <nama-file>`\
Perintah berikut digunakan untuk menampilkan conflicts diantara branch yang akan di-merge:\
`git diff <source-branch> <target-branch>`\
Untuk menampilkan semau conflict yang ada, gunakan:\
`git diff`

##### GIT TAG 
Tagging digunakan untuk menandai commits tertentu. Contohnya: \
`git tag 1.1.0 <insert-commitID-here>`

##### GIT LOG
Dengan menjalankan peritah ini akan menampilkan daftar commits yang ada di branch beserta detail-nya. Contoh outputnya adalah:
```
•	commit 15f4b6c44b3c8344caasdac9e4be13246e21sadw
•	Author: Alex Hunter <alexh@gmail.com>
     Date: Mon Oct 1 12:56:29 2016 -0600
```
##### GIT RESET
Untuk me-reset index dan bekerja dengan kondisi commit paling baru, gunakan perintah git reset:\
`git reset --hard HEAD`

##### GIT RM
Gunakan perintah ini untuk menghapus file dari index dan direktori kerja. Contohnya:\
`git rm filename.txt`

##### GIT STASH
Mungkin inilah salah satu perintah dasar git yang jarang digunakan orang, yang bisa membantu menyimpan perubahan yang tidak langsung di-commit, namun hanya sementara. Contoh:\
`git stash`

##### GIT SHOW
Untuk menampilkan informasi tentang object pada git, gunakan git show:\
`git show`

##### GIT FECTH
Perintah ini digunakan untuk menampilkan semua object dari remote repository yang tidak berada di direktori kerja lokal. Contohnya:\
`git fetch origin`

##### GIT LS-TREE
Untuk menampilkan susunan object berdasarkan nama dan mode setiap item, dan nilai blob SHA-1, gunakan perintah git ls-tree. Contohnya:\
`git ls-tree HEAD`

##### GIT CAT-LIFE
Menggunakan nilai SHA-1, menampilkan tipe object dengan menggunakan perintah git cat-file. Contohnya:\
`git cat-file –p d670460b4b4aece5915caf5c68d12f560a9fe3e4`

##### GIT PREP
git prep mengizinkan pengguna mencari frase dan/atau kata yang berada di dalam direktori. Contohnya, untuk mencari www.hostinger.co.id di dalam semua file, gunakan:\
`git grep "www.hostinger.co.id"`

##### GITK
gitk adalah tampilan grafis dari repository lokal yang bisa dipanggil dengan menjalankan perintah:\
`gitk`

##### GIT INSTAWEB
Dengan perintah git instaweb, web server bisa dijalan berdampingan dengan repository lokal. Nantinya web browser akan langsung diarahkan ke server tersebut. Contohnya:\
`git instaweb –httpd=webrick`

##### GIT GC
Untuk mengoptimasi repository melalui garbage collection, yang akan membersihkan file yang tidak dibutuhkan dan mengoptimasinya, gunakan:\
`git gc`

##### GIT ARCHIVE
Perintah git archive memungkinkan user membuat file zip atau tar yang mengandung susunan repository. Contohnya:\
`git archive --format=tar master`

##### GIT PRUNE
Melalui perintah git prune, object yang tidak memiliki incoming pointers akan dihapus. Gunakan:\
`git prune`

##### GIT FSCK
Untuk membuat pengecekan keseluruhan dari file system git, gunakan perintah git fsck. Object yang corrupt akan dikenali:\
`git fsck`

##### GIT REBASE
Perintah ini digunakan untuk menerapkan ulang commit di branch yang lain. Contohnya:\
`git rebase master`