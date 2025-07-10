# **Rock Painting Detection**

This project implements object detection models to identify rock art paintings. Two models were trained: **Faster R-CNN** and **YOLOv5**. Each one was first trained to detect rock painting, then extended to differentiate between paintings depicting humans and animals. For the **YOLOv5** model, a petroglyph pretrained model from [ekohrt/petroglyph-detection](https://github.com/ekohrt/petroglyph-detection) was also used as base weights for the single class model.

The dataset was created by merging and cleaning images from Roboflow projects:

* [Rock Painting](https://universe.roboflow.com/food-annotation/rock-painting)

* [RFR](https://universe.roboflow.com/nico-jejov/rfr-ibkvz-wmt59)

Annotations were modified and images unrelated to rock paintings were removed. The final dataset for 
single class can be found [here](https://universe.roboflow.com/nico-jejov/rock-painting-single-class/dataset/2) and 
for the human and animal classes [here](https://universe.roboflow.com/nico-jejov/rock-painting-double-class/dataset/2)
