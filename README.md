# 📊 PathMNIST Visualisation & Classification Project

This project explores the **PathMNIST** medical image dataset using Python, and demonstrates both **data visualisation** and **machine learning techniques** to analyse and classify multi-class tissue samples.

---

## 📁 Dataset

We used the **PathMNIST** dataset from the MedMNIST collection, which contains 107,180 RGB images (28×28 pixels) of 9 tissue classes. For this coursework, the dataset was filtered down to **40,500 samples** using stratified sampling to balance all 9 classes.

---

## ⚙️ Preprocessing

1. **Loading and Merging**
   - Combined training, validation, and test splits using `np.load`.

2. **Flattening**
   - Reshaped image data to convert 3D images into 1D feature vectors.

3. **Stratified Sampling**
   - Selected exactly **4,500 samples per class** for a balanced dataset (total = 40,500).

4. **Label Mapping**
   - Mapped numeric labels (0–8) to string class names like `'ADI'`, `'TUM'`, etc.

5. **Cleaning**
   - Checked and confirmed that:
     - No missing values were present
     - No duplicate records existed

6. **One-Hot Encoding**
   - Encoded the label column for compatibility with ML algorithms while keeping the original class names.

---

## 📊 Visualisations

The project includes multiple visualisation techniques to explore and understand the dataset:

- **Box Plot** – shows intensity distribution across classes
- **Violin Plot** – adds density curves for deeper comparison
- **Pie Chart** – visualises intensity distribution across ranges
- **Histogram** – pixel intensity frequency across the whole dataset
- **Radar Chart** – compares mean and std dev per class
- **t-SNE Scatter Plot** – 2D embedding to show class separation
- **Bubble Chart** – pixel-based class frequency using color & size
- **Heatmap** – average pixel values across classes
- **Stacked Bar Chart** – pixel intensity range by class
- **Contingency Table & Mosaic Plot** – visual relationship between label and dummy group

---

## 🤖 Machine Learning

Four ML models were trained on the data:

| Model               | Accuracy | F1 Score |
|---------------------|----------|----------|
| Logistic Regression | 33%      | 33%      |
| Random Forest       | 63%      | 63%      |
| K-Nearest Neighbors | 30%      | 22%      |
| XGBoost             | 74%      | 74%      |

- **Train/Val/Test Split:** 70% / 20% / 10%  
- **Evaluation Metrics:** Accuracy, Macro Precision, Recall, F1 Score  
- **Label encoding** was applied using `LabelEncoder`.

---

## ▶️ How to Run

1. Make sure `pathmnist.npz` is placed in the **same directory** as `main.ipynb`.

2. Install dependencies:
    ```bash
    pip install pandas matplotlib seaborn scikit-learn xgboost umap-learn medmnist
    ```

3. Open and run `main.ipynb` step-by-step.

---

## 📌 Notes

- All visualisations use only the cleaned and balanced dataset.
- t-SNE may take several minutes depending on system memory.
- This notebook satisfies coursework requirements for preprocessing, visualisation, and ML.

---
