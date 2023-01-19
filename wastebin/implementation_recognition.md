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

The first approach to solve the waste recognition task was to find pre-trained models which could be easily used to recognize different kinds of waste. 