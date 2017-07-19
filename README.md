# AttentionNet
Residual Attention Network for Image Classification (**CVPR-2017 Spotlight**)

By Fei Wang, Mengqing Jiang, Chen Qian, Shuo Yang, Chen Li, Honggang Zhang, Xiaogang Wang, Xiaoou Tang


### Introduction
**Residual Attention Network** is a convolutional neural network using attention mechanism which can incorporate with state-of-the-art feed forward network architecture in an end-to-end training fashion.

**Residual Attention Networks** are described in the paper "Residual Attention Network for Image Classification"(https://arxiv.org/pdf/1704.06904.pdf).

This repository contains Residual Attention Network prototxts. The trained model will be released soon. 

### Citation
If you find Residual Attention Network useful in your research, please cite:

	@article{wang2017residual,
  		title={Residual Attention Network for Image Classification},
  		author={Wang, Fei and Jiang, Mengqing and Qian, Chen and Yang, Shuo and Li, Cheng and Zhang, Honggang and Wang, Xiaogang and Tang, Xiaoou},
  		journal={arXiv preprint arXiv:1704.06904},
  		year={2017}	
	}

### Main Performance

|    Network       |Test Size|  top-1  |  top-5  |
|------------------|---------|---------|---------|
| Attention-56     | 224\*224|  21.76% |   5.9%  |
| AttentionNeXt-56 | 224\*224|  21.2%  |   5.6%  |
| Attention-92     | 320\*320|  19.5%  |   4.8%  |


### Note
0. We train our models using caffe("https://github.com/buptwangfei/caffe")

1. We refer to "https://github.com/happynear/caffe-windows.git" to implement BN layer which merge computations of "mean" "variance" and "scale" "shift" into one layer. We use moving average in the training stage.

3. The scale augmentation and ratio augmentation are used in the training process.

4. If you want to train Residual Attention Network, you should use my caffe code and add data augmentation described in the paper. I think it is easy to reproduce the performance on the ImageNet validation dataset.


