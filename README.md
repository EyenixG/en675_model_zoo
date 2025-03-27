
<img alt="Python" src ="https://img.shields.io/badge/python-3.8-orange"/>


## EN675 NPU Model Zoo
The EN675 Series SoC Model Zoo privides the trained models for AI Object Detection (OD) and Classification (CLS) applications.  
:rocket: EN675 NPU Spec Link : [EYENIX EN675 NPU Spec & Demo](https://resonant-duke-420.notion.site/EN675-AI-NPU-Solution-d407c17992d8447b9c98ac2bfede8cdb)
***
&#160;
## New Release
### ⭐eyenix_model_v3 has been released⭐ 
eyenix_model_v3 performs better than eyenix_model_v2.  
eyenix_model_v3 is available from EN675_SDK_V1.15.00R, which will be released later.  
&#160;
## Download
### ▶ Object Detection
### **classes** : Person, Car, Motorbike, Bicycle, Truck, Bus  


|Model|Binary|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)| mAP|
|:-----:|:---:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|[od6class_320.bin](https://github.com/Eyenix/en675_model_zoo/files/9623476/od6class_320.zip)|[od6class_320.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812959/od6class_320.zip)|11MB|26ms|13ms| - |
|512_512_eyenix_model_v1|[od6class_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9466035/od6class_512.zip)|[od6class_512.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812963/od6class_512.zip)|18MB|37ms|20ms| - |
|640_640_eyenix_model_v1|[od6class_640.bin](https://github.com/Eyenix/en675_model_zoo/files/9485743/od6class_640.zip)|[od6class_640.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812969/od6class_640.zip)|25MB|54ms|29ms| - |
|672_384_eyenix_model_v2|[od6class_672_384.bin](https://github.com/Eyenix/en675_model_zoo/files/12459169/od6class_672_384.zip)|[od6class_672_384.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812971/od6class_672_384.zip)|22MB|63ms|28ms| [Click](#model---672x384-eyenix-model-v2-tiny) |
|672_384_eyenix_model_v3 (tiny)|-|-|-MB|-ms|-ms| [Click](#model---672x384-eyenix-model-v3-tiny) |


&#160;

### **class** : Face  


|Model|Binary|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)| mAP |
|:-----:|:---:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_face_v1|[face_320.bin](https://github.com/Eyenix/en675_model_zoo/files/9925058/face_320.zip)|[face_320.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813033/face_320.zip)|12MB|22ms|11ms| - |
|448_448_eyenix_model_face_v1|[face_448.bin](https://github.com/Eyenix/en675_model_zoo/files/9925059/face_448.zip)|[face_448.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813035/face_448.zip)|23MB|50ms|20ms| - |
|512_512_eyenix_model_face_v1|[face_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9925060/face_512.zip)|[face_512.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813036/face_512.zip)|31MB|68ms|28ms| - |  
|512_288_eyenix_model_face_v2|[face_512_288.bin](https://github.com/Eyenix/en675_model_zoo/files/12459171/face_512_288.zip)|[face_512_288.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813038/face_512_288.zip)|14MB|38ms|17ms| [Click](#model---512x288-eyenix-model-v2-tiny) |
|672_384_eyenix_model_face_v3 (tiny)|-|-|-MB|-ms|-ms| [Click](#model---512x288-eyenix-model-v3-tiny) | 
|512_288_eyenix_model_face_v3 (tiny)|-|-|-MB|-ms|-ms| [Click](#model---672x384-eyenix-model-v3-tiny-1) |

**caution** : For the eyenix_face model_v1, the confidence score max is 64 instead of 256. User needs to change the value of the ClassConfTH array in npu_conf.c

&#160;

### **class** : COCO 80 Class  

|Model|Compile Results|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|640_640_eyenix_model_v2 (tiny)|-|-|36MB|-ms|-ms|
|640_640_eyenix_model_v3 (tiny)|-|-|41MB|-ms|-ms|


&#160;

## 🏆 Performance
### ▶ Object Detection
### COCO (80classes) Model  
👍 Train Dataset : COCO 2017 (train)  
👍 Test Dataset : COCO 2017 (val)
|Model|mAP at IOU = 0.50:0.95 (GPU)|mAP at IOU = 0.50:0.95 (NPU)| mAP at IOU = 0.50 (GPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|:---:|:---:|
|640_352_eyenix_model_v2 (tiny)|33.4|27.5|49.9|44.9|
|832_480_eyenix_model_v2 (tiny)|36.9|29.1|54.8|48.2|
|640_640_eyenix_model_v3 (tiny)|37.2|36.1|55.3|53.7|
|**640_640_eyenix_model_v3 (Large)**|47.6|**45.4**|66.6|**64.1**|

&#160;

### 6 class Model  
**classes** : Person, Car, Motorbike, Bicycle, Truck, Bus  


👍 Train Dataset : EYENIX OD6class DB (train)  
👍 Test Dataset : COCO 2017 (val)

### Model - 672x384 eyenix model v2 (tiny)  

|Class|mAP at IOU = 0.50:0.95 (NPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|
|**ALL**|30.4|53.3|
|Person|42.2|74.0|
|Car|31.5|57.4|
|Motorcycle|30.5|60.7|
|Bicycle|14.9|29.4|
|Truck|19.4|34.6|
|Bus|44.2|63.7|

### Model - 672x384 eyenix model v3 (tiny)

|Class|mAP at IOU = 0.50:0.95 (NPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|
|**ALL**| 39.9 | 62.1 |
|Person| 48.3 | 76.5 |
|Car| 38.4 | 62.7 |
|Motorcycle| 39.6 | 68.5 |
|Bicycle| 25.6 | 46.1 |
|Truck| 27.4 | 42.6 |
|Bus|60.0 | 76.5 | 

&#160;

### Face Model 
**class** : Face  

👍 Train Dataset : EYENIX FACE DB (train)  
👍 Test Dataset : WIDER FACE (EASY)

### Model - 512x288 eyenix model v2 (tiny)  

|Class|mAP at IOU = 0.50:0.95 (NPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|
|**Face**| - | - |

### Model - 512x288 eyenix model v3 (tiny)  

|Class|mAP at IOU = 0.50:0.95 (NPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|
|**Face**| - | - |

### Model - 672x384 eyenix model v3 (tiny)  

|Class|mAP at IOU = 0.50:0.95 (NPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|
|**Face**| - | - |

&#160;

## :clapper:promotion (DEMO)
#### :arrow_forward: Parking lot solution
![Parking_lot solution](https://user-images.githubusercontent.com/66294848/188069884-3441a15f-2a91-477a-b8d1-6337c931c25d.gif)

&#160;


[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FEyenix%2Fen675_model_zoo&count_bg=%2379C83D&title_bg=%23555555&icon=pytorch.svg&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
