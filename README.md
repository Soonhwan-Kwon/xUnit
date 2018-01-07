# xUnit
Learning a Spatial Activation Function for Efficient Image Restoration.

<p align="center">
  <img width="495" height="396" src="/figures/figure1.png">
</p>

Please refer our [paper](https://arxiv.org/abs/1711.06445) for more details.


# Dependencies
- python (tested with 3.5)
- PyTorch >= 0.2.0
- [PyINN](https://github.com/szagoruyko/pyinn)


# Code
Clone this repository into any place you want.

	git clone https://github.com/kligvasser/xUnit
	cd xUnit


# Results
### Gaussian Denoising

The average PSNR in [dB] attained by several state of the art denoising algorithms on the BSD68:

| Methods | BM3D | WNNM | EPLL | MLP | DnCNN-S | xDnCNN |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| # Parameters | - | - | - | - | 555K | **303K** |
|      σ=25    | 28.56 | 28.82 | 28.68 | 28.95 | **29.22** | 29.21 |
|      σ=50    | 25.62 | 25.87 | 25.67 | 26.01 | 26.23 | **26.26** |


### Single Image Super Resolution

The average PSNR in [dB] attained in the task of 3× and 4× SR on datasets Set5, Set14 and BSD100:

| Dataset | Scale | SRCNN (57K) | xSRCNN-c (44K)| xSRCNN-f (**32K**)|
| :---: | :---: | :---: | :---: | :---: |
| Set14 | 3× | 29.29 | 29.45 | **29.47** |
|       | 4× | 27.49 | 27.72 | **27.76** |
| BSD100 | 3× | 28.41 | **28.54** | 28.53 |
|        | 4× | 26.90 | 27.04 | **27.06** |
