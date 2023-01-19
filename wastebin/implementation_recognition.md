---
title: Implementation Waste Recognition
layout: default
parent: wastebin
nav_order: 3
---

# Implementation of the waste recognition

One of the core mechanics of this prototype is the recognition of different kinds of waste which triggers the catapult mechanism in case of the the wrong kind of trash is thrown into the bin.
In the following the implementation of the waste recognition shall be described in detail as well as the different attempts at implementing it. 

## Setup
For the recognizing different kinds of trash a raspberry pi in combination with a camera module was used. This camera was then directed at the area of the bin where the waste gets thrown in by people passing by. For the implementation of the recognition system python was chosen as language. 

## Iteration A

The first approach to solve the waste recognition task was to find pre-trained models which could be easily used to recognize different kinds of waste. Beside being able to classify different kinds of waste the model also needed to be usable on a raspberry pi. After some research a firs pre-trained model was found. It was a tensorflow-lite model pre-trained on the COCO-dataset which includes 80 different classes of objects. Since there was no suitable waste dataset within reach at this point the idea was formed to test this model as a first try and only use the class "bottle" for recognition.
Meaning that the only distinction would have been between a bottle and every other kind of waste. But experimenting with the camera module it the realization came fast that the model was not working well enough for the purpose of this prototype. While the model was not a suitable solution a first code snippet for loading and applying models was found.

## Iteration B

Since the first model was not working well enough the decision was made to look for pre-trained models which were trained on more specific datasets meaning models that were actually able to distinguish mainly between waste and did not include other objects. After some research a dataset called TACO ("trash annotated in context") on Kaggle. This dataset included only images of different kinds of waste and offered detection as well as classification.
