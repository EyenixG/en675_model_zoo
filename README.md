
<img alt="Python" src ="https://img.shields.io/badge/python-3.8-orange"/>


## EN675 NPU Model Zoo
The EN675 Series SoC Model Zoo privides the trained models for AI Object Detection (OD) and Classification (CLS) applications.  
:rocket: EN675 NPU Spec Link : [EYENIX EN675 NPU Spec & Demo](https://resonant-duke-420.notion.site/EN675-AI-NPU-Solution-d407c17992d8447b9c98ac2bfede8cdb)
***
&#160;
### :star: Download
#### :arrow_forward: Object Detection
**classes** : Person, Bicycle, Motorbike, Car, Bus, Truck  
<figure>
    <img src="./img/6classes_image.PNG" title="6class">    
</figure>

|Model|ONNX|Compile Results|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|-|-|11MB|26ms|13ms|
|512_512_eyenix_model_v1|[512_512_eyenix_model_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9466030/512_512_eyenix_model_v1.zip)|[od6class_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9466035/od6class_512.zip)|18MB|37ms|20ms|
|640_640_eyenix_model_v1|[640_640_eyenix_model_v1.onnx](https://github.com/Eyenix/en675_model_zoo/files/9485742/640_640_eyenix_model_v1.zip)|[od6class_640.bin](https://github.com/Eyenix/en675_model_zoo/files/9485743/od6class_640.zip)|25MB|54ms|29ms|

&#160;

### To be updated later
**class** : Face  
<figure>
    <img src="./img/face_image.PNG" title="face">    
</figure>

|Model|ONNX|Compile Results|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|-|-|-|-|-|
|512_512_eyenix_model_v1|-|-|-|-|-|
|640_640_eyenix_model_v1|-|-|-|-|-|


&#160;

### :trophy: Performance
#### :arrow_forward: Object Detection
:+1: Train Dataset : PASCAL VOC 2007 (train, val), PASCAL VOC 2012 (train, val)  
:+1: Test Dataset : PASCAL VOC 2007 (test)
|Model|mAP at IOU = .50 (GPU)|mAP at IOU = .50 (NPU)| test file |
|:-----:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|75.2|-|-|
|512_512_eyenix_model_v1|78.2|-|-|
|640_640_eyenix_model_v1|79.4|-|-|

&#160;



### :clapper:promotion (DEMO)
#### :arrow_forward: Parking lot solution
![Parking_lot solution](https://user-images.githubusercontent.com/66294848/188069884-3441a15f-2a91-477a-b8d1-6337c931c25d.gif)

&#160;


[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FEyenix%2Fen675_model_zoo&count_bg=%2379C83D&title_bg=%23555555&icon=pytorch.svg&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
