# Faster R-CNN


## Environments Set Up：
* Python3.6/3.7/3.8
* Pytorch1.7.1
* pycocotools(Linux:`pip install pycocotools`; Windows:`pip install pycocotools-windows`
* Ubuntu or Centos
* Better to use GPU

## Structure：
```
  ├── backbone: Backbone network, which can be selected according to your requirements
  ├── network_files: Faster R-CNN网络（including modules such as Fast R-CNN as well as RPN）
  ├── train_utils: Training validation related modules (including cocotools)
  ├── my_dataset.py: Custom dataset for reading VOC datasets
  ├── train_mobilenet.py: Training with MobileNetV2 as backbone
  ├── train_resnet50_fpn.py: Training with resnet50+FPN as backbone
  ├── train_multi_GPU.py: For users with multiple GPUs
  ├── predict.py: Simple prediction script with trained weights for prediction testing
  ├── validation.py: Validate/test the COCO metrics of the data using the trained weights and generate record_mAP.txt
  └── pascal_voc_classes.json: pascal_voc labeled file
  └── Results: loss curve, mAP figure for the training process.
  └── outputs: logs.
  
```

## Pre-training weights download address（Download it and put it in the 'backbone' folder）：
* MobileNetV2 weights(Download it, rename it to `mobilenet_v2.pth`, and put it in the `bakcbone` folder.): https://download.pytorch.org/models/mobilenet_v2-b0353104.pth
* Resnet50 weights(Download it, rename it to `resnet50.pth` and put it in the `bakcbone` folder.): https://download.pytorch.org/models/resnet50-0676ba61.pth
* ResNet50+FPN weights: https://download.pytorch.org/models/fasterrcnn_resnet50_fpn_coco-258fb6c6.pth
* Note that the downloaded pre-training weights remember to be renamed.
 
 
## Datasets saved in  'VOCdekit' file:
* Images: VOCdekit->VOC2012->JPEGImages
* Labeled Files: VOCdekit->VOC2012->Annotations


