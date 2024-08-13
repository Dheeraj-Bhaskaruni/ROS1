WSL 2 installation of UBUNTU 20.04 along with GPU Support 

1. **Install WSL with distribution**

### Option 1 :  

```bash
#check for the required version
wsl --list --online

#choose from the list
wsl --install <Distribution Name>

#else default version will be installed with the below command
#wsl --install

```

### Option 2

-Download required Ubuntu version from Microsoft store, reboot system.  
-Open the “Ubuntu” application using the “Start” menu.'     
-complete following steps: 

>“Enter new UNIX username:”  
>“New password:”    
>“Retype new password:”_  

-Finally it says “Installation successful!”     

### ***example appearance: your username + “@DESKTOP” + some random numbers and letters. If you see that, continue below.***


2.  **CUDA on WSL User Guide**

Follow the steps here: https://docs.nvidia.com/cuda/wsl-user-guide/index.html#getting-started-with-cuda-on-wsl-2

Install Pytorch:


```bash

sudo apt update && sudo apt upgrade
sudo apt install python3 python3-pip
pip3 install torch torchvision torchaudio
sudo apt install python-is-python3 # this helps us to call python3 wherever there is python
pip3 install numba
```

Check installation

```bash
python

>>> import torch
>>> torch.cuda.is_available()
True
>>>

```









