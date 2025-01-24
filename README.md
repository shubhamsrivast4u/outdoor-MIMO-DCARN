# DCARN: Efficient Channel State Feedback for Massive MIMO Systems in Outdoor Scenarios

Official implementation of "DCARN: Efficient Channel State Feedback for Massive MIMO Systems in Outdoor Scenarios" by Shubham Srivastava and Adrish Banerjee.



## Dataset

The model is trained on the [COST2100](https://ieeexplore.ieee.org/document/6393523) channel dataset. We recommend using the preprocessed version from [CsiNet](https://ieeexplore.ieee.org/document/8322184). Download this from:
- https://www.dropbox.com/scl/fo/tqhriijik2p76j7kfp9jl/h?rlkey=4r1zvjpv4lh5h4fpt7lbpus8c&e=1&dl=0
- https://pan.baidu.com/s/1Ggr6gnsXNwzD4ULbwqCmjA#list/path=%2F

## Usage

Jupyter notebooks are provided for training and testing:
- `DCARN_eZrYout.ipynb`: Contains code for DCARN-Zx variant with reduction ratio 1/Y
  - Z indicates expansion factor (1, 10, 20, 50)  
  - Y indicates reduction ratio (4, 8, 16, 32, 64)

Update dataset paths in notebooks as needed.

## Acknowledgments 

We thank the authors of:
- [ACRNet](https://github.com/Kylin9511/ACRNet)
- [CRNet](https://github.com/Kylin9511/CRNet)
- [CsiNet](https://github.com/sydney222/Python_CsiNet)

Special thanks to Chao-Kai Wen and Shi Jin's group for providing the preprocessed COST2100 dataset.

```
