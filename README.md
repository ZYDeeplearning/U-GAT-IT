## U-GAT-IT &mdash; Official PyTorch Implementation(pycharm实现源码在Release中，可直接下载或者下载jupyter notebook文件在colab and kaggle)
### : Unsupervised Generative Attentional Networks with Adaptive Layer-Instance Normalization for Image-to-Image Translation

<div align="center">
  <img src="./assets/teaser.png">
</div>

### [Paper](https://arxiv.org/abs/1907.10830) | [Official Tensorflow code](https://github.com/taki0112/UGATIT)
The results of the paper came from the **Tensorflow code**


> **U-GAT-IT: Unsupervised Generative Attentional Networks with Adaptive Layer-Instance Normalization for Image-to-Image Translation**<br>
>
> **Abstract** *We propose a novel method for unsupervised image-to-image translation, which incorporates a new attention module and a new learnable normalization function in an end-to-end manner. The attention module guides our model to focus on more important regions distinguishing between source and target domains based on the attention map obtained by the auxiliary classifier. Unlike previous attention-based methods which cannot handle the geometric changes between domains, our model can translate both images requiring holistic changes and images requiring large shape changes. Moreover, our new AdaLIN (Adaptive Layer-Instance Normalization) function helps our attention-guided model to flexibly control the amount of change in shape and texture by learned parameters depending on datasets. Experimental results show the superiority of the proposed method compared to the existing state-of-the-art models with a fixed network architecture and hyper-parameters.*

## Usage
```
├── dataset
   └── YOUR_DATASET_NAME
       ├── trainA
           ├── xxx.jpg (name, format doesn't matter)
           ├── yyy.png
           └── ...
       ├── trainB
           ├── zzz.jpg
           ├── www.png
           └── ...
       ├── testA
           ├── aaa.jpg 
           ├── bbb.png
           └── ...
       └── testB
           ├── ccc.jpg 
           ├── ddd.png
           └── ...
```

### Train
```
> python main.py --dataset selfie2anime
```
* If the memory of gpu is **not sufficient**, set `--light` to True

### Test
```
> python main.py --dataset selfie2anime --phase test
```

## Architecture
![generator](https://user-images.githubusercontent.com/107866293/210135428-a7a7a8fd-7a2c-4995-aaa3-b8f6396a3433.png)
![discriminator](https://user-images.githubusercontent.com/107866293/210135434-c1a99e8e-3739-4569-864f-34a99d00d825.png)

## Results
### Ablation study
<img width="438" alt="ablation" src="https://user-images.githubusercontent.com/107866293/210135443-f329dd38-3da9-40e8-a1ca-6d0b856f687f.png">

### User study

<img width="738" alt="user_study" src="https://user-images.githubusercontent.com/107866293/210135439-9f5281b4-c50a-44e1-ba38-a9c0b96c33ed.png">


