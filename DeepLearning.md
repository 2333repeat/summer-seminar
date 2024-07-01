# Summer Class
## 第一周  (2024.06.03 - 2024.06.09)
### 超分
#### 积分梯度与盲超分语义
积分梯度常用于神经网络解释性工作，数学推导较为简单。
##### Brief introduction of Integral Gradient  
- Axiomatic Attribution for Deep Networks (概览,可不看)
- https://zhuanlan.zhihu.com/p/468782348/ (可只看这个网站)
- https://pytorch.org/docs/stable/generated/torch.gradient.html (有tf代码以及可视化结果)
##### Attribution analysis on Blind Super-Resolution   
- SeD: Semantic-Aware Discriminator for Image Super-Resolution
##### Semantic Blind Super-Resolution   
- Finding Discriminative Filters for Specific Degradations in Blind Super-Resolution
### 对比学习
- InstDist: 
    - Unsupervised Feature Learning via Non-Parametric Instance Discrimination (CVPR 2018) 
    - 利用 memory bank 来存储图像经神经网络编码后的特征。
- InvaSpread: 
    - Unsupervised Embedding Learning via Invariant and Spreading Instance Feature (CVPR 2019)
    - 没有使用额外的数据结构去存储大量的样本信息；正负样本都来自于同一个 minibatch；使用同一个编码器进行端到端的学习。
- CPC: 
    - Representation Learning with Constrastive Predictive Coding (2018)
    - 可以应用于音频、图片、强化学习；将输入当成序列，利用前面的输入通过 RNN 或 LSTM 等网络输出来进行预测。

##  第二周  (2024.06.10 - 2024.06.16)
### 超分
#### 无监督计算机视觉
#### Unsupervised Super resolution
- CuNeRF: Cube-Based Neural Radiance Field for Zero-Shot Medical Image Arbitrary-Scale Super Resolution
##### Unsupervised Deraining
- Unsupervised Deraining: Where Asymmetric Contrastive Learning Meets Self-Similarity
### 图像分类
- 2012年：AlexNet
  - ImageNet Classification with Deep Convolutional Neural Networks
  - 深度卷积神经网络的ImageNet分类
- 2014年：VGG
    - Very Deep Convolutional Networksfor Large-Scale Image Recognition
    - 超深度卷积网络用于大规模图像识别
### 对比学习
- CMC：
    - Contrastive Multiview Coding（ECCV 2020）
    - 增大不同视角之间的互信息（视觉、听觉、触觉）
- SimCLR V2:
    - Big Self-Supervised Models are Strong Semi-Supervised Learners (NeurIPS 2020)
    - 使用更大的骨干网络模型; 增加 MLP层，实验测试两层最佳; 使用动量编码器，参考 MoCo
- SWaV:
    - Unsupervised Learning of Visual Features by Contrasting Cluster Assignments (NeurIPS 2020)
    - 生成多个视角，利用一个视角得到的特征去预测另一个视角的特征; 与聚类工作相结合，利用 聚类中心（3000个）进行预测; 提出 Muti-crop 的数据增强策略，多尺度的剪裁原始图像作为数据增强

##  第三周 (2024.06.17 - 2024.06.23)
### 图像分类
- 2015年：Batch Normalization
    - Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift
    - 批处理规范化：通过减少内部协变量偏移来加速深度网络训练
- 2015年：ResNet
    - Deep Residual Learning for Image Recognition
    - 深度残差学习用于图像识别

### 对比学习
- Moco V2:
    - Improved Baselines with Momentum Contrastive Learning (2020)
    - 借鉴 SimCLRv1 的策略，添加了MLP层，使用了数据增强，训练时使用 cos learning rate schedule
- Moco V3:
    - An Empirical Study of Training Self-Supervised Vision Transformers (ICCV 2021)
    - 结合 MoCov2 和 SimSiam; 骨干网络替换成了 ViT 
- BYOL:
    - Bootstrap Your Own Latent A New Approach to Self-Supervised Learning (NeurIPS 2020)
    - 结合了MOCO和SimCLR各自的优点; 并化繁为简; 无需负样本
- SimSiam:
    - Exploring Simple Siamese Representation Learning (CVPR 2021)
    - 较 BYOL 没有使用动量编码器进行参数更新; 无需负样本


## 第四周 (2024.07.01 - 2024.07.07 )
### 超分
#### 傅里叶特征
傅里叶特征是简单傅里叶变换的工程改进，此部分论文数学内容与主题关联较小，可在一定程度上忽略。
##### Brief introduction of Spectral Bias
- On the Spectral Bias of Neural Networks (概览,可不看)
##### Brief introduction of Fourier Features
- Fourier Features Let Networks Learn High Frequency Functions in Low Dimensional Domains (概览,可不看)
##### Fourier feature for continue super resolution
- Local Texture Estimator for Implicit Representation Function
### 对比学习
- DINO:
    - Emerging Properties in Self-Supervised Vision Transformers (ICCV 2021)
    - 融合 ViT 模型; 使用 student得到的结果去预测得到的结果
- CLIP:
    - Learning Transferable Visual Models From Natural Language Supervision (2021)
    - 模型训练采用了一个非常大的数据集; CLIP 预训练模型可以在不需要任何数据集训练的情况下和一个有监督学习的模型达成平手，甚至还会更高

### H100介绍
- 基于 NVIDIA GPU 加速的数据中心
- NVIDIA H100 GPU 架构深度解析
## 第五周 (2024.07.07 - 2024.07.14 )
### 超分
#### 跨领域整合的图像修复方法
##### LUTs and Image Restoration
- Toward DNN of LUTs: Learning Efficient Image Restoration with Multiple Look-Up Tables
##### Mamba and Image Restoration
- MambaIR: A Simple Baseline for Image Restoration with State-Space Model

