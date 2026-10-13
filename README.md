# Python Anomaly Detection

## Project Description

This project implements a simple statistical anomaly detection algorithm in Python to identify unusual values in a one-dimensional dataset. It uses the **three-standard-deviation method** to detect observations that fall outside the range of three standard deviations from the mean.

Anomaly detection is useful in data analysis and machine learning for identifying unusual patterns, detecting suspicious observations, and understanding data quality.

## Objectives

- Understand statistical anomaly detection.
- Calculate the mean and standard deviation of a dataset.
- Establish upper and lower anomaly thresholds.
- Identify and return values that fall outside the defined limits.
- Explore a fundamental technique used in data preprocessing and exploratory data analysis.

## Technologies Used

- **Python**
- **Statistics module** — for calculating the mean and sample standard deviation.

## How It Works

The algorithm follows these steps:

1. Calculate the mean of the dataset.
2. Calculate the sample standard deviation.
3. Multiply the standard deviation by three to establish the cutoff.
4. Calculate the lower and upper limits.
5. Identify values outside these limits.
6. Return the detected anomalies.

The thresholds are calculated as follows:

- Lower limit = Mean − (3 × Standard Deviation)
- Upper limit = Mean + (3 × Standard Deviation)

Any value below the lower limit or above the upper limit is classified as an anomaly.

## Code Example

```python
import statistics

def find_anomalies(data):
    anomalies = []

    random_data_std = statistics.stdev(data)
    random_data_mean = statistics.mean(data)

    anomaly_cut_off = random_data_std * 3

    lower_limit = random_data_mean - anomaly_cut_off
    upper_limit = random_data_mean + anomaly_cut_off

    for outlier in data:
        if outlier > upper_limit or outlier < lower_limit:
            anomalies.append(outlier)

    return anomalies
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Vedline2547/Anomaly-detection.git
```

### 2. Navigate to the project directory

```bash
cd Anomaly-Detection
```

### 3. Run the Python script

```bash
python main.py
```

Ensure Python is installed on your computer before running the script.

## Applications

- Detecting unusual sensor readings.
- Identifying suspicious financial transactions.
- Analyzing engineering measurements.
- Detecting unexpected values during data preprocessing.
- Learning the statistical foundations of machine learning.

## Limitations

- The method works best when the data is approximately normally distributed.
- Extreme observations can influence the mean and standard deviation, potentially masking other anomalies.
- The function requires at least two numerical observations to calculate the sample standard deviation.
- An observation flagged as an anomaly is not necessarily an error; it may represent a genuine, rare event.

## Future Improvements

- Compare the three-standard-deviation method with the Interquartile Range (IQR) method.
- Add data visualization to highlight anomalies.
- Support datasets with multiple features.
- Explore machine learning techniques such as Isolation Forest.

## Author

**Vedline Ochieng**

GitHub: [@Vedline2547](https://github.com/Vedline2547)

## License

This project is available for educational and learning purposes. You may add an MIT License if you want to permit reuse under its terms.
