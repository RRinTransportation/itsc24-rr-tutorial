---
permalink: /step-by-step/
title: Step-by-step tutorial walkthrough
layout: post
date: 2024-10-13 10:00:00
author: ["Bidisha Ghosh","Hoa Xuan Nguyen","Cathy Wu", "Junyi Ji"]
---

## Hands-on Activity 1

### Prerequisites
Please download the following two .csv files for this activity:
- [data_TCS183.csv](https://www.rerite.org/itsc24-rr-tutorial/session_files/session1/data_TCS183.csv)
- [data_TrafficData.csv](https://www.rerite.org/itsc24-rr-tutorial/session_files/session1/data_TrafficData.csv)

### Reproducibility Motivation

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

**TASK 1**: Visualise 'Total' traffic from 13/06/2008 to 20/06/2008 using a line plot

```python
# Load the CSV file into a DataFrame, specifying the correct header row
file_path = 'data_TCS183.csv'  
df_1 = pd.read_csv(file_path, header=1)  # Use the second row (index 1) as header

# Display the first few rows of the DataFrame to check
print(df_1.head())
```

Select the 'Time' and 'Total' columns to create a shorten dataframe, do all data processing on newly created dataset, remove redundant columns

```python
df_1_shorted = df_1[['Time', 'Total']]

# Create new DataFrame for the given tasks
df_1_shorted = pd.DataFrame(df_1_shorted)
# Convert 'Time' column to datetime
df_1_shorted['Time'] = pd.to_datetime(df_1_shorted['Time'], dayfirst = True)
# Set 'Time' as the index
df_1_shorted.set_index('Time', inplace=True)
print(df_1_shorted)
```

**TASK 2**: Replace the erroneous point 
```python
# First, identify the incorrect data
incorrect_value = 5181
correct_value = 181
incorrect_date = '2008-06-19'

# Locate the row with the incorrect value on the specified date
df_1_shorted.loc[(df_1_shorted.index.date == pd.to_datetime(incorrect_date).date()) & (df_1_shorted['Total'] == incorrect_value), 'Total'] = correct_value
df_1_filtered_corrected = df_1_shorted.loc[start_date:end_date]
```

```python
# Plot the data
plt.figure(figsize=(12, 6))
plt.plot(df_1_filtered.index, df_1_filtered_corrected['Total'], linestyle='-')
plt.title('Total Traffic Flow from 13/06/2008 to 20/06/2008')
plt.xlabel('Time')
plt.ylabel('Total (veh/hr)')
plt.grid(True)
plt.savefig(f'Corrected Total Traffic Flow Over Time.png')
plt.show()
```

**TASK 3**: Create a scatter plot describing the ‘Total flow’ vs. ‘Total density’.

```python
# Load the CSV file into a DataFrame
file_path_2 = 'data_TrafficData.csv' 
df_2 = pd.read_csv(file_path_2) 
# Display the first few rows of the DataFrame to confirm the correct header is used
print(df_2.head())
```

```python
# Select the last two columns, removing redundant columns
df_2_shorted = df_2[['Total density (veh/km)', 'Total flow (veh/hr)']]
# Display the new DataFrame
print(df_2_shorted)
```

```python
# Create scatter plot
plt.figure(figsize=(10, 6))
plt.scatter(df_2_shorted['Total density (veh/km)'], df_2_shorted['Total flow (veh/hr)'], linestyle='-')
plt.title('Traffic Flow vs Density')
plt.xlabel('Total density (veh/km)')
plt.ylabel('Total flow (veh/hr)')
plt.grid(True)
plt.savefig(f'Traffic Flow vs Density.png')
plt.show()
```

**TASK 4**: Calculate the free flow velocity.
```python
# Greenshield’s macroscopic stream model for calculations of free stream velocity ($v_f$) and density jam ($k_j$)
# 1. From q_max, get the corresponding k_max
# Find the index of the maximum value in 'Total flow (veh/hr)'
q_max = df_2_shorted['Total flow (veh/hr)'].max()
print("Maximum flow (q_max): ", q_max)
q_max_index = df_2_shorted['Total flow (veh/hr)'].idxmax()
# Find the corresponding value in 'Total density (veh/m/lane)'
k_max = df_2_shorted['Total density (veh/km)'].iloc[q_max_index]
# Display the results
print("The corresponding density to maximum flow (k_maxflow)': ", k_max)

# 2. Calculation of the jam density (k_j = k_0 * 2) 
k_j = k_max * 2
print('\nJam density (veh/km) (k_j = k_maxflow * 2) = ', k_j)

# 3. Calculation of the free flow velocity 
v_f = q_max * 4 / k_j
print('\nFree speed (km/lane/h) (v_f = q_max * 4 / k_j) = ', v_f) 
```


```python
# Recreate scatter plot with slope lines
plt.figure(figsize=(10, 6))
plt.scatter(df_2_shorted['Total density (veh/km)'], df_2_shorted['Total flow (veh/hr)'], alpha=0.7, label='Data')
plt.plot([k_max, 0], [q_max, 0], color='red', linestyle='--')
plt.text(k_max, q_max, f"Critical Point (q_max={q_max:.2f}, k_maxflow={k_max:.2f})",
         horizontalalignment='left', verticalalignment='bottom')
# Add title and labels
plt.title('Fundamental diagram')
plt.xlabel('Total Density (veh/km)')
plt.ylabel('Total Flow (veh/hr)')
plt.legend(loc = 'lower right')
plt.grid(True)
plt.savefig(f'Greenshield stream model.png')
plt.show()
```

#### Part 2: Exchange document and discussion

Introduce yourself to your collaborator and tell them why you're here.​

Exchange your notes for completing tasks with your collaborator. Attempt to replicate your collaborator’s work reproducing the figures s/he has produced preferably using the software that s/he used.​

Afterwards, discuss the difficulties you encountered and the reasons you were or weren't able to replicate their work.

#### Discussion

- Which software did you use for data analysis (e.g., Excel, R, Python, MATLAB, etc.)?​

- What tool did you use for documenting your work (e.g., Word, LaTeX, plain text, etc.)?​

- Was your partner able to successfully reproduce your work?​

- Did you need to use the same software as your partner to reproduce their work?​

- What were the primary challenges you encountered while reproducing your partner's work?​

- What key factors contributed to successfully reproducing your partner's work?

### Four aspects of reproducibility:

1. Documentation: details of you code, model, algorithm, data, helps for running your code.

2. Organization: save data in clear structure, easily to double-check and use, separate raw and processed data, save code in separate folder.

3. Automation: reduce audience effort to manipulate/edit your code to make it work, no effort is the best

4. Dissemination: your research journal, data, code, algorithm are reproducible. How to maintain these materials assessable?

## Hands-on Activity 2