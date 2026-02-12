# EE7209 Machine Learning Project

## Human Activity Recognition

### Author

Ahameth Aathil

### Description

This project implements a deep learning model for human activity recognition (HAR) using accelerometer readings. The dataset consists of six activities:

- Cycling
- Pushup
- Run
- Squat
- Table Tennis
- Walk

Each activity is recorded in a separate `.csv` file. Data is collected at 40 Hz (one sample every 25 ms) using five accelerometers. Each accelerometer provides three readings (X, Y, Z), resulting in 15 features per data sample.

The project aims to identify an activity given a **sequence of consecutive snapshots** rather than a single snapshot. Each sequence consists of `K` consecutive rows from the dataset.

### Tools Used

- Python
- TensorFlow / PyTorch
- Scikit-learn
- Jupyter Notebook / Google Colab

### Project Tasks

1. **Deep Learning Model**  
   - Choose an appropriate deep learning model (e.g., LSTM, GRU, 1D-CNN) to classify activities based on sequences of sensor readings.
   - Train the model on generated sequences of length `K`.
   - Evaluate model performance using metrics such as accuracy, F1-score, or confusion matrix.

2. **Deployment on Hugging Face Spaces**  
   - Load the trained model into Hugging Face Spaces.
   - Create a simple GUI to allow users to input a datapoint (via CSV, text, or copy-paste) and obtain predictions.

3. **Bonus Task (Optional)**  
   - Identify the pair of sensor devices (each providing three features) that gives the best classification performance.

### Dataset

The dataset is organized as follows:

| Activity       | File Size |
|----------------|-----------|
| Cycling        | 3,432 KB  |
| Pushup         | 587 KB    |
| Run            | 634 KB    |
| Squat          | 838 KB    |
| Table Tennis   | 4,827 KB  |
| Walk           | 1,309 KB  |

> Each `.csv` file contains accelerometer readings with columns representing the 15 features from five accelerometers (X, Y, Z axes).

### Deliverables

- **Google Colab Notebook** with code and explanations
- **PDF print** of the notebook
- **Hugging Face Space** link with the student ID
- **5-minute YouTube video** explaining the project

### Notes / Hints

- To generate sequences of length `K`, consider overlapping sequences with 50% overlap to increase training data and capture continuous movements.
- When creating a sequence, you can store just the starting index and dynamically read the consecutive rows from the original CSVs.
- You are **not required** to find the optimal `K` value or save all sequences permanently.

---

### Example Project Flow

1. Load `.csv` files for each activity
2. Generate sequences of length `K` with overlap
3. Split data into training and test sets
4. Train deep learning model (LSTM, GRU, or 1D-CNN)
5. Evaluate model performance
6. Deploy model on Hugging Face Spaces with a GUI for predictions
