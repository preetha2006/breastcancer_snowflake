🔬 Breast Cancer Classification with Snowflake & Naive Bayes

A complete machine learning pipeline for breast cancer classification that integrates Snowflake Data Warehouse for data storage and retrieval with Naive Bayes classification algorithm, featuring an interactive Gradio web interface for real-time predictions.

Overview:
This project demonstrates an end-to-end machine learning workflow for classifying breast tumors as malignant or benign using cell nucleus features extracted from digitized images of fine needle aspirate (FNA) of breast masses. The project showcases:
- Cloud-based data storage and retrieval using **Snowflake**
- Machine learning classification using **Gaussian Naive Bayes**
- Interactive web application using **Gradio**
- Complete data science pipeline from data loading to deployment

Features
- Cloud Integration: Seamless data retrieval from Snowflake Data Warehouse
- ML Classification: Gaussian Naive Bayes algorithm for binary classification
- EDA & Visualization: Comprehensive exploratory data analysis
- Interactive UI: Beautiful Gradio interface for real-time predictions
- High Accuracy: Achieves 96.49% accuracy on test data
- Secure: Best practices for handling sensitive medical data

Dataset
- Samples: 569 instances
- Features: 30 numerical features describing cell nucleus characteristics
  - 10 mean values (radius, texture, perimeter, area, smoothness, compactness, concavity, concave points, symmetry, fractal dimension)
  - 10 standard error values
  - 10 worst/largest values
- Target Variable: Binary classification
  - 0 = Benign (non-cancerous)
  - 1 = Malignant (cancerous)
- Class Distribution: 
  - Benign: 357 (62.7%)
  - Malignant: 212 (37.3%)

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **Python 3.8+** | Programming language |
| **Snowflake** | Cloud data warehouse |
| **pandas** | Data manipulation and analysis |
| **scikit-learn** | Machine learning algorithms |
| **Gradio** | Interactive web interface |
| **NumPy** | Numerical computing |
| **Matplotlib/Seaborn** | Data visualization |

Step 1: Clone the Repository
git clone https://github.com/yourusername/breast-cancer-classification.git
cd breast-cancer-classification

Step 2: Install Dependencies
pip install -r requirements.txt

Step 3: Configure Snowflake
If you want to fetch data from Snowflake, update the credentials in the notebook:
conn = snowflake.connector.connect(
    user='YOUR_USERNAME',
    password='YOUR_PASSWORD',
    account='YOUR_ACCOUNT',
    database='BREAST_CANCER_DATASET',
    schema='PUBLIC',
    warehouse='COMPUTE_WH'
)

Launching the Gradio Interface:
python gradio_app.py

Training Results
- Algorithm: Gaussian Naive Bayes
- Train-Test Split: 80-20
- Feature Scaling: StandardScaler

Gradio Interface:
The Gradio web application provides an intuitive interface for making predictions:

Features:
- 11 Essential Inputs: Only the most important diagnostic features
- Real-time Prediction: Instant classification results
- Confidence Scores: Probability percentages for both classes
- Minimal UI: Clean, modern, and user-friendly design
- Color-coded Results: Green for benign, red for malignant

Required Inputs:
1. Radius Mean
2. Texture Mean
3. Perimeter Mean
4. Area Mean
5. Compactness Mean
6. Concavity Mean
7. Concave Points Mean
8. Radius Worst
9. Texture Worst
10. Perimeter Worst
11. Area Worst

