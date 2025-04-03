
<img alt="Python" src ="https://img.shields.io/badge/python-3.8-orange"/>


## EN675 NPU Model Zoo
The EN675 Series SoC Model Zoo privides the trained models for AI Object Detection (OD) and Classification (CLS) applications.  
:rocket: EN675 NPU Spec Link : [EYENIX EN675 NPU Spec & Demo](https://resonant-duke-420.notion.site/EN675-AI-NPU-Solution-d407c17992d8447b9c98ac2bfede8cdb)
***
&#160;
## New Release
### ⭐eyenix_model_v3 has been released⭐ 
eyenix_model_v3 performs better than eyenix_model_v2.  
eyenix_model_v3 is available from EN675_SDK_V1.15.00R
&#160;

## Release Model Download
### ▶ Object Detection
### **classes** : Person, Car, Motorbike, Bicycle, Truck, Bus  


|Model|Binary|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)| mAP|
|:-----:|:---:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|[od6class_320.bin](https://github.com/Eyenix/en675_model_zoo/files/9623476/od6class_320.zip)|[od6class_320.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812959/od6class_320.zip)|11MB|26ms|13ms| - |
|512_512_eyenix_model_v1|[od6class_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9466035/od6class_512.zip)|[od6class_512.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812963/od6class_512.zip)|18MB|37ms|20ms| - |
|640_640_eyenix_model_v1|[od6class_640.bin](https://github.com/Eyenix/en675_model_zoo/files/9485743/od6class_640.zip)|[od6class_640.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812969/od6class_640.zip)|25MB|54ms|29ms| - |
|672_384_eyenix_model_v2|[od6class_672_384.bin](https://github.com/Eyenix/en675_model_zoo/files/12459169/od6class_672_384.zip)|[od6class_672_384.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812971/od6class_672_384.zip)|22MB|63ms|28ms| [Click](#model---672x384-eyenix-model-v2-tiny) |
|672_384_eyenix_model_v3 (tiny) - release|[od6class_672_384_v3.bin](https://github.com/user-attachments/files/19480573/od6class_672_384_v3_bin.zip)|[od6class_672_384_v3.cfg](https://github.com/user-attachments/files/19480585/od6class_672_384_v3_cfg.zip)|30MB|-ms|-ms| [Click](#model---672x384-eyenix-model-v3-tiny---release) |
|672_384_eyenix_model_v3 (tiny) - update|[od6class_672_384_v3.bin](https://github.com/user-attachments/files/19480594/od6class_672_384_v3_bin.zip)|[od6class_672_384_v3.cfg](https://github.com/user-attachments/files/19480604/od6class_672_384_v3_cfg.zip)|30MB|-ms|-ms| [Click](#model---672x384-eyenix-model-v3-tiny---update) |
|864_512_eyenix_model_v3 (tiny) - update|[od6class_864_512.bin](https://github.com/user-attachments/files/19480608/od6class_864_512_bin.zip)|[od6class_864_512.cfg](https://github.com/user-attachments/files/19480610/od6class_864_512_cfg.zip)|44MB|-ms|-ms| [Click](#model---864x512-eyenix-model-v3-tiny---update) |


&#160;

### **class** : Face  


|Model|Binary|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)| mAP |
|:-----:|:---:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_face_v1|[face_320.bin](https://github.com/Eyenix/en675_model_zoo/files/9925058/face_320.zip)|[face_320.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813033/face_320.zip)|12MB|22ms|11ms| - |
|448_448_eyenix_model_face_v1|[face_448.bin](https://github.com/Eyenix/en675_model_zoo/files/9925059/face_448.zip)|[face_448.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813035/face_448.zip)|23MB|50ms|20ms| - |
|512_512_eyenix_model_face_v1|[face_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9925060/face_512.zip)|[face_512.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813036/face_512.zip)|31MB|68ms|28ms| - |  
|512_288_eyenix_model_face_v2|[face_512_288.bin](https://github.com/Eyenix/en675_model_zoo/files/12459171/face_512_288.zip)|[face_512_288.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813038/face_512_288.zip)|14MB|38ms|17ms| [Click](#model---512x288-eyenix-model-v2-tiny) |
|512_288_eyenix_model_face_v3 (tiny)|-|-|-MB|-ms|-ms| [Click](#model---512x288-eyenix-model-v3-tiny) |

**caution** : For the eyenix_face model_v1, the confidence score max is 64 instead of 256. User needs to change the value of the ClassConfTH array in npu_conf.c


&#160;

## 🏆 Performance
### ▶ Object Detection
### COCO (80classes) Model  
👍 Train Dataset : COCO 2017 (train)  
👍 Test Dataset : COCO 2017 (val)
|Model|Compile Results|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|640_640_eyenix_model_v3 (yolov5s_silu)|[yolov5s_silu.bin](https://github.com/user-attachments/files/19480519/yolov5s_silu.bin.zip)|[yolov5s_silu.cfg](https://github.com/user-attachments/files/19480521/yolov5s_silu.cfg.zip)|55.5MB|157.1ms|77.8ms|
|640_640_eyenix_model_v3 (yolov5s_relu6)|[yolov5s_relu6.bin](https://github.com/user-attachments/files/19480508/yolov5s_relu6.zip)|[yolov5s_relu6.cfg](https://github.com/user-attachments/files/19480514/yolov5s_relu6.zip)|53.8MB|114ms|65.1ms|
|640_640_eyenix_model_v3 (yolov7_tiny_silu)|[yolov7_tiny_silu.bin](https://github.com/user-attachments/files/19480501/yolov7_tiny_silu.zip)|[yolov7_tiny_silu.cfg](https://github.com/user-attachments/files/19480498/yolov7_tiny_silu.zip)|47MB|140.6ms|71.1ms|
|640_640_eyenix_model_v3 (yolov7_tiny_relu6)|[yolov7_tiny_relu6.bin](https://github.com/user-attachments/files/19480490/yolov7_tiny_relu6.zip)|[yolov7_tiny_relu6.cfg](https://github.com/user-attachments/files/19480495/yolov7_tiny_relu6.zip)|45.9MB|108.8ms|60.8ms|

&#160;

|Model|mAP at IOU = 0.50:0.95 (GPU)|mAP at IOU = 0.50:0.95 (NPU)| mAP at IOU = 0.50 (GPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|:---:|:---:|
|640_640_eyenix_model_v3 (yolov5s_silu)|39.3|35.2|58.6|54.7|
|640_640_eyenix_model_v3 (yolov5s_relu6)|38.1|34.8|57.6|54.4|
|640_640_eyenix_model_v3 (yolov7_tiny_silu)|39.1|34.8|57.8|53.9|
|640_640_eyenix_model_v3 (yolov7_tiny_relu6)|38.2|34.1|56.5|53.1|
|**640_640_eyenix_model_v3 (Large)**|47.6|**45.4**|66.6|**64.1**|

&#160;

👍 Train Dataset : Widerface (train)  
👍 Test Dataset : Widerface (val)
|Model|Compile Results|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|640_640_eyenix_model_v2 (yolov7_tiny_silu)|||MB|ms|ms|
|640_640_eyenix_model_v3 (yolov7_tiny_silu)|||MB|ms|ms|

&#160;

|Class|mAP at IOU = 0.50:0.95 (NPU)|mAP at IOU = 0.50 (NPU)|
|:-----:|:---:|:---:|
|640_640_eyenix_model_v2 (yolov7_tiny_silu)| - | - |
|640_640_eyenix_model_v3 (yolov7_tiny_silu)| - | - |

&#160;

## 🏆 Performance of released model
### ▶ 6 class Model  (**classes** : Person, Car, Motorbike, Bicycle, Truck, Bus  )

### Model - 672x384 eyenix model v2 (tiny)  

update ...

### Model - 672x384 eyenix model v3 (tiny) - release

update ...

### Model - 672x384 eyenix model v3 (tiny) - update

update ...

### Model - 864x512 eyenix model v3 (tiny) - update

update ...
&#160;

### ▶ Face Model (**class** : Face)

### Model - 512x288 eyenix model v2 (tiny)  

update ...

### Model - 512x288 eyenix model v3 (tiny)  

update ...

&#160;

## promotion (DEMO)
#### ▶ Parking lot solution
![Parking_lot solution](https://user-images.githubusercontent.com/66294848/188069884-3441a15f-2a91-477a-b8d1-6337c931c25d.gif)

&#160;
