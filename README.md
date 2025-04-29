<h2 align="center"> Articulated Mechanical Manipulator </h2>
<hr>

## Forward Kinematics:
<p align="center">
 <img src="https://github.com/user-attachments/assets/6fbf1ec9-1b48-4e30-b304-93ea3dfc89ea" width="800">

## Parametric Table and Homogeneous Transformation Matrix of Forward Kinematics:
 <p align="center"> 
<img src="https://github.com/user-attachments/assets/ae3a99d1-b088-4cab-9591-c14f36f770a3" width="800">
 <p align="center"> 
<img src="https://github.com/user-attachments/assets/50501fe7-82b6-4ace-855e-efb6c8c33454" width="800">

## Inverse Kinematics:

## Top View and Front View of Inverse Kinematics:
<p align="center">
<img src="https://github.com/user-attachments/assets/2989fdba-28c3-42ac-bb22-6e33caba42af" width="800">


## Python Code of the Calculator:
  ```
### Inverse Kinematics of an Articulated Manipulator 

import numpy as np

# intro

print("╭" + "─" * 40 + "╮")
print("│{:^42}│".format("⚙️   ARTICULATED MANIPULATOR   ⚙️"))
print("│{:^40}│".format("Inverse Kinematics Calculator"))
print("╰" + "─" * 40 + "╯\n")

# link lengths in mm
print("Enter the value of the following link lengths:")
a1 = float(input("a1 = "))
a2 = float(input("a2 = "))
a3 = float(input("a3 = "))
print()

# Position Vector in mm
print("Enter the value of the following position vectors:")
x0_3 = float(input("x0_3 = "))
y0_3 = float(input("y0_3 = "))
z0_3 = float(input("z0_3 = "))
print()

# Inverse Kinematic Solutions using Graphical Method

# Solution 1
theta1 = np.arctan(y0_3/x0_3)
theta1 = theta1*180/np.pi

# Solution 2
r1 = np.sqrt((y0_3**2)+(x0_3**2))

# Solution 3
r2 = z0_3-a1

# Solution 4
phi1 = np.arctan(r2/r1)
phi1 = phi1*180/np.pi

# Solution 5
r3 = np.sqrt((r2**2)+(r1**2))

# Solution 6
phi2 = np.arccos((a3**2-a2**2-r3**2)/(-2*r3*a2))
phi2 = phi2*180/np.pi

# Solution 7
theta2 = phi1 + phi2

# Solution 8
phi3 = np.arccos((r3**2-a2**2-a3**2)/(-2*a2*a3))
phi3 = phi3*180/np.pi

# Solution 9
theta3 = phi3 - 180

# Displaying the Joint Variables
print("The following are the resulting joint variables:")
print("theta1 = ", np.around(theta1,3))
print("theta2 = ", np.around(theta2,3))
print("theta3 = ", np.around(theta3,3))
```

## Table of Trial Values:
 <p align="justify">
For the midterm activity, the group assigned values for the trial joint in MATLAB. The values are assigned ranging from 0% to 100%, 30 as 100%, and -30 as 0%. The values were entered into the MATLAB simulation and automatically generated the corresponding trial position vector utilizing forward kinematics. Afterward, the gathered position vectors for each trial are put into the Python-based Inverse Kinematics Calculator, which the group provided and coded to compute the actual joint variables. Lastly, the computed Actual joint variables from the Python-based calculator are once again entered into the MATLAB simulation to get the Actual position vector. The gathered values are compared to each other to get the comparison of forward kinematics and inverse kinematics.
 <p align="center"> 
<img src="https://github.com/user-attachments/assets/a26a2be5-c8fc-4a1b-a4ce-42db15ef1ed6" width="1000">

## Trial # 1 (0%):
 <p align="center">
Trial from MATLAB
 <p align="center">
<img src="https://github.com/user-attachments/assets/15b969e1-e5ae-4d6c-bba7-54e407e3e89b" width="500">

<p align="center">
Trial from Calculator
<p align="center">
<img src="https://github.com/user-attachments/assets/a0082c1c-73be-4843-82f4-a74ceda08abc" width="500">

<p align="center">
Actual from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/c8c0cb13-828d-4cf3-b8ad-dbd7f2c14ab6" width="500">

## Trial # 2 (25%):
<p align="center"> 
Trial from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/f4bfc7cc-4ad4-48c4-95fd-dc9e9bb650c9" width="500">

 <p align="center">
Trial from Calculator
<p align="center">
<img src="https://github.com/user-attachments/assets/6116307e-66c3-4d20-bf2b-a4f373df07ea" width="500">

<p align="center">
Actual from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/15ced4be-c9e3-4898-96d7-5d95a6d1f16d" width="500">

## Trial # 3 (50%):
<p align="center"> 
Trial from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/50b516c9-9ec5-4d89-80ff-d32fdeeac9c1" width="500">

<p align="center">
Trial from Calculator
<p align="center">
<img src="https://github.com/user-attachments/assets/6d45d49e-efe2-4e5b-a43b-355c720182e0" width="500">
 
<p align="center">
Actual from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/6568d431-a96b-404e-bc9e-3b5386c7ce48" width="500">

## Trial # 4 (75%):
<p align="center"> 
Trial from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/47d50ab1-fa75-4504-86c1-b39959ce6615" width="500">

<p align="center">
Trial from Calculator
<p align="center">
<img src="https://github.com/user-attachments/assets/20068155-241e-4c00-b89b-aa7ddd99b4d5" width="500">
 
<p align="center">
Actual from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/f4719ff3-88f3-4206-885f-4a26dd242112" width="500">

## Trial # 5 (100%):
<p align="center"> 
Trial from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/3481918e-cfec-4d5a-951b-10dbcb2e4e18" width="500">

<p align="center">
Trial from Calculator
<p align="center">
<img src="https://github.com/user-attachments/assets/cc2b5051-8b80-49d5-8dfb-605f726d2ebd" width="500">
 
<p align="center">
Actual from MATLAB
<p align="center">
<img src="https://github.com/user-attachments/assets/f4eb09fa-c230-4a16-8181-7588dca3993a" width="500">

## Conclusion:

 <p align="justify">  This lab exercise investigated the inverse kinematics of an articulated manipulator, focusing on the procedure of finding joint parameters that result in a specified end-effector position and orientation. The experiment started with building a Parametric Table based on Denavit–Hartenberg (D-H) parameters to model the geometry of the manipulator systematically. This gave us a systematic approach to deriving the Homogeneous Transformation Matrices employed in forward kinematics, allowing us to calculate the pose of the end-effector with respect to the base frame.

 <p align="justify">  By reversing the forward kinematic procedure, we used analytical and/or numerical techniques to solve the inverse kinematics problem. This enabled us to verify the motion of the manipulator for various target positions, while also resolving problems like redundancy, multiple solutions, and singularities.

 <p align="justify">  Overall, this lab emphasized the role of the underpinning concepts of forward and inverse kinematics in controlling motion in robotics. The formal application of D-H parameters and transformation matrices not only simplified the process of modeling but also underlined the mathematical exactness that applies in practical applications of robotics.  </p>

