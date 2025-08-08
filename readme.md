# Predict Accident Severity

This project focuses on analyzing and predicting the severity of road accidents using a dataset derived from the [US Accidents (March 2023)](https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents) dataset. The primary goal is to build a machine learning pipeline that preprocesses real-world accident data and applies stratified sampling to ensure balanced representation of severity classes in the training data.

## Project Structure

- **stratified.ipynb**: Performs efficient stratified sampling on a 10% sample of the full dataset using Dask and scikit-learn, and saves the output as `stratified_sample.csv`.
- **main.ipynb**: Loads and cleans the stratified dataset, drops irrelevant or high-nullity columns, parses time features, and prepares the data for model training.

## Dataset

- **Source**: US Accidents (March 2023) — a comprehensive dataset containing road accident reports across the United States.
- **Columns Used**:
  - Start_Time, End_Time, Start_Lat, Start_Lng, Severity, Temperature(F), Humidity(%), Pressure(in), Visibility(mi), Wind_Direction, Wind_Speed(mph), Weather_Condition
- **Dropped Features**: ID, Description, Location metadata, Timezone information, and others deemed non-informative or with high missing values.

## Technologies Used

- Python
- Pandas
- Dask
- scikit-learn

## Goals

- Apply **stratified sampling** on a massive dataset using scalable tools (Dask).
- Preprocess temporal and meteorological features effectively.
- Prepare a clean, balanced dataset for building predictive models.

## How to Use

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/predict-accident-severity.git
    cd predict-accident-severity
    ```

2. Ensure the `US_Accidents_March23.csv` dataset is available in the root directory.

3. Run the Jupyter Notebooks in the following order:
    - `stratified.ipynb` (to generate `stratified_sample.csv`)
    - `main.ipynb` (to clean and explore the sampled data)

