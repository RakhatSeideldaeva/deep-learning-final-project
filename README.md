Week 1 Report

What I did this week

1. I chose a dataset

I picked **Daily and Sports Activities Dataset** from UCI Machine Learning Repository.

Link: https://archive.ics.uci.edu/ml/datasets/Daily+and+Sports+Activities

What is in this dataset:
- 19 activities (sitting, standing, walking, running, stairs up, stairs down, cycling, etc.)
- 8 people (4 women, 4 men)
- 5 sensors on body (torso, right arm, left arm, right leg, left leg)
- Each sensor has 9 measurements (accelerometer, gyroscope, magnetometer)
- Total: 45 signals

Dataset size:
- 9120 samples
- Each sample: 125 time steps × 45 features

 2. I set up GitHub repository

I created these folders:

```
project-repo/
├── README.md
├── requirements.txt
├── data/
│   └── README.md
├── notebooks/
│   └── 01-eda.ipynb
├── src/
│   ├── data_loader.py
│   └── preprocessing.py
├── reports/
│   └── week-01.md
└── results/
```

3. I wrote code to load data

File `src/data_loader.py` does:
- Reads all text files
- Converts to numpy arrays
- Adds labels (which activity)
- Remembers person ID

4. I explored the data

In `notebooks/01-eda.ipynb` I:

Found out:
- No missing values
- All activities have same number of samples (480 each)
- 8 different people

Made plots:
- Time series graphs
- Activity distribution chart
- Correlation heatmap

What I learned:
- Sitting and moving activities are easy to separate
- Gyroscope sensors help tell similar activities apart
- Different people have slightly different signals

 5. I made a plan for models

Simple model (baseline):
- Random Forest classifier

Deep learning model:
- 1D CNN or LSTM

Split the data:
- 70% training
- 15% validation
- 15% test

Problems I had

1. Many files - 9120 files. Solution: I will load in batches
2. File names - Some folders had extra spaces. I fixed this when reading

Plan for next week

- Normalize the data
- Train Random Forest (baseline model)
- Write code for 1D CNN
- Get first results


