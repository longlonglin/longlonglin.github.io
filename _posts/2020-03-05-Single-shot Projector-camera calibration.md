---
layout: project
title: A Fast and Flexible Projector-Camera Calibration System
author: Bingyao Huang
permalink: /single-shot-pro-cam-calib
published: true
teaser: https://raw.githubusercontent.com/BingyaoHuang/single-shot-pro-cam-calib/master/doc/reconstruct.png
---
#### Bingyao Huang, Ying Tang, Samed Ozdemir, and [Haibin Ling](https://www3.cs.stonybrook.edu/~hling)
#### [[IEEE T-ASE 2020 paper](/pub/ProCamCalib/)] [[ISMAR-Adjunct 2018 paper](https://arxiv.org/pdf/1803.09058.pdf)]  [[GitHub](https://github.com/BingyaoHuang/single-shot-pro-cam-calib)]

<p align="center"><img src="https://raw.githubusercontent.com/BingyaoHuang/single-shot-pro-cam-calib/master/doc/reconstruct.png" alt="procam-calib" width="80%"/></p>

## Abstract
Existing projector-camera calibration methods typically warp keypoints from a camera image to a projector image using estimated homographies, and often suffer from errors in camera parameters and noises due to imperfect planarity of the calibration target. This paper proposes a practical and robust projector-camera calibration system that explicitly deals with these challenges. Firstly, a graph-theory-based correspondence algorithm is built on top of a color-coded spatial structured light (SL) pattern. Such SL correspondences are then used for a coarse projector-camera calibration. To gain more robustness against noises from an imperfect planar calibration board, we develop a bundle adjustment algorithm to jointly optimize the estimated projector-camera parameters and the correspondences' coordinates. Moreover, our system requires only one shot of SL pattern for each calibration board pose, which is much more practical than multi-shot solutions. Comprehensive experimental validation is conducted on both synthetic and real datasets and our method clearly outperforms existing methods in all experiments. For the benefit of the society, a practical open source software with graphical user interface (GUI) of the developed system is publicly available at [[GitHub](https://github.com/BingyaoHuang/single-shot-pro-cam-calib)].

___
## Single-shot-per-pose
<p align="center"><img src="https://raw.githubusercontent.com/BingyaoHuang/single-shot-pro-cam-calib/master/doc/calib.gif" alt="calib" width="80%"/></p>

___
## Software video user guide
<!-- <p align="center"> -->
<div class="video_wrapper">
<div class="responsive-video">
<iframe width="80%" height="400px" src="https://www.youtube.com/embed/fnrVDOhcu7I?mute=1" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
</div>

___
## Related Work
* Bingyao Huang and Haibin Ling. **End-to-end Projector Photometric Compensation**. CVPR. 2019. [[Paper](http://openaccess.thecvf.com/content_CVPR_2019/papers/Huang_End-To-End_Projector_Photometric_Compensation_CVPR_2019_paper.pdf)]  [[Supp. material](https://www3.cs.stonybrook.edu/~hling/publication/CompenNet_sup.pdf)]  [[GitHub](https://github.com/BingyaoHuang/CompenNet)] [[Webpage]({{site.baseurl}}/compennet)]
* Bingyao Huang and Haibin Ling. **CompenNet++: End-to-end Full Projector Compensation**. ICCV. 2019. [[Paper](http://openaccess.thecvf.com/content_ICCV_2019/papers/Huang_CompenNet_End-to-End_Full_Projector_Compensation_ICCV_2019_paper.pdf)]  [[Supp. material](https://www3.cs.stonybrook.edu/~hling/publication/CompenNet++_sup-high-res.pdf)]  [[GitHub](https://github.com/BingyaoHuang/CompenNet-plusplus)] [[Webpage]({{site.baseurl}}/compennet++)]
* Daniel Moreno and Gabriel Taubin. **Simple, accurate, and robust projector-camera calibration**. 3DIMPVT. 2012. [[Paper](http://mesh.brown.edu/calibration/files/Simple%2C%20Accurate%2C%20and%20Robust%20Projector-Camera%20Calibration.pdf)] [[Webpage](http://mesh.brown.edu/calibration/)]

___