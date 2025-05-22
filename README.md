# Project-Progress-1
date: 24-04-25
----------------------------------------
First, we downloaded our datasets and examined the number of rows and columns, reviewed the column headers and identified the suitable machine learning algorithm which was classification. Next, we proceeded with data cleaning, where we eliminated variables (columns) that recorded certain datasets which were not commonly employed in the exisiting buildings automation system. From this, the number of variables decreased from 30 to 20 in the steps to follow. 
Next, we divided our dataset into five classes: Outdoor Air Temperature Sensor Bias, Supply Air Temperature Sensor Bias, OA Damper, Cooling Coil Valve, and Fault-Free where we chose to explore the raw data based on its fault intensity. For instance,
21 separate datasets were provided, each indicating their fault type and fault intensities. 20 of these datasets were data that contained the faults in which we then compared these data to the Fault-Free dataset.
# Exploring Raw Data
In exploring the raw data, we separated the 21 datasets into their respective classes by fault type, for example, Outdoor Air Temperature Sensor Bias obtains 4 files and is categorized to its sensor readings (Bias: 2 deg, Bias: 4 deg, Bias:-2 deg, Bias: -4 deg). The same procedure was done for all the other classes.  
The datasets were loaded into Matlab then combined into 5 separate classes according to its faulty name and intensity. 
After merging the dataset, it was executed in MATLAB to perform the analysis. 
Using the scatter plot function, the 20 variables(columns) were plotted against the time variable to determine how the recorded data changed according to time variable. The data was graphed into the 4 Fault classes and each graph included the plots of the different fault intensities. 
Next, the 4 classes were plotted against the Fault Free data to visualize how the Fault classes differed from the Fault free data. 
