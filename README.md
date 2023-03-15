# The Temporal Property Validator (TPV)

---
## TPV Overview and Demo
We have created a video demonstration of TPV that can be viewed below.

<!--## [YouTube](https://www.youtube.com/watch?v=-BNNKYI61EE "TPV Tool Demo") or watched below.-->


<p align="center">
<video src="https://user-images.githubusercontent.com/107634143/224585912-82957982-be74-490b-b2a0-742a472e8407.mp4"/>
</p>

## TPV Installation Instructions
This repository contains a modified distribution of USE that includes our TPV plug-in. To install the tool, download the repository files as a zip folder and extract them in the desired install directory.

**Note: You must install the Java Runtime Environment in order to run USE**.


## Overview of USE 

We have used MDE technologies to define, implement, and package the code of the TPV tool as a plugin for the UML-based Specification Environment (USE). We provide a video overview of how to create UML design class diagrams and load them into USE for analysis. This tutorial can be watched below and can also be acessed on [YouTube](https://www.youtube.com/watch?v=44PB0AZTZjA "USE Tutorial").

<p align="center">
<video src="https://user-images.githubusercontent.com/107634143/206098715-3625ec62-cd35-4db7-9fa6-62deed9785df.mp4"/>
</p>



## TPV Usage Instructions

### 1. Running TPV.

**Running USE on Windows**

Open the bin folder and run the ‘use’ executable.

**Running USE on Mac**
1. Open a terminal window.
2. Traverse to the *lib* directory of the downloaded USE files
3. Execute the following command: java -jar use.jar

**Launching TPV**

After running USE, a user needs to open the TPV plugin by clicking the icon shown below.
<p align="center">
<img width="1074" alt="USEMainWindow" src="https://user-images.githubusercontent.com/107441403/206083168-a6140f9b-c09f-4510-84a3-180adbdccbab.png">
</p>
<p align="center"><b>Figure 1. USE Main Window</b></p>

This opens the TPV Main Window shown below:

<p align="center">
<img width="717" alt="MainWindow" src="https://user-images.githubusercontent.com/107441403/203444260-a06e3d34-419f-4a68-abef-0e803d1edc70.png">
</p>
<p align="center"><b>Figure 2. TPV Main Window</b></p>

### 2. Creating a Class Diagram to Input.
Refer to the Overview of USE section above for a demo of how to create UML class diagrams in USE specification. Alternatively, you can create a class diagram using any other UML tool and extract it as an XMI file that can then be opened using TPV. We provide a couple of examples in this repository to make it easier for a user to get started with the tool. 

### 3. Choosing a Class Diagram for Analysis.
The first input of TPV is the class diagram to be analyzed. TPV can take UML class into the following two formats:
1. The USE specification format saved in .use files.
2. The standard UML format saved in .uml files.

To choose a class diagram, click *Select* (TPV Main Window, 1), which opens the following window. Then, select the file containing the class diagram that will be analyzed and press *Open*.

<p align="center">
<img width="556" alt="Chooseuml" src="https://user-images.githubusercontent.com/107441403/203628591-c24e0259-759b-4e04-9128-d20059d5aa30.png">
</p>
<p align="center"><b>Figure 3. Choose Input Model File Window</b></p>

### 4. Specifying TOCL Temporal Properties.
The second input necessary for TPV is a TOCL temporal property to be checked. A user can input a property in three different ways. 

1. Using a prespecified TOCL property saved in a .tocl file.
2. Specifying a TOCL property manually from scratch. 
3. Using the specification patterns to specify a propety.

We show how to specify a property using the above three ways. The first is inputting a .tocl file containing a TOCL property (TPV Main Window, 2).
Click *Select*, which opens a window that asks for a .tocl file.

<p align="center">
<img width="554" alt="Choosetocl" src="https://user-images.githubusercontent.com/107441403/203629092-edc061bd-9ead-45f3-b686-ec69bda4afc8.png">
</p>
<p align="center"><b>Figure 4. Choose Input TOCL File Window</b></p>
  
Select a file containing a temporal property to analyze against and press *Open*.
### 5. Specifying a TOCL Temporal Property.
It is also possible to input a TOCL temporal property by specifying it within the plug-in interface (TPV Main Window, 3). Clicking *Specify* opens the following window:

<p align="center">
<img width="615" alt="SpecifyTOCL" src="https://user-images.githubusercontent.com/107441403/203629894-c3292989-b73f-49da-b32f-4c97c4fda99f.png">
</p>
<p align="center"><b>Figure 5. Specify TOCL Property Window</b></p>
  
The first specification method involves typing a TOCL property into the text box labeled *Enter TOCL temporal properties* (Specify TOCL Property Window, a).

### 6. Using the specification patterns to specify a propety.

Alternatively, clicking the *Use Patterns* button (Specify TOCL Property Window, d) will bring up the temporal pattern specification window below.

<p align="center">
<img width="1097" alt="Choose pattern window" src="https://user-images.githubusercontent.com/107441403/206089949-d5d7f571-949a-43f7-a62a-230e4d62cd22.png">
</p>
<p align="center"><b>Figure 6. Choose pattern window</b></p>


This window offers a choice to use different temporal specification patterns as templates for defining TOCL properties. After choosing one, you will then be directed to choose a scope for the property in the window below.

<p align="center">
<img width="1095" alt="Choose scope window" src="https://user-images.githubusercontent.com/107441403/206090301-448fde44-2b1d-42e6-bfdd-b3c78a824154.png">
</p>
<p align="center"><b>Figure 7. Choose scope window</b></p>

Choosing a scope results in the final window below, which includes a description of the pattern considering the scope, an example with explanation, and instructions on how to use the pattern.

<p align="center">
<img width="1092" alt="Response in global scope pattern window" src="https://user-images.githubusercontent.com/107441403/206090583-3cd033c2-c8d0-4d73-8911-b69ac757c75c.png">
</p>
<p align="center"><b>Figure 8. Response in global scope pattern window</b></p>

Specified properties can then be saved using the *Save to File* option. (Specify TOCL Property Window, e).




To use a specified TOCL property for analysis, click *Apply* (Specify TOCL Property Window, c). Any syntax errors generated by specified properties will be displayed in the dialog labeled *Feedback* (Specify TOCL Property Window, b).

### 7. Using the Optimization Technique.

The state explosion problem is a known difficulty in model checking when analyzing complex models. As such, TPV includes an *optimization technique* to improve analysis efficiency. The optimization algorithm finds elements in a model that are related to a given property and returns an optimized model that only includes elements relevant for the analysis of the property. This technique reduces the search space for analysis and was found to improve analysis times by up to 90\% during prior testing. A user needs to  click the checkbox (TPV Main Window, 4) to use it.

### 8. Choosing a Configuration Method.
The next step is configuring the analysis (TPV Main Window, 5). There are two ways to configure the analysis. The first method is entering a new analysis configuration. The second method is using a previously defined configuration stored in a .properties file.
#### i. Creating a New Analysis Configuration
Creating an analysis configuration is done by specifying a search-scope and search-depth for the analysis. Search-scope defines the maximum number of objects of each class that can be instantiated during analysis. Search-depth defines the maximum number of transitions considered for analysis. For instance, if you wanted to analyze a Restaurant model where the maximum number of customers (along with every other class) is 10 and you want to perform at most 8 operations on the system, then you might specify a search-scope of 10 and a search-depth of 8. However, the tool may produce a smaller counterexample if it is enough to illustrate an error.
Once scope and depth have been specified, it is possible to enter an advanced configuration mode. In this advanced mode, an individual analysis configuration can be created for each class and association present in the model.
#### ii. Using a Previously Defined Configuration
To use a previously created configuration, click on the *Configuration method* dropdown (TPV Main Window, 5) and select *Upload .properties file*.
The option *Enter a .properties File* should become visible. Click *Select* and choose the .properties file containing the desired analysis configuration.

### 9. Performing the Analysis.
Finally to perform the analysis and search for a counterexample, press *Validate*. You can also press *Cancel* to close the window.
<p align="center">
<img width="890" alt="Counterexample" src="https://user-images.githubusercontent.com/107441403/206092273-d6833eb9-65fd-4f6c-a98f-a910f2b40034.png">

</p>
<p align="center"><b>Figure 9. Example counterexample</b></p>

### 10. Extracting a Sequence Diagram.
Optionally, you can extract a sequence diagram from a produced counterexample. After pressing *Validate* in the last step, the window below pops up in the bottom right corner.
<p align="center">
<img width="257" alt="STM2SD" src="https://user-images.githubusercontent.com/107441403/206092548-a02ff7b9-3ac4-4b93-b037-635577ae4135.png">
</p>
<p align="center"><b>Figure 10. Snapshot Transition to Sequence Diagram Window</b></p>

Pressing *OK* converts the counterexample to a sequence diagram like the one below:
<p align="center">
<img width="244" alt="Sequence diagram" src="https://user-images.githubusercontent.com/107441403/206092978-72018e92-f687-4c63-aa36-44f9f149d82d.png">
</p>
<p align="center"><b>Figure 11. Example sequence diagram</b></p>
Using the same window, you can convert back to an object diagram and go back and forth.

### 11. Using Examples.
Along with the tool, we have provided a few examples in the *examples* folder including a Traffic Light model and a Steam Boiler Control System Model, both with temporal properties.
<p align="center">
 <img width="1227" alt="Traffic light example folder" src="https://user-images.githubusercontent.com/107441403/206085585-253a50eb-6f07-457e-b3d4-905e4fcd9dc9.png">
 </p>
 <p align="center"><b>Figure 12. TrafficLight example folder</b></p>

This folder includes a .uml file of the model, which can be used as the class diagram input in Step 3. It also includes a folder of temporal properties; any of these can be used as the temporal property input in Step 4.
<!-- ## Acknowledgement-->
<!--## Citation-->
## TPV Evaluation Survey
We would love to hear your feedback about TPV. If you would like to provide your feedback, you can fill out the following survey at 
[TPV Survey](https://forms.gle/HFdTDfSnBVrxkUSM8 "TPV Tool Demo").
Your thoughtful feedback is greatly appreciated. 

## References
##### 1. Al-Lail, Mustafa, Ramadan Abdunabi, Robert B. France,  and Indrakshi Ray. "An Approach to Analyzing Temporal Properties in UML Class Models." In MoDeVVa@ MoDELS, pp. 77-86. 2013.
##### 2. Al-Lail, Mustafa. "A Framework for Specifying and Analyzing Temporal Properties of UML Class Models." In MoDELS (Demos/Posters/StudentResearch), pp. 112-117. 2013.
##### 3. Al-Lail, Mustafa, Ramadan Abdunabi, Robert B. France, and Indrakshi Ray. "Rigorous Analysis of Temporal Access Control Properties in Mobile Systems." In 2013 18th International Conference on Engineering of Complex Computer Systems, pp. 246-251. IEEE, 2013.
##### 4. Al-Lail, Mustafa, Wuliang Sun, and Robert B. France. "Analyzing behavioral aspects of UML design class models against temporal properties." In 2014 14th International Conference on Quality Software, pp. 196-201. IEEE, 2014.
##### 5. Al Lail, Mustafa. "A Unified Modeling Language Framework for Specifying and Analyzing Temporal Properties." PhD diss., Colorado State University, 2018.
##### 6. Al Lail, Mustafa, Antonio Rosales, Hector Cardenas, Lars Hamann, and Alfredo Perez. "Transformation of TOCL temporal properties into OCL." In Proceedings of the 25th International Conference on Model Driven Engineering Languages and Systems: Companion Proceedings, pp. 899-907. 2022.
##### 7. Cardenas, Hector, Zimmerman Ryan, Antonio Rosales Viesca, Mustafa Al Lail, and Alfredo J. Perez. "Formal UML-based Modeling and Analysis for Securing Location-based IoT Applications." In REUNS 2022: The 8th National Workshop for REU Research in Networking and Systems. 2022.
