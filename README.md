# deep-fake-detection
Enhancing Deep Fake Detection In Multimedia: A Fusion of CNN and RNN Approaches

Within this repository, you'll discover three notebooks: "Deep Fake Detection on Images," "Deep Fake Detection on Images (XCEPTION)," and "Deep Fake Detection on Videos."

The dataset utilized for "Deep Fake Detection on Images" and "Deep Fake Detection on Images (XCEPTION)" can be accessed at the following link: https://www.kaggle.com/datasets/dagnelies/deepfake-faces

Regarding the dataset used for image detection, it comprises two main components - a metadata CSV file and a folder named "faces_224." The metadata.csv file provides detailed information about each image found in the "faces_224" folder, specifying whether an image is categorized as "Real" or "Fake." The "videoname" column in the metadata file corresponds to the names of images within the "faces_224" folder, while the "label" column designates the class of each image, either "Fake" or "Real."

## Deep Fake Detection on Images, Deep Fake Detection on Images(XCEPTION):
A Convolutional Neural Network (CNN) model is created for false media detection, specifically applied to images. The initial CNN model achieved an accuracy of approximately 50.13% on the validation dataset. To enhance accuracy, transfer learning is employed, incorporating the Xception Model pre-trained on the "ImageNet" dataset. The Xception Model, with 71 layers, is fine-tuned, culminating in a validation accuracy of 65.93%.

## Deep Fake Detection on Videos:
Expanding the detection capabilities to videos, an Recurrent Neural Network (RNN) with Inception_v3 transfer learning is implemented. The dataset comprises interview videos of celebrities sourced from YouTube. The RNN model achieves an accuracy of around 64.80%.
