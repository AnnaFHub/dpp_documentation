---
title: wastebin
layout: home
has_children: true
---

# Wastebin

Project documentation for the **Design for Physical Prototyping** course 2022/23 focusing on the topic of **Uncomfortable Devices**.

## Abstract

The idea of this project was to create a waste bin that can classify the waste that is thrown into it. If the waste belongs into the bin, it is taken, otherwhise it is catapulted out of the bin, while the person that has thrown the item into the bin gets insulted. Several iterations were necessary to get to the final prototype, both for the waste recognition part, as well as, for the bin itself.

## Concept

The idea for this project was to create a wastebin, that throws trash that does not belong into the bin back outside. Furthermore, the bin insults the person with audio output.
To throw the trash out, a catapult would be used. For the construction of the catapult multiple references were found online. However as it would not only have to catapult trash outside of the bin, but also throw correct objects into the bin, these online references were used as a starting point. After sketching differnt versions of the catapult for the usecase, the catapult in use was decided on.
The detection of wrong garbage was a bit more unclear. Multiple options were considered. The simpelest beeing a wizard of oz prototype, where a person would check whether the object belongs into the bin or not and press a button to generate the correct action. Another simplified idea was to assign a color to each garbage class and use a colorsensor to classify the garbage. The most advanced idea was to use machine learning to classify the garbage thrown into the bin.

The image below shows a first sketch of the wastebin.

![FirstSketch](assets/ersteSkizze.png)


## Implementation

A description of the implementation process can be found in the subchapters [Implementation Bin](https://annafhub.github.io/dpp_documentation/wastebin/implementation_bin.html) and [Implementation Waste Recognition](https://annafhub.github.io/dpp_documentation/wastebin/implementation_recognition.html). First focuses on the implementation of the bin itself, while the second describes the process of creating the recognition part of the project.

![throw](assets/throw2.gif)
<img src="assets/take.gif" width="300" height="510">

## Materials and tools

In the beginning the plan was to use cardboard for the first prototypes. However, cardboard was not stable enough. Therefore wood was used for the prototypes basic framework. The mechanical parts where mostly printed with PETG 3D-print fillament in order to have stable enough parts. All cableclips and mounts for the hardware were also 3D-printed. For the control of the motors and the basic logic an Arduino uno with motor shield was utilized. For the image recognition with camera and the output of the audio a Raspberry PI with a script of the programming language python was chosen. All in all the wastebin contained 1 stepper motor, 1 servo motor, 8 gears, 7 ball bearing, 1 spring, 1 ardunio, 1 motorshield, 1 raspberry PI, 1 camera, 1 speaker, 1 powerbank, 1 power supply (5V) and various small components containing about 750g 3D-print Fillament and screws.


## Conclusion

In the beginning we tried to work with cardboard to create a first prototype, however this was not stable enough, why we quickly moved on to using wood for the base construction. Without having expensive tools like a Circular saw it is very difficult to get accurate enough wood pieces for a detailed project like the catapult. All parts had to fit togehter very well, so the opportunity to use the 3D-printer for the mechanical details was very helpful. After facing problems with using the stepper motor as it was to weak for the catapulting mechanism, gears were added to reduce the force necessary by the motor. The original mechanism for folding the catapult platform up and down had to be adapted aswell, as it could not prevent the catapult platform from flipping up. The second iteration of that mechanism then worked very well. 
For the recognition of the waste, we could not manage to create an AI that would classify the waste with enough accuracy. Therefore, colordetection was used to seperate items into differnt groups. The color detection although worked really stable and the bin was able to sort properly.
