# Run gprMax on Kaggle
Run gprMax using Kaggle GPU :)

## Requirements：
Only Kaggle account.

## Installation
Just gprMax.

### 1.Install gprMax
Please make sure the GPU is available.
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

Run gprMax on Kaggle GPU is really easy