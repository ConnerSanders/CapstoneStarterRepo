# Pulse Inverted Electrolyzer

## Executive Summary

 The Pulse Inverted Electrolyzer primary goal is to boost the efficiency of the standard constant current electrolysis machine. A Standard Electrolysis system takes in constant current and turns an electrolytic solution into gasses from said solution. The  Pulse Inverted Electrolyzer will boost efficiencies in two ways. One will be by pulsing the current given to the electrodes, and the other by using constant magnetic fields to redirect ions back to the electrodes. By pulsing the current in an electrolyzer it takes advantage of two ideas happening inside the water of the system. When first fired on the electrodes will gain electrons around, and prevent current from passing through. By pulsing the current the system allows for this layer to disperse to make for more current to flow through the electrolytic solution. Also by pulsing the current, we will be able to send a burst of energy through the system instead of the constant current normally supplied. The other way the system will boost efficiency will be by using magnets placed around the housing of the cell. This will basically push the electrons closer to the electrodes and further away from the cell walls. The system will also include a way to read the power the pulse inverter will be drawing and the amount of gas being outputted, to then calculate the efficiency of the energy of the system's output versus its input. 

## Capabilities
The system will be divided into multiple systems that each have several expectations. The controller system should calculate the energy efficiency based on the flow rate of the gas output and the current draw of the pulse inverter. The safety system should any failed state go to a shutoff state. There will be a bypass for the user to be able to light the gas at the output of the gas system. The water system should automatically refill the cell with water whenever the system is too low.


## Salient Outcomes

While we did connect a pulse inverter to the cell, there were many issues with the pulse inverter tied to the resistance. The group was able to adjust to a lot of unknowns such as the pulse inverter's resistance and adapted as best as they could. Another Big outcome was the fact we had gas production from a pulsed current, as it is not common practice and with more time we could figure the best parameter of the pulse inverter to boost gas production.


## Project Demonstration & Images
[Video Demonstration](https://www.youtube.com/watch?v=DhT7RktQMQU)
<br> <img src="Documentation/Images/Front_Page/Gas_production.PNG" width="150" length="300">
<img src="Documentation/Images/Front_Page/Flame.PNG" width="300" length="600">
<img src="Documentation/Images/Front_Page/Explosion.PNG" width="300" length="200">

## About Us

### Team

**Brennan Angus**

**Matthew Beausoleil** is an Electrical Engineering student at Tennessee Technological University with a minor in Computer Science. Matthew's interests are in digital system design, telecommunications, and signal processing. Matthews's main focus in the project is the design of the water system, and ensuring that it automatically refills the water when senses it is not high enough.

**Jacob Cooper** is a Computer Engineering student at Tennessee Technological University. Jacob's interests are Circuits and Digital Based Programming. Jacob's main focus in the project is the design of the gas system and making sure there is correct ventilation and gas processing in order to create an output flame.

**Wyatt Groves** is an Electrical Engineering student at Tennessee Technological University. Wyatt's interests are Telecommunication and Signal Processing. Wyatt's main focus in the project is the design of the power system and ensuring all components receive the proper amounts of power. 

**Austin Jerrolds** is a Computer Engineering student at Tennessee Technological University. Austin's interests are Embedded Systems, Digital System Design, and software development. Austin's main focus in the project is the controller system which is responsible for the efficiency computations to measure the project's success. 

**Conner Sanders** is a Computer Engineering student at Tennessee Technological University. Conner's interests are embedded and Digital Systems. Conner also has some experience with controls and pneumatics. Conner's main focus in the project is the safety system, which cuts off power if the electrolyzer becomes unsafe.

### Faculty Supervisor
[Charles Van Neste, Phd](https://www.tntech.edu/directory/engineering/faculty/charles-van-neste.php) is an Assistant Professor at Tennessee Tech University. He received his Bachelor's, Master's, and Doctorate at Tennessee Technological University. 

### Stakeholders
The customer for the project is Dr. Van Neste for research he wishes to pursue in making a residential electrolyzer for the uses of hydrogen-powered cars. The project will be using technology develop by Dr Van Neste to see the impact it would have on the overall efficiency of the system.  



### Recognitions

The team would like to thank the ECE Department for any assistance needed in the early stages of design. We would especially like to thank **Jesse Roberts** for helping the team when Dr. Van Neste was busy with other work. 

## Repo Organization

### [Reports](/Reports)

The [Project Proposal](/Reports/Proposal/Project_Proposal-V2.pdf) report addresses key questions about the project. It states exactly what the problem is and what the solution plans to achieve. 

The [Conceptual Design and Planning](/Reports/Conceptual%20Design/Conceptual_DesignV2.pdf) report provides all specifications and constraints the project must follow. This includes standards and regulations that must be followed.

The [Experimentation](/Reports/Experimentation/Experimentation.md) report shows the experimentation done by the team to verify the project's constraints and measures of success.

The [Poster](/Reports/Poster/Capstone_Final_Presentation_Poster.pdf) is a visual summary of the project that is presented at the Senior Design Expo.

The [Final Presentation](/Reports/Final%20Presentation/Capstone%20Final%20Presentation.pdf) includes the final report/presentation done by the team to summarize the project's progress.

The [Lessons Learned](/Reports/Lessons%20Learned/Lessons%20Learned.md) files show all lessons learned throughout the process. It includes lessons in team communication, project management, and technical knowledge.

### [Documentation](/Documentation)

All documentation is included in the above folder. Folders for the files including schematics and images are included in their respective folders. All files related to a specific signoff are then in a subfolder labelled appropriately.

Documentation includes all schematics, images, models, and designs used in the project. 

[Signoffs](/Documentation/Ss) folder houses all approved detail designs. These designs are for each subsystem and show all constraints. The signoffs should convince the reader that all constraints are met as well as link to all other relevant documentation in their respective folders. These signoffs should also link any relevant software.

The [Meeting Minutes](/Documentation/Meeting%20Minutes) folder contains dated minutes for all team meetings. This allows the reader to analyze current and previous progress in a time-based manner. 


### Software
All software will be located in this directory. For each specific problem or system, a folder will be created that contains all relevant code along with a readme that explains the installation, compiling, and execution of the code.
