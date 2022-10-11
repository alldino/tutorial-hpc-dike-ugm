Tentang BigBang
===============
**BigBang** merupakan sistem **High Performance Computing** (HPC) yang dimiliki oleh **Departemen Ilmu Komputer dan Elektronika** (DIKE), Universitas Gadjah Mada.
Saat ini, **BigBang** terdiri dari 2 yaitu:

* BigBang **Solis**
* BigBang **Luna**

BigBang Solis
-------------
BigBang **Solis** memiliki spesifikasi sebagai berikut:

:guilabel:`GPU`
    * 4x GPU Geforce GTX 1080 Ti, RAM @16GB 
    * 3x GPU Geforce GTX 2080 Ti, RAM @32GB
    * 1x GPU Geforce GTX 1070 Ti, RAM 16GB
    * 1x GPU Geforce RTX 2070, RAM 16GB

BigBang Luna
------------
BigBang **Luna** dimiliki oleh DIKE di akhir tahun 2021 dengan spesifikasi sebagai berikut:

:guilabel:`GPU`
    * GPUs 8x NVIDIA A100 HPC 40GB and AI Compute FP64/TF32*/FP16*/INT8*156TF/2.5PF*/5PF*/10POPS*
    * Total GPUs Memory 320 GB
    * NVIDIA NVLink 3rd generation
    * NVIDIA NVSwitch 2nd generation
    * NVIDIA NVSwitch GPU-to-GPU Bandwidth 600 GB/s
    * Total Aggregate Bandwidth 4.8 TB/s

:guilabel:`CPU`
    * Dual AMD Rome 7742, 128 cores total, 2.25 GHz (base), 3.4 GHz (max boost)

:guilabel:`System Memory`
    * 1TB

**Networking**
    * 8x Single-Port Mellanox ConnectX-6 VPI 200Gb/s HDR InfiniBand 
    * 1x Dual-Port Mellanox ConnectX-6 VPI 10/25/50/100/200Gb/s 
    * Ethernet

**Storage**
    * OS: 2x 1.92TB M.2 NVME drives 
    * Internal Storage: 15TB (4x 3.84TB) U.2 NVME drives

**Software**
    * DGX OS 5.4 (Ubuntu Linux OS ``20.04.4``)
    * Nvidia-Driver version ``470.141.03``
    * CUDA version ``11.4``
    * NVIDIA Deepops version ``22.08`` 
    * Kubernetes version ``1.24.4``
    * Kubeflow version ``v1.6.0``
    * Standard Image (Repo docker.io):
        * kubeflownotebookswg/jupyter-tensorflow-cuda-full:v1.6.0 (Cuda version ``11.2``)
        * kubeflownotebookswg/jupyter-pytorch-cuda-full:v1.6.0
        * kubeflownotebookswg/rstudio-tidyverse:v1.6.0
        * kubeflownotebookswg/codeserver-python:v1.6.0
        * kubeflownotebookswg/tensorboards-web-app:v1.6.0
    
