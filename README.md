# SpaceX Falcon 9 Landing Prediction

## 1. Executive Summary
This project aims to predict the successful landing of the SpaceX Falcon 9 first stage. By analyzing historical launch data, we determine the factors that contribute to a successful landing. This predictive capability is crucial for estimating the cost of a launch, as the ability to reuse the first stage significantly reduces the price of space access.

The project follows a structured data science methodology, ranging from data collection via the SpaceX API to machine learning model deployment.

## 2. Project Objectives
* **Data Collection:** Retrieve launch data from the SpaceX REST API.
* **Data Wrangling:** Clean and process the dataset to handle missing values and filter for Falcon 9 launches.
* **Exploratory Data Analysis (EDA):** Visualize relationships between variables (e.g., Payload Mass vs. Launch Site) to identify patterns.
* **Predictive Modeling:** Train and evaluate classification algorithms to predict landing outcomes (Success/Failure).

## 3. Methodology

### Data Acquisition
Data is gathered using the public SpaceX API. The raw data includes flight numbers, launch dates, booster versions, payload details, orbit parameters, launch sites, and landing outcomes.

### Data Preprocessing
* Filtering data to include only Falcon 9 launches.
* Handling missing values in payload mass and orbit columns.
* Classifying landing outcomes into binary categories:
    * **1 (Success):** The booster landed successfully on a drone ship or ground pad.
    * **0 (Failure):** The booster crashed, landed in the ocean, or was not planned to be recovered.

### Visual Analysis
Key visualizations include:
* Flight Number vs. Launch Site
* Payload Mass vs. Launch Site
* Success Rate by Orbit Type
* Yearly Success Rate Trends

## 4. Technical Architecture

### Technologies Used
* **Programming Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn
* **Development Environment:** Jupyter Notebook

### Machine Learning Models
The following classification algorithms were evaluated to determine the best predictor for landing success:
1.  Logistic Regression
2.  Support Vector Machine (SVM)
3.  Decision Tree Classifier
4.  K-Nearest Neighbors (KNN)

## 5. Usage Instructions

### Prerequisites
Ensure Python is installed along with the required libraries.

### Installation
1.  Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/spacex-landing-prediction.git](https://github.com/yourusername/spacex-landing-prediction.git)
    ```
2.  Navigate to the project directory:
    ```bash
    cd spacex-landing-prediction
    ```
3.  Install dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```

### Running the Analysis
The project is divided into Jupyter Notebooks for each stage of the pipeline. To run the analysis:

```bash
jupyter notebook