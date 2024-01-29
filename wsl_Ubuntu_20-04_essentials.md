### WSL Ubuntu 20.04 essentials installation 

#### Installing miniconda as package manager to handle GPU drivers 
https://docs.conda.io/projects/miniconda/en/latest/

These four commands quickly and quietly install the latest 64-bit version of the installer and then clean up after themselves. To install a different version or architecture of Miniconda for Linux, change the name of the .sh installer in the wget command.

```bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```

After installing, initialize your newly-installed Miniconda. The following commands initialize for bash and zsh shells:

```bash
~/miniconda3/bin/conda init bash
~/miniconda3/bin/conda init zsh
```


#### Installing tensorflow for GPU 
[https://www.tensorflow.org/install/pip#windows-wsl2_1](https://www.tensorflow.org/install/pip#windows-wsl2_1:~:text=python3%20%2Dm%20pip%20install%20tensorflow%5Band%2Dcuda%5D)


```bash
pip install tensorflow[and-cuda]
```

#### Installing pytorch for GPU 
[https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/#:~:text=pip3%20install%20torch%20torchvision%20torchaudio%20%2D%2Dindex%2Durl%20https%3A//download.pytorch.org/whl/cu121)


```bash
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
```