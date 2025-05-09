# Calories Burnt Prediction using Machine Learning

## Project Overview

This project implements a machine learning model to predict calories burned during exercise based on features such as gender, age, height, weight, exercise duration, and heart rate. The dataset used is `calories.csv`, and the model is built using a RandomForestRegressor from scikit-learn. A user-friendly interface is provided using Gradio for interactive predictions.

## Dataset

- **File**: `calories.csv`
- **Columns**:
  - `User_ID`: Unique identifier for each user
  - `Gender`: Male or Female
  - `Age`: Age in years
  - `Height`: Height in centimeters
  - `Weight`: Weight in kilograms
  - `Duration`: Exercise duration in minutes
  - `Heart_Rate`: Heart rate in beats per minute (bpm)
  - `Body_Temp`: Body temperature in degrees Celsius
  - `Calories`: Target variable (calories burned)

## Key Findings

- **Correlations**:
  - Strong positive correlation between `Calories` and `Duration` (0.95)
  - Strong positive correlation between `Calories` and `Heart_Rate` (0.90)
  - Moderate positive correlation between `Calories` and `Age` (0.16)
- **Outliers**: Detected and removed using the Interquartile Range (IQR) method for numerical features.
- **Gender Distribution**: Nearly even distribution of male and female participants.

## Project Structure

- **Notebook**: `Calories_Burnt_Prediction_using_Machine_Learning (1).ipynb`
  - Data loading and preprocessing
  - Exploratory data analysis (EDA)
  - Model training with RandomForestRegressor
  - Gradio interface for predictions
- **Dependencies**:
  - Python 3
  - pandas
  - scikit-learn
  - gradio
  - matplotlib (optional for visualizations)

## Installation

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install dependencies:

   ```bash
   pip install pandas scikit-learn gradio
   ```

3. Ensure `calories.csv` is in the project directory.

## Usage

1. Run the Jupyter notebook:

   ```bash
   jupyter notebook Calories_Burnt_Prediction_using_Machine_Learning\ (1).ipynb
   ```

2. Execute the cells to:

   - Load and preprocess the data
   - Train the RandomForestRegressor model
   - Launch the Gradio interface

3. Use the Gradio interface to input values for gender, age, height, weight, duration, and heart rate to predict calories burned.

## Model Details

- **Algorithm**: RandomForestRegressor
- **Parameters**:
  - `n_estimators=100`
  - `random_state=42`
- **Features**: `Gender` (encoded), `Age`, `Height`, `Weight`, `Duration`, `Heart_Rate`
- **Target**: `Calories`
- **Train-Test Split**: 80% training, 20% testing

## Next Steps

- **Model Improvement**: Experiment with other algorithms (e.g., XGBoost, Gradient Boosting) or hyperparameter tuning.
- **Feature Engineering**: Incorporate `Body_Temp` or derived features like BMI.
- **Outlier Analysis**: Explore alternative outlier detection methods for robustness.
- **Deployment**: Host the Gradio app on a permanent server for public access.

## Requirements

- Python 3.6+
- Jupyter Notebook
- Libraries: See `Installation` section

## License

This project is licensed under the MIT License.

## Acknowledgments

- Dataset source: `calories.csv` (not provided in the repository; ensure you have it)
- Built with scikit-learn and Gradio
![image](https://github.com/user-attachments/assets/de6c3e89-dacb-4154-8876-ee8a42b5880d)
