# SmartBridgeProject:CNN Model to Classify Pollen Grains based on user input
Dataset:
The dataset used for this project is Pollen Grain Image Classification Dataset from Kaggle. The classification of pollen species and types is an important task in many areas like forensic palynology, archaeological palynology and melissopalynology. This is the first annotated image dataset for the Brazilian Savannah pollen types that can be used to train and test computer vision based automatic pollen classifiers.

The dataset has a total of 790 pollen grain images (.jpg files) containing 23 classes of pollen grains. The entire file size of the dataset is 32.85 MB with images of around 300x300 resolution. It has a usability of 8.8 and gives a good accuracy with CNN’s.
kaggle data set link
https://www.kaggle.com/andrewmvd/pollen-grain-image-classification
<img width="534" height="291" alt="image" src="https://github.com/user-attachments/assets/450e9271-bd57-479a-8111-022966daf9c5" />
The model:
This is a deep learning model which solves a classification problem with respect to the above dataset. Steps involved in making the model: Data Exploration, Pre-processing, Data Augmentation, Training (with Early Stopping), Predication Modules used : tensorflow, matplotlib, numpy , Pillow, scikit-learn, cv2, collections, os and random.
Model architecture:
Pretrained InceptionV3 + -->Dense layer/hidden layer (500)--> Dense layer/hidden layer (150)--> Output layer Link to the training colab notebook The python file contains the code to run the trained model(iofinal.py)
Approach used to increase accuracy:
Data augmentation with horizontal and vertical flipping
<img width="1132" height="91" alt="image" src="https://github.com/user-attachments/assets/5eb54ad1-5406-46be-af27-75543ace68ca" />


Exception:
There is an exception for the pollen grain pairs qualea-faramea,myrcia-arecaceae and matayba-eucalipto. The model predicts the first pollen grain type for both the types in the pair. Eg: for the first pair qualea-faramea, when the input is qualea the model predicts qualea but when the input is faramea the model still predicts it as qualea.
