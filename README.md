[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fziilk/tldi2_release/blob/dev/TLDI2.ipynb)
[![GitHub repo size](https://img.shields.io/github/repo-size/fziilk/tldi2_release)](https://github.com/fziilk/tldi2_release)
[![GitHub language count](https://img.shields.io/github/languages/count/fziilk/tldi2_release)](https://github.com/fziilk/tldi2_release)

# TLDI2: Tea Leaf Disease Identifier

TLDI2 is an Artificial Neural Network model, specifically a Convolutional Neural Network type. TLDI2 is the second version of the TLDI model, that have a lighter model size. The model's objective is to detect disease on tea leaf, thus aims to helping the tea production. 

## TLDI2 Models
The model itself have two versions and build for different purposes.

| Model         | Description                                                                                                                                                                            |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TLDI2 G2      | A custom built CNN model. Build for lightness, however less accurate compared to the _TLDI2 ResNet50_ model.                                                                             |
| TLDI ResNet50 | A CNN model built with transfer learning with a model base of the [ResNet50](https://in.mathworks.com/help/deeplearning/ref/resnet50.html). Build for accuracy, however heavy in size. |

### TLDI G2

#### _Architecture_:

<a href="https://github.com/fziilk/tldi2_release">
  <img src="https://raw.githubusercontent.com/fziilk/tldi2_release/master/tldi_g2.png" alt="TLDI2 G2 Architecture" width="1000" align="center"/>
</a>

#### _Evaluation Results_
```python
               precision    recall  f1-score   support

   algal_leaf       0.94      0.77      0.85        57
  anthracnose       0.63      0.84      0.72        50
bird_eye_spot       0.82      0.64      0.72        50
 brown_blight       0.85      0.93      0.89        57
   gray_light       0.84      0.74      0.79        50
      healthy       1.00      1.00      1.00        37
red_leaf_spot       1.00      0.82      0.90        72
   white_spot       0.69      0.86      0.76        71

     accuracy                           0.82       444
    macro avg       0.85      0.83      0.83       444
 weighted avg       0.84      0.82      0.82       444
```

### TLDIResNet50 

#### _Architecture_:

<a href="https://github.com/fziilk/tldi2_release">
  <img src="https://raw.githubusercontent.com/fziilk/tldi2_release/master/tldi_resnet50.png" alt="TLDI2 ResNet50 Architecture" width="500"/>
</a>


#### _Evaluation Results_:

```python
               precision    recall  f1-score   support

   algal_leaf       0.93      1.00      0.97        57
  anthracnose       0.90      0.94      0.92        50
bird_eye_spot       0.92      0.90      0.91        50
 brown_blight       0.98      0.88      0.93        57
   gray_light       0.96      0.94      0.95        50
      healthy       1.00      1.00      1.00        37
red_leaf_spot       0.99      1.00      0.99        72
   white_spot       0.92      0.93      0.92        71

     accuracy                           0.95       444
    macro avg       0.95      0.95      0.95       444
 weighted avg       0.95      0.95      0.95       444
```

## Installation

To install all versions of the TLDI2, please run the following script in the terminal.

```commandline
git clone --branch models git@github.com:fziilk/tldi2_release.git
```

## Getting Predictions

Visit the [evaluation notebook](https://colab.research.google.com/github/fziilk/tldi2_release/blob/eval/Evaluation_Report_TLDI2.ipynb) to see how to load and get predictions from both version of the TLDI model.
