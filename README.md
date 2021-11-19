# Endorse Logo Detection POC

Testing with Corsair logo utilizing Tensorflow Single Shot MultiBox Detector (SSD)

![](https://github.com/eugenechung81/endorse-logo-detection-poc/blob/master/frames/test5.0.jpg)

## Single Shot MultiBox Detector

  * Uses single deep neutral network (single shot detector), set default box over different aspect ratios and scales
  * Faster than other algos like COOCO, PASCAL VOC, YOLO, Faster R-CNN with good accuracy. 59 FPS at 75% accurancy.
  * SSD performs better on large objects vs smaller objects.
  * Need to have a negative to positive exmaples ratio of 3:1 (need to know what is negative detectio)
  * Features maps (conv1: edge + blob ) + conv 3: texture, conv5 : object parts, fc8: boject classes

## Training

Check file:
`1. Object_Detection_Training_and_Detection.ipynb`

OR

Model deployed on Google Collab for faster training
https://colab.research.google.com/drive/18i3wJnTMNY5_DtbSyYcVL_8rtrx59ykG#scrollTo=p1BVDWo7pfDC

### Training Images

Check following directory for images to train / test on: `Tensorflow/workspace/images`

### Labeling Images

Use labelImg in `Tensorflow/labelImg` to label test/train images.

### Models

Models are stored `Tensorflow/workspace/models` and `Tensorflow/workspace/pre-trained-models`

## Testing

Check file: 
`2. Test Object Detection Model.ipynb`

# Results
 
* 96% accuracy at 90% filter

```
  precision    recall  f1-score   support
         0.0       1.00      0.85      0.92      2866
         1.0       0.64      1.00      0.78       760

     precision    recall  f1-score   support
         0.0       0.00      0.00      0.00        27
         1.0       0.96      1.00      0.98       708
```

# Resources

* https://towardsdatascience.com/logo-detection-in-images-using-ssd-bcd3732e1776
* https://arxiv.org/pdf/1512.02325.pdf
* https://towardsdatascience.com/understanding-ssd-multibox-real-time-object-detection-in-deep-learning-495ef744fab
