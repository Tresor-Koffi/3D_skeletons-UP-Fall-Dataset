Improved UP-Fall Dataset

 Overview

This dataset aims to facilitate research in fall detection, particularly focusing on the precise detection of impact moments within fall events. The improved data accuracy and comprehensiveness make it a valuable resource for developing and benchmarking fall detection algorithms. The dataset contains improved skeletal data extracted from fall events and daily activities of 5 subjects performing falling sceniaros.

Data Collection

The skeletal data was extracted using a pose estimation algorithm, which processes images frames to determine the 3D coordinates of each joint. Sequences with less than 100 frames of extracted data were excluded to ensure the quality and reliability of the dataset. As a result, some subjects may have fewer CSV files.


CSV Structure

The data is organized by subjects, and each subject contains CSV files named according to the pattern C1S1A1T1, where:

C: Camera (1 or 2)
S: Subject (1 to 5)
A: Activity (1 to N, representing different activities)
T: Trial (1 to 3)



subject1/`: Contains CSV files for Subject 1.

C1S1A1T1.csv: Data from Camera 1, Activity 1, Trial 1 for Subject 1
  C1S1A2T1.csv: Data from Camera 1, Activity 2, Trial 1 for Subject 1
  C1S1A3T1.csv: Data from Camera 1, Activity 3, Trial 1 for Subject 1
  C2S1A1T1.csv: Data from Camera 2, Activity 1, Trial 1 for Subject 1
  C2S1A2T1.csv: Data from Camera 2, Activity 2, Trial 1 for Subject 1
   C2S1A3T1.csv: Data from Camera 2, Activity 3, Trial 1 for Subject 1



subject2/`: Contains CSV files for Subject 2.

C1S2A1T1.csv: Data from Camera 1, Activity 1, Trial 1 for Subject 2
C1S2A2T1.csv: Data from Camera 1, Activity 2, Trial 1 for Subject 2
C1S2A3T1.csv: Data from Camera 1, Activity 3, Trial 1 for Subject 2
C2S2A1T1.csv: Data from Camera 2, Activity 1, Trial 1 for Subject 2
C2S2A2T1.csv: Data from Camera 2, Activity 2, Trial 1 for Subject 2
C2S2A3T1.csv: Data from Camera 2, Activity 3, Trial 1 for Subject 2

subject3/, subject4/, subject5/: Similar structure as above, but may contain fewer CSV files due to the data extraction criteria mentioned above.



Column Descriptions

Each CSV file contains the following columns representing different skeletal joints and their respective coordinates in 3D space:

Column Name

	

Description




joint_1_x

	

X coordinate of joint 1




joint_1_y

	

Y coordinate of joint 1




joint_1_z

	

Z coordinate of joint 1




joint_2_x

	

X coordinate of joint 2




joint_2_y

	

Y coordinate of joint 2




joint_2_z

	

Z coordinate of joint 2




...

	

...




joint_n_x

	

X coordinate of joint n




joint_n_y

	

Y coordinate of joint n




joint_n_z

	

Z coordinate of joint n




LABEL

	

Label indicating impact (1) or non-impact (0)

Example

Here is an example of what a row in one of the CSV files might look like:

joint_1_x

	

joint_1_y

	

joint_1_z

	

joint_2_x

	

joint_2_y

	

joint_2_z

	

...

	

joint_n_x

	

joint_n_y

	

joint_n_33

	

LABEL




0.123

	

0.456

	

0.789

	

0.234

	

0.567

	

0.890

	

...

	

0.345

	

0.678

	

0.901

	

0



Usage

This data can be used for developing and benchmarking impact fall detection algorithms. It provides detailed information on human posture and movement during falls, making it suitable for machine learning and deep learning applications in impact fall detection and prevention.



 Using github


1. Clone the repository:

    -bash
    git clone

https://github.com/Tresor-Koffi/IMPROVED-UP-FALL-DATASET

  
2. Navigate to the directory:

    -bash
    -cd improved-up-fall-dataset
  

Examples

Here's a simple example of how to load and inspect a sample data file using Python:
```python
import pandas as pd

# Load a sample data file for Subject 1, Camera 1, Activity 1, Trial 1

data = pd.read_csv('subject1/C1S1A1T1.csv')
print(data.head())

