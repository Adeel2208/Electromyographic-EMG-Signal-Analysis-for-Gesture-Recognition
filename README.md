# Electromyographic (EMG) Signal Analysis for Gesture Recognition

## Overview

This project focuses on analyzing electromyographic (EMG) signals to recognize hand gestures. EMG signals capture electrical activity in muscles during movement and are widely used in applications such as rehabilitation, prosthetics, and gesture-controlled systems. By analyzing this data, we aim to classify different gestures based on muscle activity.
https://www.google.com/imgres?q=emg%20signals%20for%20gesture&imgurl=https%3A%2F%2Fwww.researchgate.net%2Fpublication%2F318410077%2Ffigure%2Ffig1%2FAS%3A614173788602392%401523441850907%2FArchitecture-of-the-implemented-hand-gesture-recognition-based-on-EMG-signal-acquisition.png&imgrefurl=https%3A%2F%2Fwww.researchgate.net%2Ffigure%2FArchitecture-of-the-implemented-hand-gesture-recognition-based-on-EMG-signal-acquisition_fig1_318410077&docid=9uIYh_dBS0pTbM&tbnid=gSyjVn1lqGj2dM&vet=12ahUKEwiws9uu3PWJAxUCSvEDHde2JhEQM3oECGkQAA..i&w=738&h=304&hcb=2&ved=2ahUKEwiws9uu3PWJAxUCSvEDHde2JhEQM3oECGkQAA
The pipeline includes:
- Preprocessing raw EMG signals.
- Combining multi-subject data into a unified dataset.
- Training machine learning models for gesture classification.

---

## Dataset Information

### Source:
The dataset includes EMG signals collected from multiple subjects performing different gestures. Each subject's data is stored in separate folders with time-series files representing muscle activity.

### Structure:
The dataset is organized as follows:
```
EMG_data_for_gestures-master/
├── Subject_01/
│   ├── 1_raw_data_timestamp.txt
│   └── 2_raw_data_timestamp.txt
├── Subject_02/
│   ├── 1_raw_data_timestamp.txt
│   └── 2_raw_data_timestamp.txt
...
└── Subject_36/
    ├── 1_raw_data_timestamp.txt
    └── 2_raw_data_timestamp.txt
```

### Features:
Each data file contains:
1. **Time (ms):** The timestamp of each data point.
2. **Channel Data:** EMG readings from multiple sensors (e.g., `channel1`, `channel2`, ...).
3. **Class:** Gesture label (e.g., "0" for rest, "1" for a specific gesture).
4. **Subject ID:** Identifier for the data source (e.g., `17`).

### Preprocessing:
- **Combining Multi-Subject Data:** All data files are unified into a single dataset for easier processing.
- **Data Cleaning:** Missing values and inconsistencies are handled.
- **Normalization:** EMG signal values are scaled for uniformity across channels and subjects.

---

## Why Is This Important?

Analyzing EMG signals is crucial for developing systems like:
1. **Prosthetic Devices:** Enabling intuitive control of artificial limbs.
2. **Rehabilitation:** Monitoring and enhancing muscle recovery post-injury.
3. **Gesture Control:** Building interfaces for hands-free control of devices.

This project aims to automate gesture recognition using EMG signals, paving the way for efficient and scalable solutions in these domains.

---

## Features

### Data Preprocessing
1. **Data Combination:**
   - Consolidated data from all subjects into a single CSV file for easier processing.
2. **Handling Missing Data:**
   - Identified and filled missing values to maintain dataset integrity.
3. **Feature Scaling:**
   - Normalized EMG signal data for consistent model input.

### Exploratory Data Analysis
- Visualized the EMG signal distribution across channels.
- Examined correlations between different sensors and gestures.

### Model Architecture
- **Machine Learning Models:**
  1. Logistic Regression
  2. Random Forest
  3. Support Vector Machines (SVM)
- **Deep Learning Models:**
  - A fully connected neural network for improved classification accuracy.

### Model Evaluation
- Metrics:
  1. Accuracy
  2. Precision
  3. Recall
  4. F1-Score
- Confusion Matrix for visualizing classification performance.

---

## Installation and Usage

### Prerequisites
Ensure the following dependencies are installed:
- Python (3.x)
- NumPy
- Pandas
- Matplotlib
- scikit-learn

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/adeel2208/emg-signal-analysis.git
   cd emg-signal-analysis
   ```
2. Install required libraries:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Project
1. **Preprocessing:**
   - Run the provided script to combine multi-subject data and clean it.
2. **Model Training:**
   - Train machine learning models on preprocessed data.
3. **Model Evaluation:**
   - Evaluate the trained models using accuracy and confusion matrices.

---

## Results

- **Best Model:** Random Forest
- **Performance Metrics:**
  - Accuracy: ~94%
  - F1-Score: ~92%
  - Precision: ~93%
  - Recall: ~91%

### Visual Insights:
- Visualized the EMG signal patterns for each gesture class.
- Confusion matrix indicates high precision for most gestures.

---

## Future Enhancements
1. **Real-Time Gesture Recognition:**
   - Implement a pipeline for real-time EMG signal classification.
2. **Deep Learning Models:**
   - Explore CNNs and RNNs for improved accuracy on time-series data.
3. **Enhanced Features:**
   - Incorporate temporal and frequency domain features for better classification.

---

## Contributing

To contribute to this project:
1. Fork the repository.
2. Create a branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add feature-name"
   ```
4. Push your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

## Contact

For questions or suggestions, please contact:

**Name:** Adeel Mukhtar  
**Email:** adeelmukhtar051@gmail.com  
**GitHub:** [adeel2208](https://github.com/adeel2208)  
**LinkedIn:** [Adeel Mukhtar](https://www.linkedin.com/in/adeel-mukhtar-174b71270/)  
