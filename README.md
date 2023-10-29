
# FUM CARE Lab Robotics Projects

## Introduction
This document provides an overview of my experience working in the [FUM CARE Lab](http://www.fum-care.com/) at Ferdowsi University of Mashhad, Iran, where I had the opportunity to contribute to two robotics projects: the [FUM-Delta robot](http://www.fum-care.com/index.php/research-topics/industrial-robots/fum-delta) and the [FUM-3RRS robot](https://www.fum-care.com/index.php/research-topics/motion-simulators/fum-3rrs). The FUM CARE Lab is a leading robotics research center in Iran, boasting cutting-edge facilities, a team of expert staff, and a strong emphasis on interdisciplinary collaboration. During my 8-month tenure in the lab, I had the privilege of working under the guidance of Prof. Alireza Akbarzadeh. My name and picture can be found on the [lab's staff members' page](https://www.fum-care.com/index.php/people), under the BSc students section, with the name Kimia Mahdinezhad.

## FUM-Delta Robot

### Overview
The FUM-Delta robot is a member of the parallel robot family, renowned for its exceptional speed (approximately 10 m/s) and acceleration (100-180 m/s²). This robot comprises three parallelogram arms connected to an end effector. The joints in the FUM-Delta can be hinged, spherical, or universal. Due to its remarkable speed, the FUM-Delta is widely employed in various industries, including food and military sectors, for tasks such as pick and place and packaging of various products.
![](https://i.ibb.co/m0F7t7Z/fum-delta11.jpg)

### My Contribution
I implemented a hand gesture control system for the FUM-Delta robot using a webcam and image processing tools, including OpenCV and the [MediaPipe](https://github.com/google/mediapipe) library. This system allowed for intuitive, real-time control of the robot's movements through hand gestures. The gestures we designed included `pick` to activate the robot's suction for picking up objects (e.g., ping pong balls), `control`, and `place` to deactivate the suction and place the object.

- Hand Landmarks: We used the MediaPipe library to detect hand landmarks, enabling precise hand placement and gesture recognition.
- Control Mechanism: We utilized hand gestures and hand size to control the robot's movements, such as moving it right, left, up, down, forward, and backward. (Right, left, up, and down motions are detected by tracking the movement of hand landmarks between different frames. Forward and backward motions are detected by assessing hand size through the measurement of the distance between specific hand landmarks in various frames.)
- Object Manipulation: The robot could pick up objects using the `pick` gesture and release them using the `release` motion and a corresponding gesture.

## FUM-3RRS Robot

### Overview
The FUM-3RRS robot is a simulator with three degrees of freedom (DOF), capable of creating Heave, Pitch, and Roll movements at the end effector. This spatial parallel robot consists of a base platform, a movable platform, and three connecting legs. Each leg comprises two links and a sequence of revolute and spherical joints. The FUM-3RRS robot is specifically designed for achieving stability in swinging and turbulent environments. Despite its compact size, it can handle weights of up to 250 Kg, move 15 centimeters up or down from its home state, and generate Roll and Pitch movements of up to 15 degrees at the end effector.
![](https://i.ibb.co/SNT8J6H/fum-3rrs02.jpg)

### My Contribution
I enabled movement control on the FUM-3RRS robot, allowing it to generate trajectories by controlling roll, pitch, and yaw movements using motor drivers. Special attention was given to sensors to prevent the robot from moving too high or too low, ensuring the safety of the device. The control system was implemented using Python and C++.

Furthermore, we implemented real-time imitation of the robot's motion using an IMU sensor, which enhanced the robot's performance and precision.

## Code Availability
Please note that, due to a Non-Disclosure Agreement (NDA) signed during my work in the lab, the source code for the above projects is not available in this repository. However, you can find videos demonstrating the control of the FUM-Delta robot by myself.
