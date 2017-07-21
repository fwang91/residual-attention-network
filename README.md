# Residual Attention Network
Residual Attention Network for Image Classification (**CVPR-2017 Spotlight**)

By Fei Wang, Mengqing Jiang, Chen Qian, Shuo Yang, Chen Li, Honggang Zhang, Xiaogang Wang, Xiaoou Tang


### Introduction
**Residual Attention Network** is a convolutional neural network using attention mechanism which can incorporate with state-of-the-art feed forward network architecture in an end-to-end training fashion.

**Residual Attention Networks** are described in the paper "Residual Attention Network for Image Classification"(https://arxiv.org/pdf/1704.06904.pdf).

This repository contains the prototxts of "Residual Attention Network". The trained model will be released soon. 

### Citation
If you find "Residual Attention Network" useful in your research, please cite:

	@article{wang2017residual,
  		title={Residual Attention Network for Image Classification},
  		author={Wang, Fei and Jiang, Mengqing and Qian, Chen and Yang, Shuo and Li, Cheng and Zhang, Honggang and Wang, Xiaogang and Tang, Xiaoou},
  		journal={arXiv preprint arXiv:1704.06904},
  		year={2017}	
	}

### Models
0. Attention-56 and Attention-92 are based on the pre-activation residual unit. 

1. According to the paper, we replace pre-activation residual unit with resnext unit to contruct the AttentionNeXt-56 and AttentionNeXt-92.



### Main Performance
0. Evaluation on ImageNet validation dataset.
|    Network       |Test Size|  top-1  |  top-5  |
|------------------|---------|---------|---------|
| Attention-56     | 224\*224|  21.76% |   5.9%  |
| AttentionNeXt-56 | 224\*224|  21.2%  |   5.6%  |
| Attention-92     | 320\*320|  19.5%  |   4.8%  |


### Note
0. We use Caffe ("https://github.com/buptwangfei/caffe") to train our Residual Attention Networks.

1. We follow the implementation of BN layer from "https://github.com/happynear/caffe-windows.git", which merge computations of mean, variance, scale and shift into one layer. We use moving average in the training stage.

3. The scale augmentation and ratio augmentation are used in the training process.

4. The mini-batch of per GPU should be at least 32 images. 

5. If you want to train Residual Attention Network, you should use my caffe code and add data augmentation described in the paper. I think it is easy to reproduce the performance on the ImageNet validation dataset.
