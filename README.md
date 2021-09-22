![command-line-pic](2.png)

# Autonomous Vehicle

---

<a href="https://img.shields.io/badge/JavaScipt-100%25-yellow"><img alt="JavaScript use" src="https://img.shields.io/badge/C-100%25-yellow"></a> <a href="https://img.shields.io/badge/Used-Node.js-red"><img alt="Node.js use" src="https://img.shields.io/badge/used-Rasberrypi-red"></a> <a href="https://img.shields.io/badge/used-Arduino-orange"><img alt="npm package Inquirer" src="https://img.shields.io/badge/used-Arduino-orange"></a><a href="https://img.shields.io/badge/used-Arduino-orange"><img alt="npm package Inquirer" src="https://img.shields.io/badge/used- Neural Networks-orange"></a>

## `Table of Contents`

- [Description](#)
- [Hardware used](#)
- [Language and Library used](#)
- [Licenses](#licenses)


## `Description`

The hype around driverless cars has grown rapidly over the past several years, with many big technology companies getting behind the concept. The aim of this project is to build a prototype of autonomous vehicle . 


## `Overview of the Project`
<table style="width:100%">
  <tr>
    <th>
      <p align="center">
           <a href=""><img src="lane.png" alt="Overview" width="60%" height="60%"></a>
           <br>Basic Lane Detection
           <br><a href="https://github.com/BK3820/Autonomous_car/tree/main/laneDetection">(code)</a>
      </p>
    </th>
        <th><p align="center">
           <a href=""><img src="obj.png" alt="Overview" width="60%" height="60%"></a>
           <br>Object Detection
           <br><a href="https://github.com/BK3820/Autonomous_car/tree/main/object_detection">(code)</a>
        </p>
    </th>
       <th><p align="center">
           <a href="c"><img src="tr.png" alt="Overview" width="60%" height="60%"></a>
           <br>Traffic light & sign  Detection 
           <br><a href="https://github.com/BK3820/Autonomous_car/tree/main/Trafficlight">(code)</a>
        </p>
    </th>
        <th><p align="center">
           <a href=""><img src="beh.png" alt="Overview" width="60%" height="60%"></a>
           <br>Lane Changing Behaviour
           <br><a href="https://github.com/BK3820/Autonomous_car/tree/main/Lane_chng_beh">(code)</a>
        </p>
    </th>
  </tr>
  
</table>

## `Hardware used`

- Rasberry Pi 3 B+
- Arduino UNO
- Pi Camera module
- 10000mAh Power Bank
- L298 H Bridge
- Robo Car Chasis

# Introduction

Each year just in India around 37,000 people are killed in car accidents. That is a 5.6 % increase from 2015. Human errors caused up to 90% percent of car accidents. Autonomous vehicles may help reduce this huge number of fatalities. One of the first, most popular, and most useful technologies is line detection and lane-keeping. It started developing in the 1980s and to this day it is still being improved. The desire of a man to increase the safety of vehicles on road has led to the development of different systems that are implemented into vehicles. Each new system requires an extra mathematical representation of the data in order to make decisions correctly. Adding new systems into the vehicles exponentially


# Objective
  
 The fundamental idea behind the project is to develop a prototype of an automated car that can sense its environment and move without human input. This project proposes Car automation, which is accomplished by recognizing the road, signals, obstacles, stop signs, responding and making decisions, such as changing the course of the vehicle, stopping red signals, stopping signs, and moving on green signals using Neural Network. Self-driving car processes input -- tracks a track -- and sends instructions to the actuators that control acceleration, braking, and steering. The software tracks traffic signals and lanes by means of hard-coded rules, preventive algorithms, predictive modeling, and "smart" discrimination on objects, helping the software to follow rules on transport.

## Methodolgy
		


Naturally, one of the first things to do in developing a self-driving car is to automatically detect the lane lines using some sort of algorithm. In this project, we will use Python/c and OpenCV to automatically identify the lane lines. The most significant among them is neural networks - a concept of machine learning. Machine learning algorithms make it possible for self-driving cars to exist. They allow a car to collect data on its surroundings from cameras and other sensors, interpret it, and decide what actions to take

Artificial intelligence represents the high-level control module. AI is responsible for issuing the commands to the lower level module (the vehicle). It is designed as a multiple-state machine. Depending on the current state, different machine learning algorithm is calculated. This makes future upgrades and changes of particular algorithms easier to implement. The neural network which is the convolutional neural network will be trained to make steering predictions based on detected lane markings. The lower half of the input image will be used for training and prediction purposes.

There will be input, hidden and output layers, there will be four nodes in the output layer each corresponding to steering control instructions that are left, right, forward, and reverse. The training data can be collected or the datasets already available can be used. For training, each frame will be cropped and transformed into a NumPy array. Then the train image will be paired with the training label. Then all the paired image data and labels will be stored in the npz file.

OpenCV will be used to train the neural network. After training the weights will be stored in an XML file and for generating predictions the same neural network will be created and loaded with the trained XML file. For signal and stop sign detection that is part of object detection will be done using a shape-based approach; Haar feature-based cascade classifier will be used for object detection. Since each object requires its classifier Haar cascade is used.

The Arduino board will be used to imitate button press actions. Four Arduino pins will be used to connect four chip pins on the RC remote controller, corresponding to forward, reverse, left, and right actions respectively. The Arduino will be connected to the computer through USB and the computer will send the output commands and write out low or high signals, simulating button press actions to drive the car autonomously.

As seen in the above circuit diagram robocar chassis will be mounted with four drive motors. the drive motors will be controlled by the H bridge for maintaining speed and direction. the power bank will be the primary source of power supply for all components in the car. Here Arduino will be acting as a slave device that will be controlled by the raspberry pi. apparently raspberry pi acts as the master device. For lane detection, a Pi camera module is connected to the raspberry pi. Above all the circuit board acts as the centralized part which handles the input and output between the components through header pins and USB cable, instead of gaining power supply directly from the power bank.


As mentioned earlier the above-given circuit board acts a significant role in the whole project -the four header pins help us to provide power supply to Arduino and the USB cable helps to produce power supply to raspberry pi, the reason the capacitor is placed in the circuit board is that as sometimes the power supply gets fluctuated which eventually keep on rebooting the raspberry pi, hence to avoid such circumstances A 1000 microfarad 25-volt capacitor is placed



## References


[1] U.S. Department of Transportation’s National Highway Traffic Safety Administration. (2016). Retrieved from United States Department of Transportation: crashstats.nhtsa.dot.gov/Api/Public/Publication/812456 

[2] Tan, B., Xu, N., & Kong, a. B. (2018). Autonomous Driving in Reality with Reinforcement Learning and Image. arXiv preprint arXiv:1801.05299. Retrieved from https://arxiv.org/pdf/1801.05299.pdf 

[3] Massimo, B., & Broggi, A. (1996). Real-time lane and obstacle detection on the GOLD system. Intelligent Vehicles Symposium, 1996., Proceedings of the 1996 IEEE, 213-218. 

[4] Bertozzi, M., Broggi, A., Conte, G., & Fascioli, A. (1997). Obstacle and lane detection on ARGO. Intelligent Transportation System, 1997. ITSC'97., IEEE Conference on. IEEE, 1010-1015. 

[5] Wang, H., & Chen, Q. (2016). Real-time lane detection in various conditions and night cases. Intelligent Transportation Systems Conference, ITSC '06. IEEE, 1226-1231. 

[6] Aly, M. (2008). Real time detection of lane markers in urban streets. Intelligent Vehicles Symposium, IEEE, 7-12. 

[7] Bojarski, M., Del Testa, D., Dworakowski, D., Firner, B., Flepp, B., Goyal, P., Jackel, L.D., Monfort, M., Muller, U., Zhang, J. and Zhang, X. (2016). End to end learning for self-driving cars. arXiv preprint arXiv:1604.07316. 

[8] Krizhevsky, A., Sutskever, I. and Hinton, G.E. (2012). ImageNet Classification with Deep Convolutional. Advances in neural information processing systems, 1097-1105. 

[9] Hopcroft, J. E., Motwani, R., & Ullman, J. D. (2007). Introduction to Automata Theory, Languages, and Computation. Pearson Education, 37-47. 

[10] Simon Haykin, “What is a neural network?” in NEURAL NETWORKS A Comprehensive Foundation, Delhi, India: Pearson Education, 2005., ch. 1, sec. 1, pp. 23 – 24. 

[11] Jiangwei, C., Lisheng, J., & Lie, G. (2004). Study on method of detecting preceding vehicle based on monocular camera. Intelligent Vehicles Symposium, IEEE. 

[12] [Igor Ciganovic]. (2017, October 26). Self-Driving Car AI [Video File]. Retrieved from https://www.youtube.com/watch?v=W2hugeCLAKI



## `Language and Library used`

- Machine learning(Neural Networks)
- C
- Open cv



