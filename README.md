## Fine Tuning CNNs on the Oxford Flowers Dataset

This notebook demonstrates how to fine tune resnet50 convolutional neural networks on the Oxford Flowers dataset. The dataset has large variations in light, scale, and pose, and only has 8K examples. 
This makes it difficult to learn the trends in the dataset without pretraining or data augmentation.

In this notebook, we fine-tune a resnet50 model from the [original paper](https://arxiv.org/abs/1512.03385) pretrained on ImageNet1k. We use the [TrivialAugment](https://openaccess.thecvf.com/content/ICCV2021/papers/Muller_TrivialAugment_Tuning-Free_Yet_State-of-the-Art_Data_Augmentation_ICCV_2021_paper.pdf)
data augmentation method to improve our model's generalization, and achieve a test accuracy of 96.0%. 

To obtain better results, we turn to broader pretraining, and use the resnet50 model from [Big Transfer (BiT): General Visual Representation Learning](https://arxiv.org/pdf/1912.11370.pdf). This model was pretrained on the larger ImageNet21k 
dataset, and accordingly shows a better test accuracy of 98.2% after fine tuning. 
