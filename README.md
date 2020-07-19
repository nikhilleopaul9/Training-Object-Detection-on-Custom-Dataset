# Training-Object-Detection-on-Custom-Dataset
Training an object detection RCNN network on our own custom datasets using Keras and TensorFlow libraries.

The different steps involved are:

* Gather the images and label them using LabelImg.

* Build an object detection dataset using Selective Search

* Fine-tune a classification network (originally trained on ImageNet) for object detection

* Use our fine-tuned network to classify each region proposed via Selective Search

* Apply non-maxima suppression to suppress weak, overlapping bounding boxes

* Return the final object detection results

## Gather the Images to create the dataset and label them

I have created a watch detection model using around 500 Images of different types of watches downloaded from the internet. The images are labeled using the [LabelImg Tool](https://github.com/tzutalin/labelImg).

![Screenshot (46)](https://user-images.githubusercontent.com/49313619/87877855-59947880-c9fe-11ea-92e8-bab93c1a2a9c.png)

## Building the Dataset 

Run the BuildDataset.py file to build the dataset with positve as well as negative images in two different folders. Two folders named watch and no_watch will be created with thousands of photos in both the folders. 

![Screenshot (47)](https://user-images.githubusercontent.com/49313619/87878182-4d111f80-ca00-11ea-87e3-ebb2088a7199.png)            ![Screenshot (48)](https://user-images.githubusercontent.com/49313619/87878183-4e424c80-ca00-11ea-9ccd-4dfa64c838a1.png)

