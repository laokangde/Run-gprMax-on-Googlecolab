# Run gprMax on Googlecolab
Run gprMax using Google colab GPU

## Requirements：
1. Google account.
2. gprMax package, which you can download [here](https://github.com/gprmax/gprMax) .
3. miniconda3 package, which you can download [here](https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh), remember you need Linux version.

## Installation
The following steps provide guidance on how to install:
1. Mount your google drive, upload gprMax package and miniconda3 package.
2. Install miniconda3.
3. Install gprMax.

### 1.Mount your google drive, upload gprMax package and miniconda3 package.
First, mount your Google drive by running 
```
from google.colab import drive
drive.mount('/content/drive')
```
Then, upload gprMax package and miniconda3 package. Remember unzip gprMax package: `unzip gprMax-master.zip`

![1](https://github.com/laokangde/Run_gprMax_on_googlecolab/blob/master/1.png?raw=true)

### 2.Install miniconda3
Running
```
import os
os.chdir('/content/drive/My Drive')
!chmod 777 Miniconda3-latest-Linux-x86_64.sh
!bash Miniconda3-latest-Linux-x86_64.sh
```
After several ENTER and YES,
you will see this if you successfully installed miniconda3.

![2](https://github.com/laokangde/Run_gprMax_on_googlecolab/blob/master/2.png?raw=true)

### 3.Install gprMax
First, run `!exec bash` and `conda` to check your conda environment, you can see the conda usage like this:

![3](https://github.com/laokangde/Run_gprMax_on_googlecolab/blob/master/3.png?raw=true)

Then run the following commands:
```
cd gprMax-master
conda activate gprMax
conda env create -f conda_env.yml
# build
conda activate gprMax
python setup.py build
python setup.py install
pip install pycuda
```
![4](https://github.com/laokangde/Run_gprMax_on_googlecolab/blob/master/4.png?raw=true)
```
# run gprMax
python -m gprMax fp_sz_0.03.in -gpu -n 40
```

![5](https://github.com/laokangde/Run_gprMax_on_googlecolab/blob/master/5.png?raw=true)

Using colab to run gprMax is alittle annoying because you have to run those commands again after 12h runtime.
Another website: [https://www.paperspace.com/](https://www.paperspace.com/) is something like Google colab, but it can save your gprMax environment after 6h runtime.
