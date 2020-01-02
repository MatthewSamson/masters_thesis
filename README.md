# MASTERS_THESIS
Covers the code used in my master's thesis - SOM on distracted drivers

# Preprocess
Includes code to build the custom data transformation pipeline used to clean the raw data.

# Training
Includes code that trains the SOM models based on the required data. After training, the weights are stored. Then SOM mappings are generated and they are also stored.
SOM code is taken from the forked Minisom repository credited to . However a number of bugs in the training and parameter update algorithms were discovered which were then fixed.

# Mapping
Includes code that creates customized labels to be applied to the trained SOM mappings that have already been stored.
Also includes code on thresholding each SOM neuron based on the label that maximally activates it. This threshold is applied to determine each driver's unique pattern of points.

# Unique_Mapping
Includes code that was used to analyse the individual driver patterns. Analysis was done by re-applying labels and calculating the precentages of each class within an individual label.
Class within labels represent different driver behaviours, so the after calculating the percentages, it is possible to make comparisons between driver behaviours among different labels.
