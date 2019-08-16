# Transfer Learning

## Dataset
Link to download dataset: https://www.kaggle.com/slothkong/10-monkey-species/home (Download size: 547 MB)

The dataset has images of 10 species of monkeys (10 classes) and around 100 images for each class 

## Conventional CNN
Conventional CNNs requires way more data than what is available here but I've implemented it as a comparision to the transfer learning performance.

I've implemented a 5 layer network (3 convolutional layers and 2 fully connected layers) and achieved an **accuracy of 54% on the test set after 7 epochs.**

## Transfer Learning
The idea behind transfer learning is to use a network which has already been trained on a similar task and use the weights of that network for our task.

There are 2 ways to go about this:
1. Directly use the weights of the network without training it any further which just performs forward propagation with the weights of the model .
2. Download the weights of the model and add a few custom layers on top of the pre-trained model and let it train on the small datatset for a few epochs to fine-tune the parameters to perform better on this specific task.

I've used the Xception model for the transfer learning. This is a network developed by Francois Chollet (Google Inc) and has been trained on ImageNet.

I implemented the first method of transfer learning mentioned above and achieved an **accuracy of 91.5% on the test set after 7 epochs.**

## System requirements
1. Jupyter notebbok
2. Tensorflow
3. Keras
4. numpy
5. cv2 (OpenCV- to read images)

## How to run the code
* Download the dataset from the link and extract it to get the 10-monkey-species folder. This has the training and validation images in it.
* Copy the Transfer_Learning.ipynb file in the src folder to the same path as the 10-monkey-species folder.
* Run all the cells in the notebook.
