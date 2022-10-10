Tutorial 02 - Conda Virtual Environment 
=======================================

:guilabel:`Tutorial 02 - Tutorial Conda Virtual Environment` 
ini menjelaskan secara singkat kepada pengguna cara untuk
mengelola *library* atau *package* yang dibutuhkan, serta untuk
mengisolasi *library*/*package* antar *projects* dengan
menggunakan Conda. Panduan untuk menggunakan Conda
lebih lanjut dapat dilihat pada `tautan berikut`_.
`Cheat sheet`_ Conda berikut juga sangat berguna jika
hanya ingin mengacu perintah-perintah Conda yang awam digunakan.

Conda (**Anaconda**) merupakan sistem pengelelolaan
*package* dan *environment*. Conda dapat digunakan
untuk mengunduh dan menginstall *library* python yang dibutuhkan 
serta *package* lainnya, seperti **Cudatoolkit** versi tertentu
yang berbeda dari **Cudatoolkit** versi bawaan yang
sudah terinstall terlebih dahulu pada *image* notebook
yang dipilih.

Jika pengguna memiliki lebih dari satu *project*
pada satu *notebook* dan ingin agar *library/package*
tiap *project* terisolasi dari *project* lainnya,
maka pengguna dapat membuat *environment* untuk tiap
*project*. Salah satu manfaat dari 
mengisolasi *library/package* *project* yang berbeda 
di *environment* yang berbeda adalah untuk
menghindari konflik *library/package* ataupun
versi dari *library/package* yang dibutuhkan
masing-masing *project*.  


Conda Virtual Environment 
-------------------------
Setiap notebook session sudah 
terpasang Conda dengan
*environment* bawaan dengan nama **base**.
*Library/Package* yang terinstall pada *environment*
bawaan ini tergantung pada *image* dari *notebook*
yang dipilih atau disiapkan pengguna pada saat memulai
*notebook session*.  

Membuat *Environment* Baru
~~~~~~~~~~~~~~~~~~~~~~~~~~
Pengguna dapat membuat environment
baru dengan memasukkan perintah berikut::

    conda create -name nama-environment python=versi-python

Sebagai contoh, untuk membuat *environment* baru
dengan nama **project-baru** dengan python versi 3.8,
pengguna memasukkan perintah berikut::

    conda create -name project-baru python=3.8 

Pengguna lalu dapat mengaktifkan *environment* tertentu 
dengan menggunakan perintah berikut::
    
    conda activate nama-environment

Pengguna juga dapat melihat *library/package* yang terinstall
pada *environment* yang sedang aktif dengan perintah berikut::

    conda list

Untuk menonaktifkan *environment* yang sudah diaktifkan,
masukkan perintah berikut::
    
    conda deactivate

Memulai *Environment* dari *File*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Terkadang kita tidak ingin menginstall *library/package*
pada *environment* dari awal, melainkan 
memulai *environment* yang sama dengan *environment* yang sudah 
dimiliki sebelumnya, misalnya dari komputer lokal.
Ini bisa dilakukan dengan menyimpan informasi
dari *environment* yang kita sudah miliki sebelumnya
ke sebuah *file*, lalu menggunakan *file* tersebut
untuk menginisiasi *environment* baru yang ingin kita buat.

Pengguna dapat menyimpan informasi dari
*environment* tertentu ke dalam sebuah file 
dengan mengaktifkan *environment* tersebut terlebih dahulu, 
lalu masukkan perintah berikut::

    conda list --explicit > env-sumber.txt

Nama file untuk penyimpanan (di tutorial ini dimisalkan env-sumber.txt),
dapat dinamai apapun. 

Setelah itu, untuk membuat *environment* baru
dan menginisiasinya dengan file, pengguna dapat
menggunakan perintah berikut::

    conda env create --name env-baru --file env-sumber.txt

Manajemen *Library/Package* dengan Conda
----------------------------------------
Pastikan untuk mengaktifkan *environment* yang
ingin dikelola sebelum menginstall atau menghapus
*library/package* dari *environment* tersebut.
Pengunduhan dan instalasi *library/package*
dapat dilakukan dengan perintah ``conda`` dan
``pip`` (`Pypi`_). Instalasi *library/package* dengan
Conda dapat dilakukan dengan perintah berikut::

    conda install nama-package

Ada beberapa *options* pada perintah ``conda install``
seperti ``-c nama-channel`` untuk menentukan
sumber pengunduhan *library/package* yang diinginkan.
Detail dari *options* untuk perintah ``conda install``
dapat dilihat dengan memasukkan perintah::

    conda install --help

Jika ingin mengunduh dan menginstall *library/package* dengan
``pip``, pastikan *package* **pip** sudah terinstall pada *environment*
yang aktif dengan perintah berikut::

    conda install pip

Jika **pip** belum terinstall pada *environment* yang sedang
aktif, maka *library* yang diinstall akan terinstall pada *environment* bawaan (base).
Jika **pip** sudah terinstall pada environment yang
sedang aktif, maka instalasi dapat dilakukan dengan perintah berikut::

    pip install nama-library

.. _tautan berikut: https://docs.conda.io/
.. _Cheat sheet: https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf
.. _Pypi: https://pypi.org/