# RSI-CB: A Large Scale Remote Sensing Image Classification Benchmark via Crowdsource Data
 
## The manuscript can be downloaded from https://www.mdpi.com/1424-8220/20/6/1594?type=check_update&version=2 or https://arxiv.org/abs/1705.10450 
 
(1).	We propose a crowdsource data-based method to build a RSI-CB. The crowdsource data in our method is a high-precision supervisor. Traditional methods require a significant amount of manual work; thus, they are less efficient and time-consuming. Using crowdsource data as a supervisor facilitates machine self-learning through the Internet. Moreover, the size of the benchmark sample could be infinite both in amount and variety. In addition, crowdsource data are basic data sources in the big data era and are updated rapidly. Therefore, the remote sensing benchmark constructed using crowdsource data can possibly continue to expand in terms of diversity, quantity, and robustness of samples. Consequently, our method can potentially realize weak unsupervised learning further for remote sensing image.

(2).	Based on the above method, we construct a global -scale RSI-CB. Considering the different image size requirements of the DCNN, we construct two datasets of 256 × 256 and 128 × 128 pixel sizes (RSI-CB256 and RSI-CB128, respectively) with 0.3–3-m spatial resolutions. The former contains 35 categories and more than 24,000 images. The latter contains 45 categories and more than 36,000 images. We establish a strict object category system according to the national standard of land-use classification in China and the hierarchical grading mechanism of ImageNet. The six categories are agricultural land, construction land and facilities, transportation and facilities, water and water conservancy facilities, woodland, and other land.

(3).	We conduct various experiments to compare RSI-CB with SAT-4, SAT-6, and UC-Merced datasets on handcrafted features, such as scale-invariant feature transform (SIFT), color histogram indexing (CH), local binary patterns (LBP), GIST, and classical DCNN models, such as AlexNet, VGGNet, GoogLeNet, and ResNet. In addition, we demonstrate that DCNN models trained by RSI-CB have good performance when transferred to other datasets, that is, UC-Merced, and good generalization ability. The experiments show that RSI-CB is a more suitable benchmark for remote sensing image classification than other benchmarks in the big data era, and has potential applications.

## Citation
If this repo is useful to your research, please kindly cite:

```
Li, H.; Dou, X.; Tao, C.; Wu, Z.; Chen, J.; Peng, J.; Deng, M.; Zhao, L. RSI-CB: A Large-Scale Remote Sensing Image Classification Benchmark Using Crowdsourced Data. Sensors 2020, 20, 1594. https://doi.org/10.3390/s20061594

Bibtex
@article{li2020RSI-CB,
    title={RSI-CB: A Large-Scale Remote Sensing Image Classification Benchmark Using Crowdsourced Data},
    author={Li, Haifeng and Dou, Xin and Tao, Chao and Wu, Zhixiang and Chen, Jie and Peng, Jian and Deng, Min and Zhao, Ling},
    journal={Sensors},
    DOI = {doi.org/10.3390/s20061594},
    year={2020},
    volume = {20},
    number = {6},
    pages = {1594},
    type = {Journal Article}
}

Endnote
%0 Journal Article
%A Li, Haifeng
%A Dou, Xin
%A Tao, Chao
%A Wu, Zhixiang
%A Chen, Jie
%A Peng, Jian
%A Deng, Min
%A Zhao, Ling
%D 2020
%T RSI-CB: A Large-Scale Remote Sensing Image Classification Benchmark Using Crowdsourced Data
%B Sensors
%V 20
%N 6
%P 1594
%R doi.org/10.3390/s20061594
%! RSI-CB
```

----
RSI-CB
====
* [RSI-CB256 can be downloaded here in OneDrive](https://1drv.ms/u/s!Am218i8VSQEBaTyXDc-zA56zPv4) or [here in BaiduYun](https://pan.baidu.com/s/1pLnZQ23)
* [RSI-CB128 can be downloaded here in OneDrive](https://1drv.ms/u/s!Auv9HKTH1GC9jBbv-XzBFyMegqlL) or [here in BaiduYun](https://pan.baidu.com/s/1bpIQ0IN)
## 1) Distribution of POI

According to the global distribution of OSM, we selected the cities such as `Beijing, Shanghai, New York and Washington, London ，Liverpool，Berlin,Tokyo,Paris,Toronto and other cities around the world`. The POI distribution was shown as following.<br>
<div align=center><img src="https://github.com/wzx918/test/blob/master/osm%E5%88%86%E5%B8%83%E5%9B%BE.png"/></div>

----
## 2) Category hierarchy

According to the Chinese land classification standard and the ImageNet hierarchical grading mechanism, the common class between the Chinese land classification standard and the OSM categories are selected as the priority object.
<div align=center><img src="https://github.com/wzx918/test/blob/master/%E5%88%86%E5%B1%82%E5%88%86%E7%BA%A7.png"/></div>

-----
## 3) RSI-CB128 & RSI-CB256

RSI-CB128 contains 45 categories, about 36000 images. There is an average of 800 images in each category; RSI-CB256 contains 35 categories,about 24000 images. There is an average of 690 images in each category.<br>  
<div align=center><img src="https://github.com/wzx918/test/blob/master/%E6%95%B0%E9%87%8F%E5%88%86%E5%B8%83.png"/></div>
<div align=center><img src="https://github.com/wzx918/test/blob/master/128%E6%A0%B7%E6%9C%AC%E5%9B%BE.png"/></div>
                              
-----
Models:
====
## 1) Handcrafted features && DCNNs
We used method of handcrafted features(eg, SIFT/CH/LBP/GIST) and DCNNs (e.g., AlxeNet/VGG16/GoogleNet/ResNet,[models can be downloaded here in OneDrive](https://1drv.ms/f/s!Auv9HKTH1GC9a-SqCjiPVgGpI-0) or [here in BaiduYun](https://pan.baidu.com/s/1gfcePUV) ) to test RSI-CB and other relatived banchmarks (e.g. UC-Merced / Sat-4 / Sat-6). The precision matrix was listed as following: 
<div align=center><img src="https://github.com/wzx918/test/blob/master/%E4%BC%A0%E7%BB%9F%E6%96%B9%E6%B3%95%E7%BB%93%E6%9E%9C.png"/></div>
<div align=center><img src="https://github.com/wzx918/test/blob/master/dl%E6%96%B9%E6%B3%95%E7%BB%93%E6%9E%9C.png"/></div>
                                   
----
## 2) Transfer capability 
In order to test the transfer ability of the RSI-CB training model, we choosed the common 13 categories of the RSI-CB256 and UCM databases, with 100 images per category, and trained AlexNet-Conv3 with the rest images of RSI-CB256 for the common 13 categories. Experimental results showed that models trained by RSI-CB had good transfer ability.
<div align=center><img src="https://github.com/wzx918/test/blob/master/%E8%BF%81%E7%A7%BB%E8%83%BD%E5%8A%9B%E6%B5%8B%E8%AF%95.png"/></div>
  
