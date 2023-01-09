---
layout: page
title: About Me
permalink: /about
---

<div class="post-flex-display">
    <img src="/img/dkprofile.jpg" width="300" alt="dkprofile">
</div>

### Contact

[E-Mail](mailto:dhk6869@gmail.com)
[Github](https://github.com/dokkev)

### Education
- PhD in Mechanical Engineering, University of Texas at Austin, 2022 - Current
- MS in Robotics, Northwestern University, 2021
- BS in Mechanical Engineering, Saint Louis University, 2020
 
## About Me

Hello! My name is Dongho Kang (DK), and I am a full-stack robotician. I am a PhD Student at University of Texas at Austin starting in Fall 2022.
I am a part of the [Human Centered Robotics Lab](https://sites.utexas.edu/hcrl/)

### Current Research Topics
 - Visuotactile Perception 
 - Human Centered Robotic Sensing & Navigation
 - Biomimetic Robotic Systems


### Past Research

During my time at Northwestern University, I focused my research topics on whisker-based tactile sensing, manipulation, and robotic perception.
My big interest in robotics comes in developing robots and sensors inspired from animals. My final project [Whisker-based Tactile Sensing and Classification](https://dokkev.github.io/Whisker/) at Northwestern focuses on understanding and quantativelt interpreting three-dimensional dynamic data that a rat obtains through whisking over different shapes of objects in a simulation. Rats use whiskers to navigate through holes and find open space. As they scan, their whiskers make unexpected contact with an object, and the rat then explores the object to extract the details of its shape. The use of whisker inputs to detect, localize, and extract the spatial properties of objects. These unique features allow rats to operate in complete darkness<sup>1</sup>, and I hope to integrate these features into robotics research for robotic navigation.

In neuroscience, we wonder how rats process the mechanosenosry input to determine their actions during active sensing. A rat tends to bring its snout to the object as close as possible while ensuring whiskers contact the object symmetrically, and this project provides reinforcement learnings models that mimic a rat's active sensing behaviors to investiage the coordinate transformation from the whisker frame to the haed frame through evaulating  the weights of each whisker to neurons in the input layer in neural networks of reinforcement learning models.

My [Autonomous Fire Fighter Robot Arm](https://dokkev.github.io/firefigther-robot/) project aims integrating a fire safety feature to a common robotic arm manipulator that can be widely used in various settings such as warehouses, garages, and houses. I believe that making robots cope with emergency situations like fire is an important step for robots to operate and cooperate with humans in our daily lives.

### Current Research
Human integrates the sense of vision and touch to perceive the world allowing us to extract tactile information from vison and visualize geometric features from touch. This sophiscated multimodality is achieved by learning as an infant develops visuotactile coordination through haptic exploration such as grasping during first 12 months. Yet, robotic perception is in its infancy compared to human sensory, perceptual, and cognitive systems. Despite spectacular progess of tactile sensing technology such as biomimetic tactile sensors inspired from skin in this past decade, connecting tactile perception and computer vision in robotics to implement mulitimodality is still a challenge, and I hope to investigate this topic in my doctoral studies. 



<!-- ### Research Interests
I hope to pursue a Ph.D. to investigate dexterous robotic manipulation 

<strong>Adaptive Grasping with Dynamic Tactile Sensing</strong>
While fast-adapting mechanoreceptors enable humans to identify contact events such as object slippage, dynamic tactile sensing systems provide essential information for robots to perform dexterous manipulation. Therefore, I would like to research distributed dynamic tactile sensing system designs to imitate Meissner and Pacinian corpuscles. I am particularly interested in utilizing fiber-based transducers. While they satisfy dynamic tactile sensors’ design principles with their flexibility and high sensitivity, they are also capable of multiplexing and light. I hope to investigate and compare the performances of different types of dynamic tactile sensor design, such as piezoelectric, capacitive, and magnetic sensors in different environments during my doctoral studies.

<strong>Multimodal Tactile Sensing with Computer Vision</strong>
The sense of touch and vision work together as parts of a multimodal system as humans often combine touch with vision. I hope to investigate combining vision data and tactile data to implement multimodal tactile sensing systems. I believe that this multimodal sensing system can transfer information across modalities to reinforce the performance of tactile sensing. For example, training vision modality with tactile data will allow it to infer tactile information from computer vision like human estimates the texture of an object with eyes. On the other hand, vision modality can transfer image recognition data to train tactile modality and link tactile and visual information together. I hope to apply these technologies for autonomous and dexterous manipulation during my Ph.D.

<strong>Stereognosis and Modeling of Soft Robots</strong>
Implementing stereognosis in soft robotics requires both proprioception and tactile sensing simultaneously, while stretchable, resilient, durable, and multimodal sensor design is challenging but crucial. Stereognostic sensing enhances locomotion and manipulation performance by the distribution of strain to prevent mechanical failure. I hope to implement and improve flexible and durable proprioception and tactile sensing systems that can classify mechanical cues during my Ph.D. In addition, there have not been many studies on data interpretation of soft robotic sensing, and they are often oversimplified despite the complexity of the shape reconstruction \cite{ml}. I hope to research advanced data processing algorithms with machine learning to achieve accurate proprioception of soft robots. 

<strong>Sensory Feedback Control with Machine Learning.</strong>
While conventional rigid robots utilize motor controls on their joints, soft robots face challenges in accurate analytic modeling due to complex behaviors such as nonlinearity, deformation, and hysteresis \cite{soft}. I believe that data-driven controllers which utilize sensory information can be enhanced with machine learning to solve non-linear problems. With proper stereognostic sensing, I believe it is sufficient to implement deep learning algorithms to estimate inverse kinematic solutions for 3D motion. Combined with tactile sensing feedback, I hope to implement a closed-loop control system to improve actuation accuracy. Moreover, I would like to investigate a reinforcement learning approach for optimal control for electrically-driven soft actuators.   -->



### References

[1] Hartmann MJ. A night in the life of a rat: vibrissal mechanics and tactile exploration. Ann N Y Acad Sci. 2011 Apr;1225:110-8. doi: 10.1111/j.1749-6632.2011.06007.x. PMID: 21534998.

[2] Robert D. Howe (1993) Tactile sensing and control of robotic manipulation,
Advanced Robotics, 8:3, 245-261, DOI: 10.1163/156855394X00356
