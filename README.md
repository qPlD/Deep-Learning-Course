# Deep-Learning-Course

## Introduction
You will create a classifier and test it on a collection of images for a new task. While you are welcome to build a full network from scratch, most of you will not have sufficient access to the data and compuational power required, so you are welcome to provide a solution based on transfer learning from a pre-trained network, adapted to your new task.

## Pytorch
</br>PyTorch has a range of pre-trained models ready to use which can be accessed from https://pytorch.org/docs/stable/torchvision/models.html and information about the pre-trained versions is available at https://pytorch.org/docs/stable/hub.html#loading-models-from-hub

A tutorial on fine-tuning pre-trained networks in PyTorch is available https://pytorch.org/tutorials/beginner/finetuning_torchvision_models_tutorial.html and this gives you a good potential structure for the task.
General notes on transfer learning: https://cs231n.github.io/transfer-learning/

## Dataset
If you use the pretrained model, a good way to start is by freezing all layers up to the last layer before the output. Adapt the output layer to fit your classification problem. You might then unfreeze some earlier layers for further fine tuning.

You will need to create a training set (at least 100 images per class, potentially classifying e.g type of location, activity. If you are training a full network from scratch you would need orders of magnitude more, but this will work for transfer learning on an existing network). It might be sensible to start off testing and demonstrating your approach by using an existing dataset e.g. the flowers one. You can find other interesting datasets at:

* Google's dataset search tool
* http://deeplearning.net/datasets
* UCI ML collection
* https://www.visualdata.io
* https://ai.google/tools/datasets

**Final Chosen dataset: Caltech101**

---

You should not just work with a single pre-created dataset, but you can augment your own data with data from one or more other datasets, but there should be a significant level of novelty in the dataset created.

Write a pre-processing step that will resize and crop the images to the right size ((224, 224) is default for ResNet50 and (299,299) is the default for Inception), and consider how you can apply data augmentation techniques to your new dataset, and design appropriate pre-processing functions.
