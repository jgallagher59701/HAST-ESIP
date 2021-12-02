# HAST
Information about the High Altitude Sensor Technology (HAST) Project

## The HAST project
The HAST project is a collaboration between the Montana Technology University Departments of Biology and Electrical Engineering and OPeNDAP. 
The project aims to develop sensor technology that can be used to montor conditions in the alpine environment in near real-time. 

## Development at MTech
* https://github.com/mtech-ee/HighAltitudeSoilSensing


## Development at OPeNDAP
Here are five Github repositories for the HAST leaf node part of the project, all of them are publicly accessible. I don't use the Arduino IDE but instead use a tool PlatformIO that works with MS VisualStudio. It supports multi-file code, etc., and works pretty well with Segger J-Link debugger probes (Segger makes a $20-30 probe for educational use that I have).

* [soild sensor common](https://github.com/jgallagher59701/soil_sensor_common): This Arduino library enables communication between the HAST leaf node and a stand-in main node. The MTech main node could use this library at some point, making the integration work less painful. Note that this _will_ work easily with the Arduino IDE.
* [leaf node](https://github.com/jgallagher59701/HAST_leaf_node): This is the code for the leaf node.
* [leaf node PCB](https://github.com/jgallagher59701/HAST_leaf_node_pcb): The KiCAD files for the leaf node Printed Circuit Board.
* [leaf node data](https://github.com/jgallagher59701/HAST_leaf_node_data): A grab bag of data from various leaf node deployments. Also, in here there is a Jupyter notebook with calculations for the batter life of the leaf node based on current measurements of one copy of the node. The link for that notebook is here: [Compute_Leaf_Node_Current](https://github.com/jgallagher59701/HAST_leaf_node_data/blob/main/Compute_Leaf_Node_Current_2.ipynb). Github renders these notebooks so you don’t have to go through the tedium of running them yourself to see the results.
* [lora main node stand-in](https://github.com/jgallagher59701/HAST_lora_main): This is the code for my main node stand-in. It dumps data to an SD card and to the serial port. Included is a python program to read from said serial port and write the info to a CSV file.

Here’s a graph from the notebook in bullet #4. In the notebook I show how the data from the scope is filtered, etc.
