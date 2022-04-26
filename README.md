# Signature Verification using Siamese-Resnet

In this project we combine 2 popular Neural Network Architecture to verify the authenticity of the signature . They are :
- Residual Network(ResNets)
- Siamese Network

## Resnet

We use ResNet as the base network . The following image is the architecture of the ResNet:

  ![base_network](https://user-images.githubusercontent.com/57098615/165115852-b7680112-dfd6-4ed8-8dae-bfa7316905cc.png)

## Siamese

Here, the siamese network takes a pair of images as input and outputs the Euclidean distance between them :

  ![siamese_model](https://user-images.githubusercontent.com/57098615/165115726-0a91a655-87be-41ee-942e-3558a515dd00.png)
  
## Dataset

The datset used here is the [CEDAR Dataset] (http://www.cedar.buffalo.edu/NIJ/data/signatures.rar)

## Preprocessing

We create a dataframe whose first 2 columns contain the relative paths of the image pair and the third column contains the label ; where, 1 corresponds to the legitimate pair and 0 corresponds to the forgery/fake pair .

We resize the image into the shape (150,220) .

## Loss function :

The loss function used here is contrastive loss . It minimizes the distance between similar input and maximizes the distance between dissimilar inputs .

  ![contrastive_loss](https://user-images.githubusercontent.com/57098615/165119751-c4c658c8-01a8-4514-a21d-4da22c45d9e7.png)
  
## Training

We use the TPUs provided by Google Colab for training . 

## Evaluation 

We use the best model, so far . Then, predict the output for the test set . We also use the a threshold of 0.5 for classifying . 
