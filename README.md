# Obesity Level Prediction Using Machine Learning

Introduction to Data Science semester project.

This project predicts a person's obesity level from their age, height, weight, eating habits and activity. A Random Forest model sorts each person into one of 7 levels, from Insufficient Weight to Obesity Type III. The model runs as a web app on Hugging Face, and a Power BI dashboard shows the data.

## Live demo

* [Obesity Level Predictor (graphical)](https://huggingface.co/spaces/abdullah052/Obesity_level_predictor)
* [Obesity Level Predictor (simple)](https://huggingface.co/spaces/abdullah052/obesity-level-predictor)

## Dataset

[Estimation of Obesity Levels Based on Eating Habits and Physical Condition](https://archive.ics.uci.edu/dataset/544) (Palechor and Manotas, 2019), also on Kaggle.

* 2,111 records, 16 input features
* People from Mexico, Peru and Colombia
* Features include age, gender, height, weight, family history, high calorie food, vegetables, meals per day, water, exercise, screen time, alcohol and transport

## Results

Random Forest with 100 trees, 80/20 train/test split.

**Accuracy: 95.04%** on 423 test records

| Obesity level | Precision | Recall | F1 |
| --- | --- | --- | --- |
| Insufficient Weight | 1.00 | 0.96 | 0.98 |
| Normal Weight | 0.87 | 0.94 | 0.90 |
| Overweight Level I | 0.87 | 0.86 | 0.86 |
| Overweight Level II | 0.96 | 0.96 | 0.96 |
| Obesity Type I | 0.99 | 0.95 | 0.97 |
| Obesity Type II | 0.97 | 0.98 | 0.97 |
| Obesity Type III | 1.00 | 1.00 | 1.00 |

## Project structure

```
notebook/   Training notebook (Google Colab)
data/       Dataset (CSV)
model/      Trained model, scaler and encoders (.pkl)
app/        Gradio app for Hugging Face Spaces
dashboard/  Power BI dashboard (.pbix)
docs/       Project documentation
```

## How to run

1. Install the packages:
   ```
   pip install -r requirements.txt
   ```
2. To train the model, open `notebook/obesity_prediction.ipynb`, put the CSV next to it and run all cells. It saves the `.pkl` files.
3. To see the dashboard, open `dashboard/obesity_dashboard.pbix` in Power BI Desktop.

## Tools

Python, Pandas, scikit-learn, Matplotlib, Joblib, Gradio, Hugging Face Spaces, Power BI.

