# IMDb Top 250 Movie Rating Predictor

## Project Overview
This project analyzes and predicts IMDb ratings of top movies using features such as **Genre, Runtime, Year, and Director**.  
It also classifies movies into **Hit or Flop** based on IMDb rating.

### Goal:
- Predict IMDb ratings using machine learning (Regression).  
- Classify movies as Hit/Flop using classification models.  
- Understand which features (Genre, Director, Runtime) affect movie ratings.  

---

## Dataset
- The dataset contains **218 movies** out of IMDb Top 250.  
- **Columns:** `Title`, `Year`, `Genre`, `Runtime`, `Director`, `IMDb_Rating`, `RT_Score`.  
- **Important:** The dataset was **manually created using OMDb API with my personal API key**.  
  - Some movies could not be fetched due to missing or regional data.  
  - This demonstrates significant effort in **programmatically fetching, cleaning, and compiling data**.  
- **CSV File:** `IMDb_Top250.csv`

---

## Folder Structure 

IMDb_Top250_Project/
├── README.md
├── IMDb_Top250.csv 
├── IMDb_Top250_Predictor.ipynb
├── images
│ ├── genre_rating.png
│ ├── year_trend.png
│ ├── hit_flop_cm.png
│ └── feature_importance.png
├── RandomForest_Regression_Model.pkl 
└── LogisticRegression_HitFlop_Model.pkl

---

## Steps Performed

### 1️⃣ Data Cleaning
- Year converted to integer, invalid entries fixed.  
- Runtime cleaned, missing values filled with median.  
- Director missing values filled with 'Unknown'.  
- IMDb ratings missing rows dropped.  
- RT_Score converted to numeric (optional for later use).  

### 2️⃣ Exploratory Data Analysis (EDA)
- IMDb rating distribution  
- Genre-wise average rating  
- Year-wise movie count  
- Top directors by average rating  
- Visualizations: Bar charts, line plots, wordclouds  

### 3️⃣ Feature Engineering
- Top 10 directors kept, rest labeled 'Other'  
- One-hot encoding applied to Genre and Director  

### 4️⃣ Regression Models (Predict IMDb Rating)
- **Linear Regression**  
- **Random Forest Regression**  
- Performance metrics: R² score, MSE  
- Visualization: Predicted vs Actual ratings  
- **Model saved** as `RandomForest_Regression_Model.pkl`

### 5️⃣ Classification Models (Hit / Flop)
- Logistic Regression  
- Accuracy and classification report checked  
- Confusion matrix visualization  
- **Model saved** as `LogisticRegression_HitFlop_Model.pkl`  

### 6️⃣ Visualizations
- Predicted vs Actual Ratings (Regression)  
- Feature Importance (Random Forest)  
- Confusion Matrix (Hit/Flop)  
- Year-wise avg rating trend  
- Genre vs Avg Rating Wordcloud  

---

## Key Insights
- Certain genres consistently have higher IMDb ratings.  
- Top directors strongly influence ratings.  
- Runtime has moderate impact on ratings.  
- Random Forest outperforms Linear Regression in predicting IMDb ratings.  
- Classification model accurately predicts Hit/Flop for most movies.  

---

## Technologies & Libraries
- **Python:** Pandas, Numpy  
- **Visualization:** Matplotlib, Seaborn, Wordcloud  
- **Machine Learning:** Scikit-learn (Linear Regression, Random Forest, Logistic Regression)  
- **Model Saving:** Joblib  

---

## How to Use
1. Clone this repository:  
```
git clone <your-repo-url>
```
2. Install dependencies:  
```
pip install -r requirements.txt
```
3. Open `IMDb_Top250_Predictor.ipynb` to explore EDA and models.  
4. Use saved models (`.pkl`) for future predictions without retraining.  

---

## Author / Dataset Credit
- **Author:** Shalini Saurav  
- Dataset manually created using **OMDb API** (personal API key).  
- Significant effort: programmatically fetched data, cleaned, and compiled into CSV.  
- Visualizations and models designed by the author.  

---

## License
- Dataset and code created by the author.  
- Free to use for **educational and learning purposes**.
