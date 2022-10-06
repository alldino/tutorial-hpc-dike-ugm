Tutorial 01 - Kubeflow Dasar 
============================

.. warning::

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

.. figure:: /_static/gbr/tutorial/01/make-note.gif
    :width: 100%
    :align: center
    :alt: Cara membuat notebook  

    Cara membuat notebook

Mengakses Notebook
------------------

.. figure:: /_static/gbr/tutorial/01/akses-note.gif
    :width: 100%
    :align: center
    :alt: Cara mengakses notebook  

    Cara mengakses notebook

Menjalankan Notebook
--------------------

.. figure:: /_static/gbr/tutorial/01/exec-note.gif
    :width: 100%
    :align: center
    :alt: Cara menjalankan notebook  

    Cara menjalankan notebook

Menampilkan Grafik dengan Tensorboard
-------------------------------------

.. figure:: /_static/gbr/tutorial/01/show-graph-note.gif
    :width: 100%
    :align: center
    :alt: Cara menampilkan grafik notebook  

    Cara menampilkan grafik notebook

