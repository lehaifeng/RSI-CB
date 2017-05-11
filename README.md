# RSI-CB: A Large Scale Remote Sensing Image Classification Benchmark via Crowdsource Data
 
 * ### `Paper and benchmark will come soon`
 

 We propose a scalable remote sensing benchmark based on crowd source data, which can efficiently label the remote sensing image through the crowdsource data at hand.On the basis of this method, we construct a global scale large-scale remote sensing image classification database. 
 
There are six kinds of land category:`cultivated land `,` construction land and facilities`, `transportation and facilities`,` water area and facilities`, `woodland`, and `other land `, where each category has several subclasses. Considering the different depth of the convolution network for the image size requirements, we built a` 256 * 256` and `128 * 128` size of the two data sets, the former contains `35 categories` of objects, a total of more than `24,000 images`, the later contains `45 categories`,a total of more than `36,000 images`. 
 
Finally, We analyzed the image classification accuracy of several classical depth learning models such as AlexNet, VGGNet, GoogleNet, ResNet in RSI-CB, SAT-4, SAT-6, UC-Merced datasets and method of handcrafted features such as SIFT, CH, LBP, Gist to measure different performance on RSI-CB256 and UC-Merced，what's more,we have measured transfer performance of model trained by RSI-CB.All above showing that RSI-CB is more suitable as the model of the remote sensing image classification task, the result suggested that the model trained by the RSI-CB data has a good generalization ability and can be used in practical applications.

----
RSI-CB
====
## 1) Distribution of POI

According to the global distribution of OSM, we selected the cities such as `Beijing, Shanghai, New York and Washington, London ，Liverpool，Berlin,Tokyo,Paris,Toronto and other cities around the world`.Below are the visualization of POI distribution.<br>
         ![](https://github.com/wzx918/test/blob/master/osm%E5%88%86%E5%B8%83%E5%9B%BE.png)

----
## 2) Category hierarchy

According to the Chinese land classification standard and the ImageNet hierarchical grading mechanism, the common class between the Chinese land classification standard and the OSM category is selected as the priority object.
  ![](https://github.com/wzx918/test/blob/master/%E5%88%86%E5%B1%82%E5%88%86%E7%BA%A7.png)

-----
## 3) RSI-CB128&RSI-CB256

RSI-CB128 , containing 45 categories, about 36000 images, an average of 800 images per category; RSI-CB256,containing 35 categories,about 24000 images, an average of 690 images per category.`The benckmark will come sone`<br>  
                 ![](https://github.com/wzx918/test/blob/master/%E6%95%B0%E9%87%8F%E5%88%86%E5%B8%83.png)
                                   ![](https://github.com/wzx918/test/blob/master/128%E6%A0%B7%E6%9C%AC%E5%9B%BE.png)
                 
-----
Model
====
## 1)handcrafted features && deep convolution networks
We have used method of handcrafted features(eg, SIFT/CH/LBP/GIST) and deep convolution networks (eg AlxeNet/VGG16/GoogleNet /ResNet,`model can be downloaded` [here](https://1drv.ms/f/s!Auv9HKTH1GC9a-SqCjiPVgGpI-0) ) to test RSI-CB and the existing remote sensing image database (eg,UC-Merced / Sat-4 / Sat-6)) .Below are the precision contrast 
                 ![](https://github.com/wzx918/test/blob/master/%E4%BC%A0%E7%BB%9F%E6%96%B9%E6%B3%95%E7%BB%93%E6%9E%9C.png)
                     ![](https://github.com/wzx918/test/blob/master/dl%E6%96%B9%E6%B3%95%E7%BB%93%E6%9E%9C.png)
                    
----
## 2) capability of model transfer
In order to test the transfer ability of the RSI-CB training model, we selected the common 13 categories of the RSI-CB256 and UCM databases, with 100 images per category, and trained AlexNet-Conv3 with the rest RSI-CB256 of 13 categories , the experimental results show that RSI-CB training model has good transfer ability.
                      ![](https://github.com/wzx918/test/blob/master/%E8%BF%81%E7%A7%BB%E8%83%BD%E5%8A%9B%E6%B5%8B%E8%AF%95.png)
