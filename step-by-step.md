---
permalink: /step-by-step/
title: Step-by-step tutorial walkthrough
layout: post
---

## Hands-on Activity 1

### Prerequisites
Please download the following two .csv files for this activity:
- [data_TCS183.csv](session_files/session1/data_TCS183.csv)
- [data_TrafficData.csv](session_files/session1/data_TrafficData.csv)

### Exercise 1 - Reproducibility Motivation

#### Part 1: Analyze + Document

Complete the following tasks and write instructions/documentation for your collaborator to reproduce your work:

1. Download the original dataset (data_TCS183.csv) using the link provided in the tutorial webpage. Visualize ‘Total’ traffic from 13/06/2008 to 20/06/2008 using a line plot

2. The plotted dataset contains some error. Can you spot it?​ Replace the erroneous point (replace the erroneous value with the correct value = 181) in the data and plot the ‘Total’ traffic for visualization.​

3. Download another dataset (data_TrafficData.csv) from the tutorial webpage. Please create a scatter plot describing the ‘Total flow’ vs. ‘Total density’. ​

4. Once the scatter plot is created, please calculate the free flow velocity, using your choice of model (you may assume a triangular fundamental diagram).

```python
# Import necessary packages
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```


```python
##### TASK 1: Visualise ‘Total’ traffic from 13/06/2008 to 20/06/2008 using a line plot #####
#####-----------------------------------------------------------------------------------#####

# Load the CSV file into a DataFrame, specifying the correct header row
file_path = 'data_TCS183.csv'  
df_1 = pd.read_csv(file_path, header=1)  # Use the second row (index 1) as header

# Display the first few rows of the DataFrame to check
print(df_1.head())
```

Output 

## Hands-on Activity 2