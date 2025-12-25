# Resume Screening with Machine Learning

An automated resume screening system that uses Natural Language Processing (NLP) and Machine Learning to classify resumes into different job categories. This project helps HR departments and recruiters efficiently sort and categorize large volumes of resumes.

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Results](#results)
- [Project Structure](#project-structure)
- [Contributing](#contributing)

## 🎯 Overview

This project implements an intelligent resume screening system that automatically categorizes resumes into different job domains. It uses machine learning classification algorithms combined with TF-IDF (Term Frequency-Inverse Document Frequency) text vectorization to analyze resume content and predict the most suitable job category.

The system can classify resumes into various categories including:
- Data Science
- HR (Human Resources)
- Advocate
- Arts
- Web Designing
- Mechanical Engineer
- Sales
- Health and Fitness
- Civil Engineer
- Java Developer
- Business Analyst
- SAP Developer
- Automation Testing
- Electrical Engineering
- Operations Manager
- Python Developer
- DevOps Engineer
- Network Security Engineer
- PMO
- Database
- Hadoop
- ETL Developer
- DotNet Developer
- Blockchain
- Testing

## ✨ Features

- **Automated Resume Parsing**: Extracts and cleans text from resume documents
- **Text Preprocessing**: 
  - URL removal
  - Special character cleaning
  - Stopword removal
  - Text normalization
- **Data Visualization**: 
  - Category distribution analysis
  - Word frequency visualization using WordCloud
  - Count plots and pie charts for category insights
- **Machine Learning Classification**:
  - TF-IDF vectorization for text features
  - K-Nearest Neighbors (KNN) classifier with OneVsRest strategy
  - Model evaluation with accuracy metrics and classification reports
- **Resume Prediction**: Capability to predict categories for new, unseen resumes

## 📊 Dataset

The project uses the `resume_dataset.csv` file containing:
- **Size**: ~42,000+ resume entries
- **Columns**: 
  - `Category`: Job category/domain
  - `Resume`: Full text content of the resume
- **Categories**: 25 different job categories

## 🛠️ Technologies Used

### Python Libraries
- **Data Processing**: 
  - `numpy`: Numerical computations
  - `pandas`: Data manipulation and analysis
- **Visualization**:
  - `matplotlib`: Plotting and charts
  - `seaborn`: Statistical data visualization
  - `WordCloud`: Word frequency visualization
- **Natural Language Processing**:
  - `NLTK`: Text processing and stopword removal
  - `re`: Regular expressions for text cleaning
- **Machine Learning**:
  - `scikit-learn`: ML algorithms and evaluation metrics
    - `TfidfVectorizer`: Text feature extraction
    - `KNeighborsClassifier`: Classification algorithm
    - `OneVsRestClassifier`: Multi-class classification strategy
    - `LabelEncoder`: Category encoding
    - `train_test_split`: Dataset splitting

## 📥 Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Steps

1. Clone the repository:
```bash
git clone https://github.com/mohamed-emad-c4/Project-Resume-Screening.git
cd Project-Resume-Screening
```

2. Install required packages:
```bash
pip install numpy pandas matplotlib seaborn nltk wordcloud scikit-learn
```

3. Download NLTK data (run in Python):
```python
import nltk
nltk.download('stopwords')
nltk.download('punkt')
```

## 🚀 Usage

### Running the Jupyter Notebook

1. Start Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `resumeScreening (1).ipynb` in your browser

3. Run all cells sequentially to:
   - Load and explore the dataset
   - Visualize category distributions
   - Clean and preprocess resume text
   - Train the classification model
   - Evaluate model performance
   - Predict categories for new resumes

### Quick Start Example

```python
# Load the dataset
import pandas as pd
resumeData = pd.read_csv('resume_dataset.csv', encoding='utf-8')

# View categories
print(resumeData['Category'].unique())

# Train model and predict (see notebook for full implementation)
```

## 🧠 Model Details

### Preprocessing Pipeline
1. **Text Cleaning**:
   - Remove URLs, mentions, special characters
   - Convert to lowercase
   - Remove punctuation and extra whitespace
   - Filter out stopwords

2. **Feature Engineering**:
   - TF-IDF vectorization to convert text to numerical features
   - Captures word importance across documents

3. **Model Training**:
   - Algorithm: K-Nearest Neighbors (KNN) with OneVsRestClassifier
   - Train-test split: 80-20 ratio
   - Label encoding for categorical targets

### Evaluation Metrics
- Accuracy Score
- Classification Report (Precision, Recall, F1-Score)
- Confusion Matrix analysis

## 📈 Results

The model provides:
- **Visualization Insights**: 
  - Distribution of resumes across categories
  - Most common words in resumes
  - Category-wise resume counts
- **Classification Performance**: Detailed metrics per category
- **Prediction Capability**: Can classify new resumes into appropriate categories

Example predictions can be made on new resume text by using the trained model on unseen data.

## 📁 Project Structure

```
Project-Resume-Screening/
│
├── resumeScreening (1).ipynb    # Main Jupyter notebook with full implementation
├── resume_dataset.csv           # Dataset with resume texts and categories
└── README.md                    # Project documentation
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Potential Improvements
- Add more classification algorithms (SVM, Random Forest, Neural Networks)
- Implement deep learning models (LSTM, BERT)
- Create a web interface for resume upload and classification
- Add support for PDF and DOCX resume formats
- Improve text preprocessing with lemmatization
- Add skill extraction and matching features
- Implement real-time prediction API

## 📄 License

This project is open source and available for educational purposes.

## 👤 Author

**Mohamed Emad**
- GitHub: [@mohamed-emad-c4](https://github.com/mohamed-emad-c4)

## 🙏 Acknowledgments

- Dataset contributors
- scikit-learn and NLTK communities
- Open source NLP and ML community

---

**Note**: This project is designed for educational purposes and demonstrates the application of machine learning in HR tech and recruitment automation.