# Endorse Logo Detection POC

Testing with Corsair logo utilizing Tensorflow

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