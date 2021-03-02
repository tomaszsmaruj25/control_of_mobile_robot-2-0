# Control of mobile robot with kinematics and dynamics model

## Introduction
The aim of the discussed laboratory exercises was to get to know and understand the issues related to the control of mobile robots. In the following exercises, individual work stages were performed - from creating a robot model to designing a controller. The end result was to be the modeling of a limited mobility mobile robot control system with kinematics (2.0). 

## Sources and environment

The model was made in Matlab & Simulink. Project created together with [Szymon Kacperek](https://github.com/szymonkacperek). 
For this task we used the script ["Controlling mobile robots, laboratory - Maciej Michałek, Dariusz Pazderski"](https://issuu.com/wydawnictwo_pp/docs/sterowanie_robotow)

## Controller Types

### Linearization techniques
As a mobile robot is a nonlinear system, controlling such a robot is more difficult than in
the case of linear systems. Therefore, the drivers resulting from this method rely on adding to the chip
linearizing feedback from state. Linearization can be performed by two procedures:
• Determining the linear approximation resulting from the expansion into the Taylor series near a certain one
operating point.
• By transforming the state variables and control inputs in the input-output path using
feedback.
This controller is suitable for trajectory tracking, position retrieval, and track following. 

### Pomet stabilizer
This method is designed for point stabilization task. The main problem with getting to a point is the lack of continuous excitation, as in the case of a trajectory tracking task, for example, where it is time dependent. It is constant over time for the task of driving to a point. The main concept of this control is to replace the stimulation from the reference signal generator with a trigger artificially generated in feedback. The time-dependent function will be used for this, which will bypass the limitations of Brokett's theorem and constantly stimulate the target point. 

###  VFO Method
The vector field orientation control method (VFO) belongs to the class of discontinuous algorithms. It makes it possible to solve the task of tracing variables in time and the task of point-to-point control. The discontinuity in the driver version for the control-to-point task allows the constraint resulting from Broktett's theorem to be omitted. The principle of VFO control results from simple geometric interpretations related to the structure of the kinematics model.
The key element in the VFO control is the so-called The vector field of convergence (depending on the state of the robot) which has the dimension of the generalized velocity. 
