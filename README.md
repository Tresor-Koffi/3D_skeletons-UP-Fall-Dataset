# Improved UP-Fall Dataset

## Overview
This dataset contains improved skeletal data extracted from fall events and daily activities of 5 subjects.
The data is organized by subjects, and each subject contains CSV files named according to the pattern C1S1A1T1, where:
- **C**: Camera (1 or 2) # So C1 refer to the data extracted from  camera 1 data and C2 refer to data extracted from the camera 2
- **S**: Subject (1 to 5)
- **A**: Activity (1 to N, representing different activities)
- **T**: Trial (1 to 3)

Due to limitations in the pose estimation algorithm, sequences with less than 100 frames of extracted data were excluded to ensure data quality. As a result, some subjects may have fewer CSV files.

This dataset aims to facilitate research in fall detection, particularly focusing on the detecting impact within fall events. 
The improved data accuracy and comprehensiveness make it a valuable resource for developing and benchmarking fall detection algorithms.

## Structure
- `subject1/`: Contains CSV files for Subject 1.
  - `C1S1A1T1.csv`: Data from Camera 1, Activity 1, Trial 1 for Subject 1.
  - `C1S1A2T1.csv`: Data from Camera 1, Activity 2, Trial 1 for Subject 1.
  - `C1S1A3T1.csv`: Data from Camera 1, Activity 3, Trial 1 for Subject 1.
  - `C2S1A1T1.csv`: Data from Camera 2, Activity 1, Trial 1 for Subject 1.
  - `C2S1A2T1.csv`: Data from Camera 2, Activity 2, Trial 1 for Subject 1.
  - `C2S1A3T1.csv`: Data from Camera 2, Activity 3, Trial 1 for Subject 1.
- `subject2/`: Contains CSV files for Subject 2.
  - `C1S2A1T1.csv`: Data from Camera 1, Activity 1, Trial 1 for Subject 2.
  - `C1S2A2T1.csv`: Data from Camera 1, Activity 2, Trial 1 for Subject 2.
  - `C1S2A3T1.csv`: Data from Camera 1, Activity 3, Trial 1 for Subject 2.
  - `C2S2A1T1.csv`: Data from Camera 2, Activity 1, Trial 1 for Subject 2.
  - `C2S2A2T1.csv`: Data from Camera 2, Activity 2, Trial 1 for Subject 2.
  - `C2S2A3T1.csv`: Data from Camera 2, Activity 3, Trial 1 for Subject 2.
- `subject3/`, `subject4/`, `subject5/`: Similar structure as above, but may contain fewer CSV files due to the data extraction criteria mentioned above.

## How to Use
1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/improved-up-fall-dataset.git
    ```
2. **Navigate to the directory**:
    ```bash
    cd improved-up-fall-dataset
    ```

## Examples
Here's a simple example of how to load and inspect a sample data file using Python:
```python
import pandas as pd

# Load a sample data file for Subject 1, Camera 1, Activity 1, Trial 1
data = pd.read_csv('subject1/C1S1A1T1.csv')
print(data.head())
