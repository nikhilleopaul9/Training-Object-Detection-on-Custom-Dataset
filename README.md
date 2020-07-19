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

**watch and no_watch folders**

![Screenshot (47)](https://user-images.githubusercontent.com/49313619/87878182-4d111f80-ca00-11ea-87e3-ebb2088a7199.png)      ![Screenshot (48)](https://user-images.githubusercontent.com/49313619/87878183-4e424c80-ca00-11ea-9ccd-4dfa64c838a1.png)

## Fine-tuning a network for object detection with Keras and TensorFlow

Run the script for tuning the model. Run the Mobilenet script if you have a low end PC and run the Resnet50 script if you have a high end PC with minimum 12-16 GB of ram or minimum 4GB-6GB of GPU memory. You can even use the RCNN_Tuning.ipynb in Google Colaboratory for better performance. Mobilenet may not be able to perform as good as the Renet50 Model, but it will be much faster when it comes to computation. 

We are Fine Tuning a Resnet50 CNN which is pre-trained on the 1,000-class ImageNet dataset for better performance. It will take a significant amout of time depending on your PCs configuration and the CNN Model used. 

## Final Object Detection Results

![Screenshot (49)](https://user-images.githubusercontent.com/49313619/87878803-3ec50280-ca04-11ea-9913-418c7bc99409.png)
![Screenshot (50)](https://user-images.githubusercontent.com/49313619/87878798-3c62a880-ca04-11ea-87a8-7577fe287d6c.png)

![Screenshot (51)](https://user-images.githubusercontent.com/49313619/87878801-3e2c6c00-ca04-11ea-95af-31f4b28815d5.png)

<p align="center">
  <![Screenshot (51)](https://user-images.githubusercontent.com/49313619/87878801-3e2c6c00-ca04-11ea-95af-31f4b28815d5.png)>
</p>
