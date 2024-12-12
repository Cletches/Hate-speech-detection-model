 Hate Speech Detection Model

This project is a machine learning-based solution to classify tweets into three categories:  
1. Hate Speech  
2. Offensive Language 
3. No Hate and Offensive 

The script preprocesses text data, trains a decision tree classifier, and provides predictions based on user input.

---

Table of Contents
1. [Features](#features)  
2. [Setup Instructions](#setup-instructions)  
3. [Usage](#usage)  
4. [How It Works](#how-it-works)  
5. [Dependencies](#dependencies)  
6. [Future Enhancements](#future-enhancements)

---

Features

- Data Preprocessing:  
  - Removes URLs, HTML tags, punctuation, and stopwords.  
  - Converts text to lowercase.  
  - Stems words to their root form.  

- Machine Learning Model:  
  - Uses a `DecisionTreeClassifier` to classify tweets.  

- Real-time User Input:  
  - Classifies text input by the user into predefined categories.  

---

Setup Instructions

1. Clone the Repository 
   ```bash
   git clone https://github.com/your-repository.git
   cd your-repository
   ```

2. Install Dependencies  
   Ensure you have Python 3.7+ installed. Then, install the required libraries:  
   ```bash
   pip install pandas numpy scikit-learn nltk
   ```

3. Download Stopwords
   The script uses NLTK stopwords. Download them before running:  
   ```python
   import nltk
   nltk.download('stopwords')
   ```

4. Add the Dataset
   Place the dataset (`twitter.csv`) in the same directory as the script. Ensure it matches the expected format.

---
 Usage

1. Run the script:  
   ```bash
   python hate_speech_detection.py
   ```

2. Enter a text input when prompted. Example:  
   ```text
   Enter a Text: Let's unite and kill all the people who don't value our religion.
   ```
   The model will output a prediction:  
   ```text
   ['Hate Speech']
   ```

---
 How It Works

1. **Dataset Preprocessing**:  
   - Reads the `twitter.csv` file, retaining only relevant columns (`tweet` and `labels`).  
   - Applies the `clean()` function to preprocess text.

2. Feature Extraction**:  
   - Converts the cleaned text into a numerical representation using `CountVectorizer`.

3. Model Training**:  
   - Splits the data into training and testing sets.  
   - Trains a `DecisionTreeClassifier` on the training set.

4. Prediction**:  
   - Accepts user input, preprocesses it, and classifies it using the trained model.

---

Dependencies

- Python: 3.7+  
- Libraries**:  
  - pandas  
  - numpy  
  - scikit-learn  
  - nltk  

---

 Future Enhancements

- Implement more sophisticated models like Random Forest or Neural Networks for better accuracy.  
- Include cross-validation for performance evaluation.  
- Expand preprocessing to handle emojis and other text features.  
- Add a web or desktop interface for easier usage.

---

Feel free to contribute by submitting pull requests or reporting issues! 🎉
