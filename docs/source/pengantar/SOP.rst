SOP Penggunaan Fasilitas BigBang 
================================

BigBang Luna
------------

.. note::

  **User** yang akan menggunakan :guilabel:`BigBang Luna`, harus memastikan kode yang akan **di-running** sudah **free** dari ``error``. Sehingga bisa memaksimalkan slot **waktu yang diberikan**.

:guilabel:`BigBang Luna`, dialokasikan penggunaannya untuk :guilabel:`dosen DIKE`, :guilabel:`dosen kolaborator` serta :guilabel:`mahasiswa pascasarjana (S2 ILKOM/S2 MKA/S3 ILKOM)` di lingkungan **Departemen Ilmu Komputer dan Elektronika, FMIPA, UGM**. Untuk menggunakan fasilitas ini, user harus mendaftar terlebih dahulu melalui SI HPC (silahkan cek step-stepnya di bagian `Permohonan <https://tutorial-hpc-dike-ugm.readthedocs.io/en/stable/pengantar/permohonan.html>`_). Berikut ini adalah **SOP penggunaan** :guilabel:`BigBang Luna`:

  * **By default**, setiap ``user`` akan mendapatkan :guilabel:`1 GPU`, :guilabel:`24 Core CPU`, :guilabel:`memory 64 GB` dan :guilabel:`storage 20GB` 
  * Maksimal penggunaan resource adalah **2 hari kalender (2x24 jam)**. Waktu dihitung mulai dari diberikan akses ke fasilitas.
  * Pada masa penggunaan, setiap harinya user **wajib** mensubmit progress report via link berikut `Submit Progress Report <https://forms.gle/YLfYg9ejvCh7BnQP8>`_. Report ditulis dengan menggunakan `Template Progress Report <https://drive.google.com/drive/folders/1MioBtrDfGvee6QQMP_LyqgVNACZ3qz-Y?usp=sharing>`_ ini.
  * Setiap harinya, penggunaan :guilabel:`BigBang Luna` akan dimonitor apakah idle/utilitas rendah
  * ``Jika idle/utilitas rendah`` pada saat monitoring dan ``belum mensubmit progress report`` sampai pukul 23.00, maka service akan **di-disable** per pukul 10.00 (di hari dan jam kerja berikutnya)
  * Jika user yang sudah menggunakan **resource selama 2 hari**  dan **aktif mengupload progress report**, meminta ``tambahan waktu``, maka akan **dicek**:
  
      1. Ada ``slot kosong/tidak``
      2. Ada ``antrian atau tidak`` 
      3. Jika ``ada slot kosong/tidak ada antrian``, bisa **diperpanjang** dengan mempertimbangkan progress, akan ditambahkan 2 hari lagi.
  * **Pengajuan tambahan waktu** bisa dilakukan dengan mengisi poin **perpanjangan waktu** ketika mensubmit progress report di hari ke-2.
  * Setelah 2 hari pemakaian, user akan menerima **notifikasi via e-mail** jika masa pemakaian sudah ``habis`` dan akun akan **di-disable**.
  * Jika 8 slot user DGX sudah **full**, dan ada **request user baru**, maka request akan masuk :guilabel:`antrian list`` dengan **sistem FCFS (First Come First Serve)**.
  * Jika terjadi ``mati listrik/masalah teknis lain``, admin **tidak bertanggung jawab** terhadap data/kode yang sedang dirunning, sehingga user harus melakukan backup sesering mungkin.
  * Kejadian ``mati listrik/masalah teknis`` **tidak mempengaruhi** ``durasi pemakaian`` yang telah ditetapkan sebelumnya (waktu pemakaian akan dianggap terus berjalan).
