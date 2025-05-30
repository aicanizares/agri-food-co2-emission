# Forecasting Global Temperature Rise Due to CO₂ Emissions

## Introduction  
Climate change is accelerating, with **31% of human-caused GHG emissions** originating from agri-food systems (UN, 2020). This project predicts **yearly temperature increases** based on CO₂ emissions data to support **policymakers & researchers** in climate strategies.

## Data Overview  
- **Source:** FAO, IPCC, Kaggle Dataset  
- **Years Covered:** 1990-2020 (31 years)  
- **Countries:** 175  
- **Features:** 31 variables (emissions, fires, food processing, transport, population)  

### **Data Challenges & Considerations**  
- **Missing Data:**  
  - NaN values in country emissions → Imputed mean for animal agriculture.  
  - Dropped countries with excessive missing values.  
- **Scaling:** MinMaxScaler used for normalization.  
- **Feature Selection:** Removed **low-correlation (<5%) & highly correlated (>80%)** features.  
- **Largest NaN Country:** Palestine (~5M people)  
- **Smallest NaN Country:** Holy See (~528 people)  

## Questions Addressed  
### **1. Which model best predicts temperature changes?**  
✔ **Best Model: KNN (5 neighbors)**  
- **Lowest MAE:** 0.3198 (More accurate predictions)  
- **Lowest RMSE:** 0.4197 (Fewer large errors)  
- **Highest R² Score:** 0.4965 (Explains variance in temperature changes)  

### **2. Why does feature selection matter?**  
✔ Dropping **weakly correlated (<5%) & redundant (>80%) features** improved model accuracy.  
✔ Final features retained: **Year, Savanna Fires, Forest Fires, Food Retail**.  

### **3. How do CO₂ emissions affect climate tipping points?**  
✔ Crossing **1.5°C total warming** (not per year) could trigger **irreversible climate shifts** (melting ice sheets, coral reef die-off, etc.).  
✔ Forecasting temperature changes helps **develop climate policies**.  

## Methodology  
1️⃣ **Data Cleaning** → Removed missing values, imputed NaNs, and normalized.  
2️⃣ **Feature Selection** → Identified **high-impact variables**.  
3️⃣ **Model Testing** → Compared **KNN, Linear Regression & Random Forest** using MAE, RMSE, R².  
4️⃣ **Hyperparameter Tuning** → Used **Grid Search** to optimize KNN (`n_neighbors`).  

## Conclusions  
✔ **KNN (5 neighbors) is the best model**, balancing accuracy and generalization.  
✔ **Feature selection improves predictions** by reducing noise.  
✔ **Temperature increases due to CO₂ emissions could accelerate climate tipping points.**  

## Future Questions  
- Can adding **meteorological variables** improve predictions?  
- How will **different emission policies** affect future CO₂ levels?  
- Can integrating **deep learning models** refine temperature forecasts?  

## Resources  
📌 **Data Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/alessandrolobello/agri-food-co2-emission-dataset-forecasting-ml/)  
📌 **Slide Presentation:** [Google Slides](https://docs.google.com/presentation/d/1WPx1LblLBt2n2qe52e1tUblgBP9EU6RFU4xCKbFjSrQ/edit?usp=sharing)  
