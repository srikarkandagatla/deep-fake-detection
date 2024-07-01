# deep-fake-detection
Enhancing Deep Fake Detection In Multimedia: A Fusion of CNN and RNN Approaches

## About Repository
Within this repository, you'll discover three notebooks: "Deep Fake Detection on Images," "Deep Fake Detection on Images (XCEPTION)," and "Deep Fake Detection on Videos."

## About Datasets
The dataset utilized for "Deep Fake Detection on Images" and "Deep Fake Detection on Images (XCEPTION)" can be accessed at the following [link](https://www.kaggle.com/datasets/dagnelies/deepfake-faces).

Regarding the dataset used for image detection, it comprises two main components - a metadata CSV file and a folder named "faces_224." The metadata.csv file provides detailed information about each image found in the "faces_224" folder, specifying whether an image is categorized as "Real" or "Fake." The "videoname" column in the metadata file corresponds to the names of images within the "faces_224" folder, while the "label" column designates the class of each image, either "Fake" or "Real."

## Deep Fake Detection on Images, Deep Fake Detection on Images(XCEPTION)
A Convolutional Neural Network (CNN) model is created for false media detection, specifically applied to images. The initial CNN model achieved an accuracy of approximately 50.13% on the validation dataset. To enhance accuracy, transfer learning is employed, incorporating the Xception Model pre-trained on the "ImageNet" dataset. The Xception Model, with 71 layers, is fine-tuned, culminating in a validation accuracy of 65.93%.

## Deep Fake Detection on Videos
A Recurrent Neural Network (RNN) with Inception_v3 transfer learning is implemented to expand the detection capabilities to videos. The dataset comprises interview videos of celebrities sourced from YouTube. The RNN model achieves an accuracy of around 64.80%.

## Results
Tables 1 and 2 provide a comprehensive overview of performance metrics for all models, including accuracy, loss, val_accuracy, val_loss, precision, F1 score, and recall. Accuracy represents overall training set performance, while val_accuracy indicates testing set accuracy during training. Precision, F1 score, and recall are crucial metrics for image and video prediction on the validation set.

### Table 1: Training and Validation Metrics
| Dataset          | Model           | Epochs | Accuracy | Loss  | Validation Accuracy | Validation Loss |
|------------------|-----------------|--------|----------|-------|---------------------|-----------------|
| deepfake_faces   | <div align="center">CNN</div> | <div align="center">15</div> | <div align="center">0.502</div> | <div align="center">0.700</div> | <div align="center">0.501</div> | <div align="center">0.692</div> |
| deepfake_faces   | <div align="center">Xception</div> | <div align="center">5</div> | <div align="center">0.983</div> | <div align="center">0.046</div> | <div align="center">0.819</div> | <div align="center">0.778</div> |
| Celeb-DF(v2)     | <div align="center">Inception-RNN</div> | <div align="center">10</div> | <div align="center">0.627</div> | <div align="center">0.493</div> | <div align="center">0.657</div> | <div align="center">0.651</div> |

**Table 1**: shows the training and validation metrics including accuracy, loss, validation accuracy, and validation loss during the training of the models.

### Table 2: Testing Set Evaluation Metrics
| Dataset          | Model           | Precision | F1 Score | Recall |
|------------------|-----------------|-----------|----------|--------|
| deepfake_faces   | <div align="center">CNN</div> | <div align="center">0.504</div> | <div align="center">0.624</div> | <div align="center">0.819</div> |
| deepfake_faces   | <div align="center">Xception</div> | <div align="center">0.865</div> | <div align="center">0.807</div> | <div align="center">0.756</div> |
| Celeb-DF(v2)     | <div align="center">Inception-RNN</div> | <div align="center">0.643</div> | <div align="center">0.653</div> | <div align="center">0.664</div> |

**Table 2**: presents the evaluation metrics including precision, F1 score, and recall on the testing set for each model.
