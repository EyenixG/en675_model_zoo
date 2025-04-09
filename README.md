
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


|Model|Binary|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_v1|[od6class_320.bin](https://github.com/Eyenix/en675_model_zoo/files/9623476/od6class_320.zip)|[od6class_320.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812959/od6class_320.zip)|11MB|26ms|13ms|
|512_512_eyenix_model_v1|[od6class_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9466035/od6class_512.zip)|[od6class_512.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812963/od6class_512.zip)|18MB|37ms|20ms|
|640_640_eyenix_model_v1|[od6class_640.bin](https://github.com/Eyenix/en675_model_zoo/files/9485743/od6class_640.zip)|[od6class_640.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812969/od6class_640.zip)|25MB|54ms|29ms|
|672_384_eyenix_model_v2|[od6class_672_384.bin](https://github.com/Eyenix/en675_model_zoo/files/12459169/od6class_672_384.zip)|[od6class_672_384.cfg](https://github.com/Eyenix/en675_model_zoo/files/12812971/od6class_672_384.zip)|22MB|63ms|28ms|
|672_384_eyenix_model_v3 (tiny) - release|[od6class_672_384_v3.bin](https://github.com/user-attachments/files/19480573/od6class_672_384_v3_bin.zip)|[od6class_672_384_v3.cfg](https://github.com/user-attachments/files/19480585/od6class_672_384_v3_cfg.zip)|30MB|80ms|39ms|
|672_384_eyenix_model_v3 (tiny) - update|[od6class_672_384_v3.bin](https://github.com/user-attachments/files/19480594/od6class_672_384_v3_bin.zip)|[od6class_672_384_v3.cfg](https://github.com/user-attachments/files/19480604/od6class_672_384_v3_cfg.zip)|30MB|80ms|39ms|
|864_512_eyenix_model_v3 (tiny) - update|[od6class_864_512.bin](https://github.com/user-attachments/files/19480608/od6class_864_512_bin.zip)|[od6class_864_512.cfg](https://github.com/user-attachments/files/19480610/od6class_864_512_cfg.zip)|46MB|131ms|60ms|


&#160;

### **class** : Face  


|Model|Binary|Cfg|Total DRAM Size|Inference Speed (Standard)|Inference Speed (Boost)|
|:-----:|:---:|:---:|:---:|:---:|:---:|
|320_320_eyenix_model_face_v1|[face_320.bin](https://github.com/Eyenix/en675_model_zoo/files/9925058/face_320.zip)|[face_320.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813033/face_320.zip)|12MB|22ms|11ms|
|448_448_eyenix_model_face_v1|[face_448.bin](https://github.com/Eyenix/en675_model_zoo/files/9925059/face_448.zip)|[face_448.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813035/face_448.zip)|23MB|50ms|20ms|
|512_512_eyenix_model_face_v1|[face_512.bin](https://github.com/Eyenix/en675_model_zoo/files/9925060/face_512.zip)|[face_512.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813036/face_512.zip)|31MB|68ms|28ms|
|512_288_eyenix_model_face_v2|[face_512_288.bin](https://github.com/Eyenix/en675_model_zoo/files/12459171/face_512_288.zip)|[face_512_288.cfg](https://github.com/Eyenix/en675_model_zoo/files/12813038/face_512_288.zip)|14MB|38ms|17ms|
|512_288_eyenix_model_face_v3 (tiny)|[face_512_288_v3.bin](https://github.com/user-attachments/files/19483493/face_512_288_v3_bin.zip)|[face_512_288_v3.cfg](https://github.com/user-attachments/files/19483497/face_512_288_v3_cfg.zip)|21MB|-ms|-ms|

**caution** : For the eyenix_face model_v1, the confidence score max is 64 instead of 256. User needs to change the value of the ClassConfTH array in npu_conf.c


&#160;


## 🏆 Performance of released model
### ▶ 6 class Model  (**classes** : Person, Car, Motorbike, Bicycle, Truck, Bus  )
* Boxes covering more than 15% of the total area have been removed

### Model - 320x320 eyenix model v1  
<img src="https://github.com/user-attachments/assets/899af614-a71a-439f-9d84-dee2ce8aa251" width="500"/>
<img src="https://github.com/user-attachments/assets/ee5a96bb-082b-41bd-8a25-b5ce878b2e43" width="500"/>

### Model - 512x512 eyenix model v1  
<img src="https://github.com/user-attachments/assets/0b2759fd-9560-4845-9223-f623fd722d0c" width="500"/>
<img src="https://github.com/user-attachments/assets/d16004b8-d40a-4724-8df4-6128170cdd91" width="500"/>

### Model - 640x640 eyenix model v1  
<img src="https://github.com/user-attachments/assets/7f493a2a-de84-49cf-8d13-d31b9bd31104" width="500"/>
<img src="https://github.com/user-attachments/assets/047ca093-57de-40b6-bd33-fd8ba8aba54f" width="500"/>

### Model - 672x384 eyenix model v2 (tiny)  
<img src="https://github.com/user-attachments/assets/b3d5a2b8-710e-4d79-9068-6e0730691dcf" width="500"/>
<img src="https://github.com/user-attachments/assets/ed533c29-82d3-434e-8f7b-d65979c0e477" width="500"/>

### Model - 672x384 eyenix model v3 (tiny) - release
<img src="https://github.com/user-attachments/assets/51fe8ebb-11e0-4a50-a491-3f6cd86f309b" width="500"/>
<img src="https://github.com/user-attachments/assets/09b1f1d0-1cb1-441c-8529-fb60206aa4e7" width="500"/>

### Model - 672x384 eyenix model v3 (tiny) - update
<img src="https://github.com/user-attachments/assets/5d05a76d-6e63-444d-9f6e-088de44e764c" width="500"/>
<img src="https://github.com/user-attachments/assets/77724a8a-7bfe-4e6b-add3-ba3b997b620f" width="500"/>

### Model - 864x512 eyenix model v3 (tiny) - update
<img src="https://github.com/user-attachments/assets/5f166ff1-5ba3-48f7-a8b0-4d9efa282de7" width="500"/>
<img src="https://github.com/user-attachments/assets/71ca8f5e-1fb4-4cbe-b1f0-6039a50e8081" width="500"/>


&#160;

### ▶ Face Model (**class** : Face)

### Model - 512x288 eyenix model v2 (tiny)  

update ...

### Model - 512x288 eyenix model v3 (tiny)  

update ...

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
|640_640_eyenix_model_v3 (yolov5s_silu)|39.3|36.0|58.6|55.1|
|640_640_eyenix_model_v3 (yolov5s_relu6)|38.1|35.2|57.6|54.4|
|640_640_eyenix_model_v3 (yolov7_tiny_silu)|39.1|35.1|57.8|54.0|
|640_640_eyenix_model_v3 (yolov7_tiny_relu6)|38.2|34.6|56.5|53.3|
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

## promotion (DEMO)
#### ▶ Parking lot solution
![Parking_lot solution](https://user-images.githubusercontent.com/66294848/188069884-3441a15f-2a91-477a-b8d1-6337c931c25d.gif)

&#160;
