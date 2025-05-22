# Project-Progress-1
date: 24-04-25
------------------------------------------------------------------------------------------------------------------------------
First, we downloaded our datasets and examined the number of rows and columns, reviewed the column headers and identified the suitable machine learning algorithm which was classification. Next, we proceeded with data cleaning, where we eliminated variables (columns) that recorded certain datasets which were not commonly employed in the exisiting buildings automation system. From this, the number of variables decreased from 30 to 20 in the steps to follow. 
Next, we divided our dataset into five classes: Outdoor Air Temperature Sensor Bias, Supply Air Temperature Sensor Bias, OA Damper, Cooling Coil Valve, and Fault-Free where we chose to explore the raw data based on its fault intensity. For instance,
21 separate datasets were provided, each indicating their fault type and fault intensities. 20 of these datasets were data that contained the faults in which we then compared these data to the Fault-Free dataset.
------------------------------------------------------------------------------------------------------------------------------
# EXPLORING RAW DATA
In exploring the raw data, we separated the 21 datasets into their respective classes by fault type, for example, Outdoor Air Temperature Sensor Bias obtains 4 files and is categorized to its sensor readings (Bias: 2 deg, Bias: 4 deg, Bias:-2 deg, Bias: -4 deg). The same procedure was done for all the other classes.  
The datasets were loaded into Matlab then combined into 5 separate classes according to its fault name and intensity. 
After merging the dataset, it was executed in MATLAB to perform the analysis. 
Using the scatter plot function, the 20 variables(columns) were plotted against the time variable to determine how the recorded data changed according to time variable. The data was graphed into the 4 Fault classes and each graph included the plots of the different fault intensities. 
Next, the 4 classes were plotted against the Fault Free data to visualize how the Fault classes differed from the Fault free data. 
------------------------------------------------------------------------------------------------------------------------------
# FEATURE EXTRACTION
As our dataset takes 1 minute interval in recording the data at different zones, therefore we had to sample the time accordingly to it fault type in order to calculate and extract features. So we calculated and extracted 15 statistical time domain features which includes mean,  maxim value, root mean square, square Root mean, standard deviation, variance, shape factor(RMS), shape factor(SRM), crest factor, latitude factor, impulse factor, skewness, kurtosis, normalised 5th central moment and normalised 6th central moment. Afterwards it was plotted in a bar graph to clearly visualize how each feature vary for all the fault types.
------------------------------------------------------------------------------------------------------------------------------
# STEPS IN EXCUTING THE MATLAB SCRIPTS
Files name and Functions
statisticalFeatures - A function file for calculating the 15 features from an input signal(x)

FEATURES_CALCS - The dataset (COMBINE_TABLE.mat), which includes sensor readings and the corresponding fault type labels, is processed by this script. It groups the dataset's numerical variables according to every individual fault type and extracts 15 statistical features from each one.

GRAPHS_FOR_STATISTICAL_FEATURES - This script basically plots a bar graph to clearly visualize how each feature vary in different fault types.

EDA - This script performs exploratory data analysis (EDA) on a table of (SFeaturesByFault) classified by its faut type to visualize the distribution of features, understand relationships between them, and observe how features vary across different fault types using correlation matrix and boxplot.

PCA - Principal Component Analysis (PCA) is carried out using this script on statistical features that have been taken from signals in order to: reduce dimensionality, visualize clusters by its fault types and understand feature contributions

NeuroNetwork: In order to categorize fault types using statistical features taken from sensor or signal data, this script creates a supervised classification process making use of feedforward neural network. It includes preprocessing, data splitting, model definition, training, evaluation, and visualization of results.

STEPS:
1: Load the dataset into the workspace, file name (COMBINE_TABLE.MAT). Note: This COMBINE_TABLE has already removed data points that was not commonly used in the building.

2: Run FEATURES_CALCS.mlx in order to extract and calculate feature from the statisticalFeatures function.

3: Run GRAPHS_FOR_STATISTICAL_FEATURES.mlx for a better visualization of the extracted feature

4: Run EDA.mlx  to observe how features vary across different fault types by plotting graphs

5: Run PCA.mlx where it normalizes the extracted features to reduce dimesionality

6: Run NeuroNetwork.mlx to train our model by splitting our dataset into 60% train, 30% test, 10% test.

