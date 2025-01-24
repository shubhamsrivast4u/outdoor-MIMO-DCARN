# DCARN: Efficient Channel State Feedback for Massive MIMO Systems in Outdoor Scenarios

Official implementation of "DCARN: Efficient Channel State Feedback for Massive MIMO Systems in Outdoor Scenarios" by Shubham Srivastava and Adrish Banerjee.

## Requirements

- Python 3.7+
- PyTorch
- CUDA-enabled GPU (recommended)
- Additional requirements are listed in 'requirements.txt'


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

## Weights of trained model
The weights of trained models are in 'Experiments/table1' folder


# Results & Performance

## NMSE (dB) Performance and Parameter Comparison
```markdown
| Model | η=1/4 | η=1/8 | η=1/16 | η=1/32 | η=1/64 | Parameters |
|-------|--------|--------|---------|---------|---------|------------|
| **DCARN Variants** |
| DCARN-50x | **-15.05** | **-10.41** | **-7.031** | **-4.448** | **-2.864** | 2.194M |
| DCARN-20x | **-14.58** | **-9.743** | **-6.576** | **-4.102** | **-2.701** | 2.137M |
| DCARN-10x | -14.20 | -9.535 | -6.369 | -3.925 | -2.621 | 2.119M |
| DCARN-1x | -11.89 | -8.315 | -5.336 | -3.448 | -2.32 | 2.10M |

```

### Key Findings
- DCARN-50x achieves state-of-the-art performance (-15.05 dB at η=1/4)
- Uses 7.3% fewer parameters than TransNet while delivering better performance
- Strong performance maintained across all compression ratios (η=1/4 to 1/64)
- Scalable variants offer flexible performance-complexity trade-offs

## Acknowledgments 

We thank the authors of:
- [ACRNet](https://github.com/Kylin9511/ACRNet)
- [CRNet](https://github.com/Kylin9511/CRNet)
- [CsiNet](https://github.com/sydney222/Python_CsiNet)

Special thanks to Chao-Kai Wen and Shi Jin's group for providing the preprocessed COST2100 dataset.

```
