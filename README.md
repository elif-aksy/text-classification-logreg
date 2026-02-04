# Text Classification with Logistic Regression (TF-IDF)

## Project Overview
This project presents an end-to-end text classification pipeline using classical machine learning techniques.  
The focus is on transforming raw, unstructured text into meaningful numerical features and building a strong, interpretable baseline model.

The notebook demonstrates a clean and reproducible workflow suitable for data-driven decision support systems in large-scale platforms.

---

## Problem Definition
Text data plays a crucial role in e-commerce platforms through customer reviews, product descriptions, and feedback systems.  
The main challenge is to convert unstructured text into structured representations and accurately classify it using scalable and interpretable models.

---

## Approach
The project follows these steps:

- Text preprocessing and cleaning  
- Feature extraction using **TF-IDF**
- Model training with **Logistic Regression**
- Hyperparameter tuning using **GridSearchCV**
- Model evaluation with robust classification metrics  

---

## Technologies Used
- Python  
- scikit-learn  
- pandas, numpy  
- matplotlib / seaborn  

---

## Dataset
This project uses the **IMDB Movie Reviews Dataset**, a publicly available dataset containing labeled movie reviews.

The dataset is **not included in the repository** to keep it lightweight and reusable.

### Download Instructions
1. Download the dataset from Kaggle:  
   https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

2. Create a folder named `data` in the repository root.

3. Place the CSV file inside the folder with the following structure:


---

## Evaluation & Results
Model performance is evaluated using:
- **Macro F1-score**
- **Precision & Recall**
- **Confusion Matrix**

These metrics provide insight into class-wise performance and robustness, especially in imbalanced scenarios.

---

## Business Relevance
Accurate text classification can support:
- Customer feedback analysis  
- Product and content categorization  
- Insight generation for analytics and BI platforms  

Such pipelines form the foundation of scalable data platforms used in large e-commerce ecosystems.

---

## How to Run
1. Download the IMDB dataset and place it under the `data/` directory  
2. Open the notebook file  
3. Run all cells sequentially  

No additional configuration is required.

---

## Future Improvements
- Experiment with alternative vectorization techniques  
- Compare different classification models  
- Extend the pipeline to multilingual or larger-scale datasets  
