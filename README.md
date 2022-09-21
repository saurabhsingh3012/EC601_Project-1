## Project 1 Report

# Visual Question Answering using Machine Learning Techniques
## Saurabh Singh




### What is VQA?

![](https://user-images.githubusercontent.com/113216824/191624483-5c4d66ac-906b-4d2a-9511-fab4ee5c4c86.png)

Visual Question Answering is a field that combines elements from various disciplines such as Computer vision, natural language processing, question featurization, image featurization and deep learning [2]. VQA attempts to respond to (usually) text-based questions about an image by inferring the answer. To do this, VQA not only needs to solve the problems already existing in computer vision, but also needs the ability to understand the question asked and reason out the answers based on the information available in the image.

A robust VQA system should have the ability to solve a wide array of questions posed to it. It should be able to answer not only direct binary or multiple-choice questions (example, what is the colour of the umbrella?), but also complex questions whose answers might be ambiguous (example, why is the dog barking?). 

There are many potential applications for VQA. One of the most obvious applications is for VQA to be used by visually impaired individuals to get information about their surroundings. A more general applications would be to improve the natural human-computer interaction that exists today. A more rigorous application could also be as an image retrieval system in search engines.[1] In fact, it has also been suggested that VQA could be used a component of image understanding for a Turing test [3] (a test that measures a machine’s ability to emulate behaviour that is indistinguishable from that of a human being).


### Current Research and Challenges:

In order for VQA to reach its solution, it has to solve a number of computer sub-problems, including but not limited to [1]

*	Object recognition – What is beside the car?
*	Object detection – Is the man wearing a hat?
*	Attribute classification – What colour is the apple?
*	Scene classification – Is it going to rain?
*	Spatial reasoning – What is between behind the cat?

