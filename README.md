## Signature Verification using Siamese-Resnet

In this project we combine 2 popular Neural Network Architecture to verify the authenticity of the signature . They are :
- Residual Network(ResNets)
- Siamese Network

# Resnet

We use ResNet as the base network . The following image is the architecture of the ResNet:

  ![Uploading base_network.png…]()

# Siamese

Here, the siamese network takes a pair of images as input and outputs the Euclidean distance between them :

  ![siamese_model](https://user-images.githubusercontent.com/57098615/165115726-0a91a655-87be-41ee-942e-3558a515dd00.png)
