# GPU Driver for Ubuntu

## Install cuda libs

https://developer.nvidia.com/cuda-downloads

Download cuda keyring and install cuda-toolkit

```sh
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2204/x86_64/cuda-keyring_1.1-1_all.deb
sudo dpkg -i cuda-keyring_1.1-1_all.deb
sudo apt update
sudo apt -y install cuda
sudo apt -y install cuda-toolkit-12-5
sudo apt install nvidia-driver-555
```
