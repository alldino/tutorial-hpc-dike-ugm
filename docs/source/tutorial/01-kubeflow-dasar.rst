Tutorial 01 - Kubeflow Dasar 
============================

.. warning::
    :align: center

    Mohon maaf masih dalam tahap perbaikan dan pembangunan! 
    Terima kasih ....

:guilabel:`Tutorial 01 - Kubeflow Dasar` ini ditujukkan kepada pengguna DGX-A100 agar lebih mudah dalam bekerja dan menggunakan fitur layanan dari antarmuka :guilabel:`Kubeflow` berbasis web.

Apa itu Notebook Kubeflow?
--------------------------

Kubeflow Notebooks menyediakan cara untuk menjalankan lingkungan pengembangan berbasis web di cluster Kubernetes Anda dengan menjalankannya di pod.

Fitur utama dari Notebook Kubeflow:

* Dilengkapi dengan fitur `JupyterLab <https://github.com/jupyterlab/jupyterlab>`_, `RStudio <https://www.rstudio.com/products/rstudio/#rstudio-server>`_ dan `Visual Studio Code (code server) <https://github.com/cdr/code-server>`_.
* Pengguna dapat membuat wadah notebook secara langsung di dalam cluster, seolah-olah sedang menggunakan workstation milik sendiri.
* Pengguna dapat memilih daftar image yang tersedia untuk notebooknya atau mengunduh image dari tempat lain, sesuai dengan paket library yang diperlukan, tanpa harus menginstall dari awal.
* Adanya fitur RBAC (*Role Based Access Control*) Kubeflow, memungkinkan untuk berbagi data dan saling berkontribusi dengan pengguna lainnya.  
* Pengguna memiliki akses internet untuk mengunduh contoh kode program notebook yang diinginkan.

Mengakses Dashboard 
-------------------

Silahkan buka :guilabel:`browser` Anda, kemudian pada bagian :guilabel:`address bar` isikan alamat IP dari server DGX-A100, seperti ``http://<alamat ip>:<port layanan>``.
Setelah diisi akan tampil halaman login dari Notebook Kubeflow. Silahkan isikan ``user name`` dan ``password`` Anda.

.. figure:: /_static/gbr/tutorial/01/dashboard.png 
    :width: 100%
    :align: center
    :alt: Tampilan halaman login notebook kubeflow 

    Tampilan halaman login notebook kubeflow

.. note::

    Bagi **pengguna baru** :guilabel:`HPC - DIKE UGM`, untuk dapat menggunakan layanan :guilabel:`DGX-A100` dimohon untuk mendaftar di `web HPC - DIKE UGM <https://hpc.dcseugm.id>`_.
    Bila membutuhkan informasi lebih lanjut, silahkan hubungi :guilabel:`Helpdesk HPC - DIKE UGM`!

Tampilan Halaman Utama Dashboard 
--------------------------------

Setelah login maka akan tampil halaman utama dari dashboard notebook kubeflow. Dashboard kubeflow ini berisi beberapa menu yang merupakan tautan cepat dari berbagai komponen yang diperlukan untuk pengolahan notebook Anda seperti notebook, pipeline, katib, dll.

.. figure:: /_static/gbr/tutorial/01/utama.png 
    :width: 100%
    :align: center
    :alt: Tampilan halaman utama dashboard notebook kubeflow 

    Tampilan halaman utama dashboard notebook kubeflow

Membuat Notebook 
----------------

Untuk membuat ``notebook`` silahkan akses menu :guilabel:`Notebooks` di bagian kiri sidebar, dan klik tombol :guilabel:`New Notebook`. Pada halaman :guilabel:`New Notebook`, silahkan isikan bagian :guilabel:`Name` dari notebook yang akan dibuat, misalnya ``contoh01``.

.. tips::

    Nama dari notebook **wajib** menggunakan ``huruf`` dan ``angka`` dan tidak boleh ada ``spasi``. Sebagai contoh: ``contoh01``.

Pada bagian :guilabel:`Docker image` tersedia beberapa opsi pilihan yaitu:

1. :guilabel:`Standard image`
   :guilabel:`Standard image` ini merupakan ``image docker`` bawaan dari sistem yang siap digunakan oleh pengguna. Secara default ada tiga **Integrated Development Environment (IDE)** yang disediakan yaitu:

   *  :guilabel:`JupyterLab`
   *  :guilabel:`Code Server` atau sering dikenal dengan :guilabel:`Visual Code Server`
   *  :guilabel:`RStudio`

2. :guilabel:`Custom image`
   :guilabel:`Custom image` ini merupakan ``image docker`` yang bisa diunduh dari *repository* semisal dari ``docker.io``, ``nvcr.io``, ``gcr.io``, dll.

Pada :guilabel:`Tutorial 01 - Kubeflow Dasar` akan mengunakan fitur dari **IDE** :guilabel:`JupyterLab` dan :guilabel:`image` yang digunakan yaitu ``kubeflownotebookswg/jupyter-tensorflow-cuda-full:v1.6.0``. 

Selanjutnya spesifikasi yang digunakan yaitu :guilabel:`CPU` ``= 8 core``, :guilabel:`RAM` ``= 16 GB``, :guilabel:`GPU` ``= 1 GPU NVIDIA``, dan :guilabel:`Workspace Volume` ``= 10 GB`` disesuaikan dengan kebutuhan komputasi yang diperlukan untuk mengolah :guilabel:`notebook`. Setelah semua ``konfigurasi`` sudah ditentukan, klik tombol :guilabel:`Launch` untuk membuat :guilabel:`notebook`. 

.. note::

    Bila spesifikasi :guilabel:`CPU`, :guilabel:`RAM`, :guilabel:`GPU`, dan :guilabel:`Workspace Volume` yang dimasukkan tidak sesuai dengan yang **disetujui** oleh **Tim Pengelola DLRC UGM**, maka :guilabel:`notebook` tidak akan terbentuk dan ada ``informasi error terkait dengan spesifikasi yang berjalan tidak sesuai``. 

.. figure:: /_static/gbr/tutorial/01/make-note.gif
    :width: 100%
    :align: center
    :alt: Cara membuat notebook  

    Cara membuat notebook

Mengakses Notebook
------------------

Setelah :guilabel:`notebook` sudah terbentuk, untuk mengaksesnya klik tautan :guilabel:`CONNECT`. Maka akan tampil satu tab baru di :guilabel:`browser` menampilkan halaman dari **IDE** :guilabel:`JupyterLab`. Halaman utama dari **IDE** :guilabel:`JupyterLab` memiliki :guilabel:`menu`:

#. :guilabel:`Notebook`
    berfungsi untuk membuka :guilabel:`editor` notebook, menjalankan ``command`` langkah demi langkah atau keseluruhan, dan menampilkan ``output`` dari notebook.
#. :guilabel:`Console`
    berfungsi untuk menampilkan :guilabel:`terminal atau console` lingkungan khusus pemrograman ``Python``.
#. :guilabel:`Others`
    * :guilabel:`Terminal`
        berfungsi mirip seperti :guilabel:`shell` atau :guilabel:`terminal command line`.
    * :guilabel:`Text File`
        berfungsi mirip dengan :guilabel:`Editor` untuk berkas berbentuk ``Text`` atau ``*.txt``.
    * :guilabel:`Markdown File`
        berfungsi mirip dengan :guilabel:`Editor` untuk berkas berbentuk ``Markdown`` atau ``*.md``.
    * :guilabel:`Python File`
        berfungsi mirip dengan :guilabel:`Editor` untuk berkas berbentuk ``Python`` atau ``*.py``.
#. :guilabel:`Menu Sidebar kiri`:
    * :guilabel:`File Browser`
        berfungsi untuk melihat isi ``file`` dan ``folder`` yang digunakan.
    * :guilabel:`Running Terminal and Kernel`
        berfungsi untuk melihat daftar dan mematikan ``Terminal`` dan ``Kernel`` yang digunakan.
    * :guilabel:`Git`
        berfungsi untuk mengatur koneksi dan update berkas ``project`` yang disimpan pada *repository* ``http://github.com``.
    * :guilabel:`Table of Contents`
        berfungsi untuk menampilkan daftar isi dari suatu berkas ``notebook``.
    * :guilabel:`Extension Manager`
        berfungsi untuk menambahkan atau menghapus ``plugins`` yang digunakan pada **IDE** :guilabel:`JupyterLab`

.. figure:: /_static/gbr/tutorial/01/jupyterlab.png
    :width: 100%
    :align: center
    :alt: Halaman utama IDE JupyterLab  

    Halaman utama IDE JupyterLab

.. figure:: /_static/gbr/tutorial/01/akses-note.gif
    :width: 100%
    :align: center
    :alt: Cara mengakses notebook  

    Cara mengakses notebook

Menjalankan Notebook
--------------------

Berkas yang diperlukan dalam :guilabel:`Tutorial 01 - Kubeflow Dasar` ini dapat diunduh pada tautan berikut:

`TensorFlow 2 quickstart for experts Example <https://storage.googleapis.com/tensorflow_docs/docs/site/en/tutorials/quickstart/advanced.ipynb>`_

Berkas ``advanced.ipyb`` dapat diunggah dari komputer lokal ke **IDE** :guilabel:`JupyterLab` dengan cara melakukan ``drag dan drop`` pada berkas tersebut menuju bagian sidemenu :guilabel:`File Browser`. Buka berkas tersebut dan klik tombol :guilabel:`RUN` pada *toolbar* untuk mengeksekusi langkah-demi-langkah atau klik tombol :guilabel:`double-chevron (>>)` untuk mengeksekusi keseluruhan isi dari berkas ``advanced.ipyb``. 

.. figure:: /_static/gbr/tutorial/01/exec-note.gif
    :width: 100%
    :align: center
    :alt: Cara menjalankan notebook  

    Cara menjalankan notebook

Menampilkan Grafik dengan Tensorboard
-------------------------------------

Visualisasi dari hasil eksperimen :guilabel:`notebook` dapat dilakukan dengan menggunakan :guilabel:`tensorboard`. :guilabel:`Tensorboard` menyediakan cara untuk memvisualisasikan eksperimen ML (*Machine Learning*) yang dijalankan, seperti melacak metrik kehilangan (*loss*) dan akurasi (*accuracy*) serta melihat histogram yang bias, bagan model, dan banyak lagi. Untuk informasi lebih lanjut tentang :guilabel:`tensorboard`, silakan kunjungi situs `tensorboard <https://www.tensorflow.org/tensorboard>`_.

Sebagai contoh sederhana, silahkan gunakan kembali server :guilabel:`notebook` yang dibuat pada langkah sebelumnya. Hubungkan dan unggah :guilabel:`notebook` baru untuk :guilabel:`Tensorboard`. Sebelum diunggah silahkan unduh :guilabel:`notebook` berikut:

`Get started with TensorBoard <https://storage.googleapis.com/tensorflow_docs/tensorboard/docs/get_started.ipynb>`_

.. figure:: /_static/gbr/tutorial/01/tensorboard.png
    :width: 100%
    :align: center
    :alt: Cara membuat tensorboard  
    
    Cara membuat tensorboard  

Perhatikan alamat dari folder ``logs``. Lokasi ini diperlukan untuk pembuatan :guilabel:`Tensorboard`. Jalankan :guilabel:`notebook` dan pada halaman :guilabel:`Kubeflow`, buka menu :guilabel:`Tensorboards`. Klik tombol :guilabel:`New Tensorboard`. Beri ``nama`` misalnya ``logs-fit`` dan centang kotak ``PVC``. Pilih ``volume workspace notebook`` dari daftar drop-down dan pada bagian ``Mount Path``, masukkan alamat lokasi folder ``logs`` yang dicatat pada langkah sebelumnya. Dalam contoh ini adalah ``logs/fit``.

.. figure:: /_static/gbr/tutorial/01/make_tensorboard.png
    :width: 100%
    :align: center
    :alt: Cara konfigurasi tensorboard  
    
    Cara konfigurasi tensorboard  

Klik tombol :guilabel:`Create` dan :guilabel:`Tensorboard` siap digunakan dalam beberapa menit. Amati tampilkan metrik dan grafik yang berbeda.

.. figure:: /_static/gbr/tutorial/01/show-graph-note.gif
    :width: 100%
    :align: center
    :alt: Cara menampilkan grafik notebook  

    Cara menampilkan grafik notebook

**Referensi:**
`Kubeflow-Basics <https://charmed-kubeflow.io/docs/kubeflow-basics>`_