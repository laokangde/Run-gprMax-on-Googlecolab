# Run gprMax on Kaggle
Run gprMax using Kaggle GPU :)

## Requirements：
Only Kaggle account.

## Installation
Just gprMax.

### 1.Open a new notebook

![1](https://github.com/laokangde/Run-gprMax-on-Googlecolab/blob/master/code.png?raw=true)

Please make sure the GPU is available.

![2](https://github.com/laokangde/Run-gprMax-on-Googlecolab/blob/master/GPU.png?raw=true)

### 2.Install gprMax
Paste the following commands into the cell then run the cell:
```
import os
!git clone https://github.com/gprMax/gprMax.git
os.chdir('/kaggle/working/gprMax')
!conda env update -f conda_env.yml
!python setup.py build
!python setup.py install
```

```
# run gprMax
!python -m gprMax ./user_models/cylinder_Bscan_2D.in -gpu -n 5
```

![3](https://github.com/laokangde/Run-gprMax-on-Googlecolab/blob/master/run_model.png?raw=true)

Run gprMax on Kaggle GPU is really easy
