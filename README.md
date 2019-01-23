# ICME2018_Occluded-Person-Reidentification_datasets
This project aims to release the datasets in the paper, [Occluded Person Re-identification](https://arxiv.org/abs/1804.02792), in ICME 2018. There would be a brief introduction to the paper and three datasets, Occluded-REID, P-DukeMTMC-reID and PETHZ as follows. Besides, another dataset in the paper, Partial-REID, is released by [Partial Person Re-identification](https://www.cv-foundation.org/openaccess/content_iccv_2015/html/Zheng_Partial_Person_Re-Identification_ICCV_2015_paper.html). 

## Introduction of Occluded Person Re-identification

### Abstract
Person re-identiﬁcation (re-id) suffers from a serious occlusion problem when applied to crowded public places. In this paper, we propose to retrieve a full-body person image by using a person image with occlusions. This differs signiﬁcantly from the conventional person re-id problem where it is assumed that person images are detected without any occlusion. We thus call this new problem the occluded person re-identitiﬁcation. To address this new problem, we proposea novel Attention Framework of Person Body (AFPB) based on deep learning, consisting of 1) an Occlusion Simulator (OS) which automatically generates artiﬁcial occlusions for fullbody person images, and 2) multi-task losses that force the neural network not only to discriminate a person’s identity but also to determine whether a sample is from the occluded data distribution or the full-body data distribution. Experiments on a new occluded person re-id dataset and three existing benchmarks modiﬁed to include full-body person images and occluded person images show the superiority of the proposed method. 
### Challenge
Occluded person re-id aims to  to search full-body person images given a person image with occlusions as a probe. The following figure shows the challenge, occlusion of person re-id. The left is that the original images in video surveillance; The middle is that occluded target persons detected by existing pedestrian detector; The right is that our goal is to retrieve a full-body person given a person with occlusions. Red bounding box means the same one, while the green means different ones.

![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/challenge.JPG)
 
### Framework
The overview of our approach is as follows. Given source images, we ﬁrstuseanOcclusionSimulatortogenerateartiﬁcialoccluded data and then we jointly encode the source data and occluded datatoaCNNnetworkwithmulti-tasklosseswhichdiscriminateaperson’sidentityaswellasdeterminingwhetherasample is from the occluded data distribution or the source data distribution.

![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/framework.JPG)

### Experiment
We evaluate the proposed method on four datasets: Occluded-REID, Partial-REID, P-DukeMTMC-reID and PETHZ, each of which is organized into two parts: occluded person images and full-body person images.

#### visual experiment of AFPB
Examples of (a) raw occluded images, (b) occluded images with manual annotations of person body parts (c) saliency maps of the baseline network (d) saliency maps of the AFPB. The salient region reveals the part that the network representation focuses on. Our proposed, the AFPB pays more attention to person body parts without occlusions.

![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/result1.JPG)


 
![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/result2.JPG)
  
![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/result3.JPG)
 

All the datasets are only allowed for non-commercial purposes.  If these datasets are used for research, please refer to the corresponding paper. 
This is the page for our paper Occluded Person Re-identification, to be appeared in ICME 2018. We are the first to propose the occluded person re-id task, as is illustrated below. 

## Occluded Person Re-id Datasets

![image](https://github.com/tinajia2012/ICME2018_Occluded-Person-Reidentification_datasets/raw/master/image/dataset.JPG)

