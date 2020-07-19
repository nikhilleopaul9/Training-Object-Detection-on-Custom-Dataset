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
