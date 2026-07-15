# Aviation Accident Analysis

This project analyzes historical aviation accident data to identify the safest aircraft makes and models for commercial and private operations. By filtering for modern, active designs and categorizing them by passenger capacity, this analysis provides data-driven recommendations for fleet acquisition.

## Project Overview

To ensure the findings are statistically reliable and relevant to modern aviation, the analysis applies strict filtering criteria:
* **Modern Aircraft Only**: Limits data to modern, professionally built designs with a maximum lifetime of 40 years (filtering data from 1983 onwards)[cite: 3].
* **Statistical Robustness**: Excludes aircraft models with too few recorded incidents to ensure a solid sample size[cite: 3].
* **Capacity Categorization**: Splits aircraft into two distinct operational classes:
  * **Small Aircraft**: Fewer than 20 total occupants[cite: 3].
  * **Larger Passenger Aircraft**: 20 or more total occupants[cite: 3].

---

## Key Features of the Cleaning Script

The first phase of this project focuses on data cleaning and preparation (`clean_aviation_data.py` / Jupyter Notebook). The cleaning pipeline:
1. **Filters Timeline**: Restricts records to accidents occurring from 1983 to the present[cite: 3].
2. **Handles Missing Values**: Cleans and imputes critical columns like total occupants, injuries, and hull damage.
3. **Categorizes Capacity**: Segregates aircraft into "Small" (< 20 occupants) and "Large" (≥ 20 occupants) classes[cite: 3].
4. **Filters Low-Volume Models**: Drops models with low accident sample sizes to avoid statistical anomalies[cite: 3].

---

## Key Safety Findings

Based on the cleaned data, the safest performers in each category are:

### 1. Small Aircraft (< 20 Occupants)
*Evaluation threshold: Models with at least 20 recorded accidents to ensure data reliability[cite: 3].*

* **Boeing 777**: 0.0% average severe injury rate, 0.0% average hull destruction rate[cite: 3].
* **Airbus A320**: 1.67% average severe injury rate, 1.67% average hull destruction rate[cite: 3].
* **Boeing 737**: 2.11% average severe injury rate, 1.41% average hull destruction rate[cite: 3].

### 2. Large Aircraft (≥ 20 Occupants)
*Evaluation threshold: Models with at least 5 recorded accidents[cite: 3].*

* **Boeing 717-200**: 0.14% average severe injury rate, 0.0% average hull destruction rate[cite: 3].
* **Boeing 787**: 0.31% average severe injury rate, 0.0% average hull destruction rate[cite: 3].
* **Boeing 757-232**: 0.43% average severe injury rate, 0.0% average hull destruction rate[cite: 3].

---

## Getting Started

### Prerequisites
Make sure you have Python installed along with the following libraries:
* pandas
* numpy

You can install the requirements using:
```bash
pip install pandas numpy

