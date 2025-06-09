# Topic - Carbon Footprint Estimator (AI/ML Regression Project)

This project uses a machine learning model to estimate weekly carbon emissions (kg/week) based on lifestyle choices such as diet, transport, and heating energy source.

**Dataset Used**:  Carbon Emission.csv

- **Features**:
  - Diet (e.g., meat, vegetarian, vegan)
  - Transport` (e.g., Private, public)
  - Heating Energy Source (e.g., gas, coal, electricity)

- **Target**:
  - CarbonEmission (monthly CO₂ emissions in kg, converted to weekly)



## Approach 

1. **Data Loading**: Used pandas to load and inspect the dataset.

2. **Data Cleaning**: Removed rows with missing values.

3. **Feature Engineering**:
   - Applied OneHotEncoder to categorical inputs.
   - Converted emissions from monthly to weekly by dividing by 4.3.
   - We use 4.3 because it's the average number of weeks in a month.
   - In a year has 12 months and 52 weeks. So, 52/12= 4.3

4. **Model Training**:
   - Used RandomForestRegressor from sklearn.
   - Trained the model on 80% of the data.

5. **Evaluation**:
   - Used Mean Squared Error to evaluate performance.
   - Visualized results using a scatter plot of actual vs. predicted values.

## Dependencies

- pandas — Data manipulation and cleaning
- matplotlib — Plotting visualizations
- seaborn — Enhanced statistical plotting
- scikit-learn — Machine learning tools:
  - train_test_split
  - OneHotEncoder
  - RandomForestRegressor
  - mean_squared_error

## Visualization

- A scatter plot compares actual vs predicted CO₂ emissions.
- A red dashed line represents perfect prediction (y = x).
- Dots closer to the line mean more accurate predictions.
