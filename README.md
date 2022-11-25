# STMTransformation
Short description.
---
## Installation Instructions
## Usage Instructions
<img width="717" alt="MainWindow" src="https://user-images.githubusercontent.com/107441403/203444260-a06e3d34-419f-4a68-abef-0e803d1edc70.png">
### 1. Choosing a Class Diagram to Input.
The first input necessary is the class diagram to be analyzed. Click *Select*, which opens a window similar to the following

<img width="556" alt="Chooseuml" src="https://user-images.githubusercontent.com/107441403/203628591-c24e0259-759b-4e04-9128-d20059d5aa30.png">

Select a class diagram to analyze and press *Open*.
### 2. Choosing a TOCL Temporal Property from a File.
The second input necessary is a TOCL temporal property. This can be inputted in different ways; this is the first. Click *Select*, which opens a window similar to the previous step that asks for a .tocl file.

<img width="554" alt="Choosetocl" src="https://user-images.githubusercontent.com/107441403/203629092-edc061bd-9ead-45f3-b686-ec69bda4afc8.png">

Select a file containing a temporal property to analyze against and press *Open*.
### 3. Specifying a TOCL Temporal Property.
It is also possible to input a TOCL temporal property by specifying it within the plug-in interface. Clicking *Specify* opens the following window:

<img width="615" alt="SpecifyTOCL" src="https://user-images.githubusercontent.com/107441403/203629894-c3292989-b73f-49da-b32f-4c97c4fda99f.png">

### 4. Using the Optimization Technique.
Additionally, there is the option to use the *Optimization Technique*, which can shorten the time needed to perform the analysis. Click the checkbox to use it.
### 5. Choosing a Configuration Method.
The next step is configuring the analysis. There are two ways to configure the analysis. The first method is entering a new analysis configuration. The second method is using a previously defined configuration stored in a .properties file.
#### i. Creating a New Analysis Configuration
Creating an analysis configuration done by specifying a search-scope and search-depth for the analysis. Search-scope defines the maximum number of objects of each class that can be instantiated during analysis. Search-depth defines the maximum number of transitions considered for analysis.
Once scope and depth have been specified, it is possible to enter an advanced configuration mode. In this advanced mode, an individual analysis configuration can be created for each class and association present in the model.
#### ii. Using a Previously Defined Configuration
### 6. Performing the Analysis.
Finally to perform the analysis and search for a counterexample, press *Validate*. You can also press *Cancel* to close the window.
## Acknowledgement
## Citation
## References
