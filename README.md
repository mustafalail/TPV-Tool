# Temporal Property Validator

---
## TPV Tool Demo
We have created a video demonstration of TPV that can be accessed through [this](https://www.youtube.com/watch?v=-BNNKYI61EE "TPV Tool Demo") link.

## Overview of USE 

We have used MDE technologies to define, implement, and package the code of the TPV tool as a plugin for the UML-based Specification Environment (USE). We provide a [video](https://www.youtube.com/watch?v=44PB0AZTZjA "USE Tutorial") overview of how to create UML design class diagrams and load them into USE for analysis. 

## TPV Installation Instructions
This repository contains a modified distribution of USE that includes our TPV plug-in. To install the tool, download the repository files as a zip folder and extract them in the desired install directory.

**Note: You must install a Java Runtime Environment in order to run USE**.


## TPV Usage Instructions

### 1. Running TPV.

**Running USE on Windows**

Open the bin folder and run the ‘use’ executable.

**Running USE on Mac**
1. Open a terminal window.
2. Traverse to the *lib* directory of the downloaded USE files
3. Execute the following command: java -jar use.jar

**Launching TPV**

After running USE, a user needs to open the TPV plugin, as shown below.


<img width="717" alt="MainWindow" src="https://user-images.githubusercontent.com/107441403/203444260-a06e3d34-419f-4a68-abef-0e803d1edc70.png">

### 2. Creating a Class Diagram to Input.
Refer to the Overview of USE section above for a demo of how to create UML class diagrams. Alternatively, you can create a class diagram using any other UML tool and extract it as an XMI file that can then be opened using TPV. 

### 3. Choosing a Class Diagram for Analysis.
The first input of TPV is the class diagram to be analyzed. Click *Select* (TPV Main Window, 1), which opens the following window. TPV can take UML class into the following two formats: 1) the USE specification format in saved in a .use files or 2) the standard UML format saved in .uml files. 

<img width="556" alt="Chooseuml" src="https://user-images.githubusercontent.com/107441403/203628591-c24e0259-759b-4e04-9128-d20059d5aa30.png">


Select the file containing the class diagram that will be analyzed and press *Open*.
### 4. Choosing a TOCL Temporal Property from a File.
The second input necessary is a TOCL temporal property. This can be inputted in different ways. The first is inputting a .tocl file containing a TOCL property (TPV Main Window, 2).
Click *Select*, which opens a window similar to the previous step that asks for a .tocl file.

<img width="554" alt="Choosetocl" src="https://user-images.githubusercontent.com/107441403/203629092-edc061bd-9ead-45f3-b686-ec69bda4afc8.png">

Select a file containing a temporal property to analyze against and press *Open*.
### 5. Specifying a TOCL Temporal Property.
It is also possible to input a TOCL temporal property by specifying it within the plug-in interface (TPV Main Window, 3). Clicking *Specify* opens the following window:

<img width="615" alt="SpecifyTOCL" src="https://user-images.githubusercontent.com/107441403/203629894-c3292989-b73f-49da-b32f-4c97c4fda99f.png">

The first specification method involves typing a TOCL property into the text box labeled *Enter TOCL temporal properties* (Specify TOCL Properties, a).
Alternatively, clicking the *Use Patterns* button (Specify TOCL Properties, d) will bring up the temporal pattern specification window.
This window offers a choice to use different temporal specification patterns as templates for defining TOCL properties. Specified properties can then be saved using the *Save to File* option. (Specify TOCL Properties, e).

To use a specified TOCL property for analysis, click *Apply* (Specify TOCL Properties, c). Any syntax errors generated by specified properties will be displayed in the dialog labeled *Feedback* (Specify TOCL Properties, b).

### 6. Using the Optimization Technique.
Additionally, there is the option to use the *Optimization Technique* included in the plug-in that can shorten the time needed to perform the analysis. Click the checkbox (TPV Main Window, 4) to use it.
### 7. Choosing a Configuration Method.
The next step is configuring the analysis (TPV Main Window, 5). There are two ways to configure the analysis. The first method is entering a new analysis configuration. The second method is using a previously defined configuration stored in a .properties file.
#### i. Creating a New Analysis Configuration
Creating an analysis configuration done by specifying a search-scope and search-depth for the analysis. Search-scope defines the maximum number of objects of each class that can be instantiated during analysis. Search-depth defines the maximum number of transitions considered for analysis.
Once scope and depth have been specified, it is possible to enter an advanced configuration mode. In this advanced mode, an individual analysis configuration can be created for each class and association present in the model.
#### ii. Using a Previously Defined Configuration
To use a previously created configuration, click on the *Configuration method* dropdown (TPV Main Window, 5) and select *Upload .properties file*.
The option *Enter a .properties File* should become visible. Click *Select* and choose the .properties file containing the desired analysis configuration.
### 8. Performing the Analysis.
Finally to perform the analysis and search for a counterexample, press *Validate*. You can also press *Cancel* to close the window.
<!-- ## Acknowledgement-->
<!--## Citation-->
## References
##### 1. Al-Lail, Mustafa, Ramadan Abdunabi, Robert B. France,  and Indrakshi Ray. "An Approach to Analyzing Temporal Properties in UML Class Models." In MoDeVVa@ MoDELS, pp. 77-86. 2013.
##### 2. Al-Lail, Mustafa. "A Framework for Specifying and Analyzing Temporal Properties of UML Class Models." In MoDELS (Demos/Posters/StudentResearch), pp. 112-117. 2013.
##### 3. Al-Lail, Mustafa, Ramadan Abdunabi, Robert B. France, and Indrakshi Ray. "Rigorous Analysis of Temporal Access Control Properties in Mobile Systems." In 2013 18th International Conference on Engineering of Complex Computer Systems, pp. 246-251. IEEE, 2013.
##### 4. Al-Lail, Mustafa, Wuliang Sun, and Robert B. France. "Analyzing behavioral aspects of UML design class models against temporal properties." In 2014 14th International Conference on Quality Software, pp. 196-201. IEEE, 2014.
##### 5. Al Lail, Mustafa. "A Unified Modeling Language Framework for Specifying and Analyzing Temporal Properties." PhD diss., Colorado State University, 2018.
##### 6. Al Lail, Mustafa, Antonio Rosales, Hector Cardenas, Lars Hamann, and Alfredo Perez. "Transformation of TOCL temporal properties into OCL." In Proceedings of the 25th International Conference on Model Driven Engineering Languages and Systems: Companion Proceedings, pp. 899-907. 2022.
##### 7. Cardenas, Hector, Zimmerman Ryan, Antonio Rosales Viesca, Mustafa Al Lail, and Alfredo J. Perez. "Formal UML-based Modeling and Analysis for Securing Location-based IoT Applications." In REUNS 2022: The 8th National Workshop for REU Research in Networking and Systems. 2022.
