# Install TF on Linux (GCP VM)
Version: 2.12.* +

## Install NVIDIA Driver
```
GRUB_CMDLINE_LINUX="nouveau.modeset=0"
sudo apt-get install build-essential linux-headers-$(uname -r) dkms
sudo chmod +x NVIDIA-Linux-x86_64-<version>.run
sudo ./NVIDIA-Linux-x86_64-<version>.run
```
The Driver can be downloaded from NVIDIA.

Test: 
```
nvidia-smi
```

## Install Cuda Toolkit
```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-keyring_1.0-1_all.deb
sudo dpkg -i cuda-keyring_1.0-1_all.deb
sudo apt-get update
sudo apt-get -y install cuda
```

Test:
```
nvcc --version
```

## Install Anaconda
```
sudo apt update
sudo apt install curl -y
cd /tmp
curl --output anaconda.sh https://repo.anaconda.com/archive/Anaconda3-5.3.1-Linux-x86_64.sh
sha256sum anaconda.sh
bash anaconda.sh
source ~/.bashrc
conda list

conda create --name tf python=3.9
conda deactivate
conda activate tf
```
Anaconda might be updated with new version, so come to this website: [https://repo.anaconda.com/archive/](https://repo.anaconda.com/archive/)

## Install Tf
```
conda install -c conda-forge cudatoolkit=11.8.0
pip install nvidia-cudnn-cu11==8.6.0.163
CUDNN_PATH=$(dirname $(python -c "import nvidia.cudnn;print(nvidia.cudnn.__file__)"))
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/:$CUDNN_PATH/lib
mkdir -p $CONDA_PREFIX/etc/conda/activate.d
echo 'CUDNN_PATH=$(dirname $(python -c "import nvidia.cudnn;print(nvidia.cudnn.__file__)"))' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CONDA_PREFIX/lib/:$CUDNN_PATH/lib' >> $CONDA_PREFIX/etc/conda/activate.d/env_vars.sh
pip install --upgrade pip
pip install tensorflow==2.12.*

python3 -c "import tensorflow as tf; print(tf.config.list_physical_devices('GPU'))"
```

## Install Dependencies for CPT
```
pip install google-cloud-bigquery
pip install joblib
pip install numpy
pip install transformers
pip install google-cloud-storage
pip install scikit-learn
pip install pandas
pip install db-dtypes
```




