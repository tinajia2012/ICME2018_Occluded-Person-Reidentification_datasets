# ICME2018_Occluded-Person-Reidentification_datasets
This project aims to release the datasets in the paper, [Occluded Person Re-identification](https://arxiv.org/abs/1804.02792), in ICME 2018. There would be a brief introduction to the paper and three datasets, Occluded-REID, P-DukeMTMC-reID and PETHZ as follows. Besides, another dataset in the paper, Partial-REID, is released by [Partial Person Re-identification](https://www.cv-foundation.org/openaccess/content_iccv_2015/html/Zheng_Partial_Person_Re-Identification_ICCV_2015_paper.html). 

## Introduction of Occluded Person Re-identification

### Abstract
Person re-identiﬁcation (re-id) suffers from a serious occlusion problem when applied to crowded public places. In this paper, we propose to retrieve a full-body person image by using a person image with occlusions. This differs signiﬁcantly from the conventional person re-id problem where it is assumed that person images are detected without any occlusion. We thus call this new problem the occluded person re-identitiﬁcation. To address this new problem, we proposea novel Attention Framework of Person Body (AFPB) based on deep learning, consisting of 1) an Occlusion Simulator (OS) which automatically generates artiﬁcial occlusions for fullbody person images, and 2) multi-task losses that force the neural network not only to discriminate a person’s identity but also to determine whether a sample is from the occluded data distribution or the full-body data distribution. Experiments on a new occluded person re-id dataset and three existing benchmarks modiﬁed to include full-body person images and occluded person images show the superiority of the proposed method. 
### Challenge
Occluded person re-id aims to  to search full-body person images given a person image with occlusions as a probe. The following figure shows the challenge, occlusion of person re-id. The left is that the original images in video surveillance; The middle is that occluded target persons detected by existing pedestrian detector; The right is that our goal is to retrieve a full-body person given a person with occlusions. Red bounding box means the same one, while the green means different ones.

![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/challenge.JPG)
 
### Framework
The overview of our approach is as follows. Given source images, we ﬁrstuseanOcclusionSimulatortogenerateartiﬁcialoccluded data and then we jointly encode the source data and occluded data to a CNN network with multi-task losses which discriminate a person’s identity as well as determining whether a sample is from the occluded data distribution or the source data distribution.

![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/framework.JPG)

### Experiment
We evaluate the proposed method on four datasets: Occluded-REID, Partial-REID, P-DukeMTMC-reID and PETHZ, each of which is organized into two parts: occluded person images and full-body person images.

#### visual experiment of AFPB
Examples of (a) raw occluded images, (b) occluded images with manual annotations of person body parts (c) saliency maps of the baseline network (d) saliency maps of the AFPB. The salient region reveals the part that the network representation focuses on. Our proposed, the AFPB pays more attention to person body parts without occlusions.

![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/result1.JPG)

#### Performance of AFPB framework
To evaluate the performance of our proposed Attention FrameworkofPersonBody(AFPB),we compare it with three networks: 1) the baseline network, ResNet-50 pretained on a large-scare person re-id dataset MARS, 2) the baseline network with the ﬁrst component of the AFPB, Occlusion Simulator, 3) the baseline network with the second component of the AFPB, multi-task losses, on four datasets, Occluded-REID, Partial-REID, P-DukeMTMC-reID and PETHZ.
 
![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/result2.JPG)

#### Comparison with the state-of-the-art

We compare our method with the state-of-the-art methods on the Occluded-REID dataset and Partial-REID dataset.
  
![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/result3.JPG)
  
## Occluded Person Re-id Datasets

In this paper, We evaluate the proposed method on four datasets: Occluded-REID, [Partial-REID](http://isee.sysu.edu.cn/files/resource/Partial-REID_Dataset.rar), P-DukeMTMC-reID and PETHZ, where we publish 3 new datasets for the occluded person re-identification task as follows.

### Occluded-REID dataset
Occluded-REID dataset is a new dataset captured by mobile camera equipments, which consists of 2000 images of 200 persons. Each identity has 5 full-body person images and 5 occluded person images with different types of severe occlusion. All images with different viewpoints and backgrounds are resized to 128×64.

### P-DukeMTMC-reID dataset
P-DukeMTMC-reID dataset is modiﬁed from [DukeMTMC-reID](http://vision.cs.duke.edu/DukeMTMC/) dataset. They contain several images with target persons occluded by different types of occlusion in public, e.g., peoples, luggages, cars, and guideboards. We select identities with both full-body person images and occluded person images. After the arrangement, there are 24143 images of 1299 identities in P-DukeMTMC-reID.

### P-ETHZ dataset
P-ETHZ dataset is selected from [ETHZ](http://homepages.dcc.ufmg.br/~william/datasets.html) dataset. ETHZ dataset is collecting images from multiple and moving cameras, which have considerable illumination variance, scale variance and occlusion. After the arrangement, there are 3897 images of 85 identities in P-ETHZ and each of identity has 1 to 30 full-body person images and occluded person images respectively.

Examples of datasets are as follows. Upper: occluded person images; Below: full-body person images.


![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/dataset.JPG)

## Citation

The Occluded-REID, P-DukeMTMC-reID and P-ETHZ datasets are for academic or educational use, but not for commercial use.
If our Occluded-REID, P-DukeMTMC-reID and P-ETHZ datasets facilitate your research, please cite our paper:
```cpp
@article{zhuo2018occluded,
  title={Occluded Person Re-identification},
  author={Zhuo, Jiaxuan and Chen, Zeyu and Lai, Jianhuang and Wang, Guangcong},
  journal={arXiv preprint arXiv:1804.02792},
  year={2018}
}
```
The right of final interpretation belongs to Prof. Lai’s research group, Sun Yat-Sen University.
## Contact

*stsljh@mail.sysu.edu.cn

*zhuojx5@mail2.sysu.edu.cn

*chenzy5@mail2.sysu.edu.cn

*wanggc3@mail2.sysu.edu.cn

## Reference
[1]Jiaxuan Zhuo, Zeyu Chen, Jianhuang Lai, Guangcong Wang. Occluded Person Re-Identification.2018 IEEE International Conference on Multimedia and Expo, ICME 2018, San Diego, CA, USA, July 23-27, 2018.

[2]W. S. Zheng, X. Li, T. Xiang, S. C. Liao, J. H. Lai, and S. G. Gong, “Partial person re-identiﬁcation,” in ICCV, 2015.

