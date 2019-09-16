# Design of an Object Detector Using Lattice-Type DenseNets

This website opens to anyone who wants to apply our proposed network. Since we are still submitting to ICRA 2020, the whole codes are not allowed but can be downloaded for our proposed trained models.

Our code is based on the [DSOD](https://github.com/szq0214/DSOD) framework.

## Introduction

We propose a new network architecture employing lattice-type DenseNets for object detection without using any pre-trained model. The proposed network can make more abundant feature maps than the conventional DenseNets as it develops feature maps in two different paths. In order to increase diversity and avoid  the problem of overlapping features, we augment  a ResNet in one of the paths. There are three dense blocks in our network, and each dense block includes a single lattice-type DenseNet. We reduce the structure of the original DenseNets to the same size as our networks to make a rapid comparison. Experiments are performed with the PASCAL VOC 2007 dataset, where our proposed architecture shows mAP improvement of approximately 2.1% relative to the reduced version of DSOD on an object detection task.

<div align=center>
<img src="https://user-images.githubusercontent.com/29120209/49847894-c359a300-fe15-11e8-8df1-c2d37c8a59b3.png">
</div>

## Results & Models
Our results are shown in the below table. We experiment using PASCAL VOC 2007 dataset.
You can download our model from below link.

| Method | # dense blocks | growth rate | mAP | processing time | Models
|:-------|:-------|:-------|:-------|:-------|:-------|
rDSOD  	| 6/8/8   | 32 | 65.5% | 2.36 days | [DSOD reference](https://drive.google.com/open?id=1cqPipKeSsosgawNQzI4Ejebqgcx2mABr)    |
LTDN	| 6/8/8   | 32 | 67.6% | 4.07 days | [Lattice reference](https://drive.google.com/open?id=17KMvCBxemBsKQ5F3ICsnOufE5xa671SZ) |
LTDN	| 3/4/4   | 32 | 62.9% | 2.31 days | [Lattice model_32](https://drive.google.com/open?id=1YwyJnJVPVNorwJ-JaUQ_TAu0bgttSQ0B)  |
LTDN	| 3/4/4   | 48 | 65.2% | 2.54 days | [Lattice model_48](https://drive.google.com/open?id=1DfBzkRH4d6hGLyJd2ORb5l9seKpFYAX_)  |
LTDN	| 3/4/4   | 64 | 66.7% | 2.85 days | [Lattice model_64](https://drive.google.com/open?id=1taRuglBciz8eNvheURfgjD42useW3Jnx)  |

## Examples
Examples of object detection results on the PASCAL VOC 2007 using the proposed LTDN.
<div align=center>
<img src="https://user-images.githubusercontent.com/29120209/49847915-d1a7bf00-fe15-11e8-93f1-8792765b6c52.png">
</div>
 

It also operates well in video. (click the image)

<a href="https://www.youtube.com/watch?v=mXzZJaABH4c">
<img src="https://user-images.githubusercontent.com/29120209/49853303-0d4c8400-fe2a-11e8-8a59-349a5d8ccddb.png" 
alt="IMAGE ALT TEXT HERE" width="640" height="360" border="10" /></a>
</div>



## Testing
- Install DSOD (https://github.com/szq0214/DSOD) and execute without any errors.

(You will need to install [CAFFE](https://github.com/BVLC/caffe) and [SSD](https://github.com/weiliu89/caffe/tree/ssd).)

- Create a subfolder `lattice` under `example/`, add files `lattice_detection_demo.py` to the folder `example/dsod/`.

(We can not share our code yet. We will share it after the revewinig.)

- Run a demo:
  ```shell
  python examples/lattice/lattice_detection_demo.py
  ```
(You should change the path or model name in the code.)

## Contact
Sang Un Park (undol26@kaist.ac.kr)
