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

The overarching goal of VQA is to extract question-relevant semantic information from the images, which ranges from the detection of minute details to the inference of abstract scene attributes for the whole image, based on the question.[1] Most VQA models use deep CNNs for image classification. But biases in the questions asked or the type of dataset used to train the VQA could actually decrease the “robustness” of the model. For example, if a question like, “What is the colour of the tree?” is asked, the presence of the term ‘colour’ automatically reduces the question into a multiple-choice question, and if the dataset used to train the model is diverse enough, the model would have a ‘pseudo-efficiency’ in predicting the correct answer. For example, the dataset VQA has 73 images containing trees, and 70 of them trees that are green. So even if the model predicted the colour of the tree to be green every time irrespective of the picture, it would still have a high number of correct answers.


While there are many number datasets to train VQA models on, the most popular datasets are:

*	DAQUAR [4] - The DAtaset for QUestion Answering on Real-world images (DAQUAR) (Malinowski and Fritz, 2014a) was the first major VQA dataset to be released. While it was a pioneering dataset specifically for VQA, it is too small to evaluate complex models. Moreover, it has only indoor images, which restricts the variety of questions that could be asked.
*	COCO-QA [5] – COCO has image and QA pairs that are created using NLP and captions from the images. The biggest drawback of COCO is due to the flaws in NLP algorithm used to generate the captions. This results in weirdly structured questions, even some that are completely unintelligent. Also, it has only four kinds of questions, which is limited to the kinds of things described in the captions of the images.
* The VQA Dataset [6] – VQA dataset consists of both real images from COCO (COCO-VQA) and cartoon images (SYNTH-VQA). Due to diversity and size of the dataset, COCO-VQA has been widely used to evaluate algorithms. However, COCO-VQA has a large variety of questions that could be answered without looking at the images due to language biases.


There are also some difficult in determining suitable evaluation metrics for VQA. While evaluating the accuracy of multiple-choice answers could be a good strategy for a few problems, but questions that are more open-ended (Example: What is in that tree?), evaluating them on the basis of the accuracy of their answers could be difficult as there could be multiple right answers. (All answers: ‘Bird’, ‘Eagle’, ‘Bald Eagle’, are correct, but the evaluation metric might penalize the answer for ‘Bird’ and ‘Eagle’ just as much if the answer was ‘Horse’. One way to minimize this could be to assign 

### Conclusions

![](https://user-images.githubusercontent.com/113216824/191626008-d5b3cf88-4f82-498c-84bf-0600a6441771.png)

As shown in above, there has been rapid improvement in the performance of VQA algorithms, but there is still a significant gap between the best methods and humans. It remains unclear whether the improvements in performance come from the mechanisms incorporated into later systems, e.g., attention, or if it is due to other factors. [1]

Although many methods have been proposed for VQA, it is difficult to determine what general techniques are superior and is heavily determined on the dataset used to train the model. For example, a model trained on a unbalanced version of VQA performed 11% worse than a model based on a balanced version of the dataset.[7]

Thus, VQA is an important basic research problem in computer vision and natural language processing that requires a system to do much more than task specific algorithms. For this, we need to more varied training datasets, remove biases from existing ones and create algorithms that could answer complex and ambiguous questions


### References:

[1] Kushal Kafle, Christopher Kanan. “Visual question answering: Datasets, algorithms, and future challenges”. Available: https://www.sciencedirect.com/science/article/pii/S1077314217301170

[2] Kenneth Marino, Mohammad Rastegari, Ali Farhadi and Roozbeh Mottaghi; OK-VQA: A Visual Question Answering Benchmark Requiring External Knowledge. https://arxiv.org/pdf/1906.00067.pdf

[3] Malinowski, M., Fritz, M., 2014b. Towards a visual turing challenge. arXiv preprint                   arXiv: [1410.8027] Towards a Visual Turing Challenge ([arxiv.org](https://arxiv.org/pdf/1410.8027.pdf))

[4] Malinowski, M., Fritz, M., 2014a. A multi-world approach to question answering about real-world scenes based on uncertain input. In: Advances in Neural Information Processing Systems : [CVPR 2016 Open Access Repository (cv-foundation.org)](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Redmon_You_Only_Look_CVPR_2016_paper.pdf)

[5] Mengye Ren, Ryan Kiros, Richard Zeme, Exploring Models and Data for Image Question Answering:https://proceedings.neurips.cc/paper/2015/hash/831c2f88a604a07ca94314b56a4921b8-Abstract.html

[6] Stanislaw Antol, Aishwarya Agrawal, Jiasen Lu, Margaret Mitchell, Dhruv Batra, C. Lawrence Zitnick, Devi Parikh: [VQA: Visual Question Answering (thecvf.com)](https://openaccess.thecvf.com/content_iccv_2015/papers/Antol_VQA_Visual_Question_ICCV_2015_paper.pdf)

[7] Peng Zhang, Yash Goyal, Douglas Summers-Stay, Dhruv Batra, Devi Parikh; Yin and Yang: Balancing and Answering Binary Visual Questions: Yin and Yang: Balancing and Answering Binary Visual Questions ([thecvf.com])(https://openaccess.thecvf.com/content_cvpr_2016/papers/Zhang_Yin_and_Yang_CVPR_2016_paper.pdf)
