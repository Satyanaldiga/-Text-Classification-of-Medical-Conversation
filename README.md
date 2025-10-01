🩺 Text Classification of Medical Conversations

Date: February 13, 2025

📌 Background

Medical conversations – also known as healthcare communication between physicians and their patients – are at the core of healthcare delivery and have a crucial impact on patient outcomes. Understanding the content and dynamics of these conversations helps improve both care quality and patient experience.

This project applies the Social Support Theory to systematically categorize medical conversations. According to this theory, physician communication can be considered a form of social support, which is divided into two main categories:

Emotional Support (e.g., greeting, offering comfort, expressing gratitude)

Informational Support (e.g., diagnosis, treatment, explanation, referral)

Each category contains multiple subcategories that capture the intent of the physician’s communication.

📊 Dataset

The dataset used in this project comes from an online healthcare platform and contains 4030 sentences and clauses written by certified medical practitioners (physicians, pharmacists, nurse practitioners).

Each entry has been manually labeled according to its content category.

Label Distribution
Label Name	Frequency
TREAT	1188
EXPLAIN	1061
DIAGNOISE	381
QUES (Question)	267
REFERRAL	222
THANK	145
WAIT	139
GREET	120
RECEIVE	110
REPEAT	86
CONSOLE	78
REMIND	78
WISH	64
REQUEST INFORMATION	55
FUTURE SUPPORT	36

The dataset was split into training and validation sets. A separate test set was reserved for final evaluation.

⚙️ Project Approach

This project focused on building a content classification model to automatically assign each medical sentence to one of the Social Support Theory categories.

🔍 Steps Taken

Dataset Exploration & Preprocessing

Reviewed and analyzed the dataset

Tokenized sentences and cleaned text

Handled class imbalance (oversampling/undersampling techniques)

Converted text into numerical representations (e.g., TF-IDF, word embeddings)

Model Design & Development

Experimented with both traditional machine learning models (Logistic Regression, Gradient Boosting) and deep learning models (CNN, LSTM, Transformer-based architectures)

Evaluated classification performance across models

Optimized model parameters using validation data

Evaluation Metrics

Accuracy

Precision

Recall

F1-score

🚀 Results

Traditional models provided strong baselines but struggled with minority classes (e.g., FUTURE SUPPORT, WISH).

Deep learning models (CNN & LSTM) showed significant improvements in recall and F1-score, particularly in underrepresented categories.

Transformer-based approaches (e.g., BERT) demonstrated the best overall balance between accuracy and class coverage, highlighting their effectiveness in understanding nuanced medical text.

🧩 Key Insights

Imbalanced labels required careful handling to avoid bias toward frequent categories (TREAT, EXPLAIN).

Emotional support categories (e.g., CONSOLE, WISH) were harder to classify due to fewer training examples.

Combining linguistic features with contextual embeddings produced the most reliable results.

📦 Technologies Used

Python 3.x

pandas, numpy, scikit-learn

TensorFlow / Keras (CNN & LSTM models)

Transformers (Hugging Face) for contextual embeddings

NLTK / spaCy for tokenization and text preprocessing

matplotlib / seaborn for visualizations

✅ Conclusion

This project successfully built a text classification system for medical conversations grounded in Social Support Theory. The system can identify whether physician communication is emotional or informational support, and further classify it into specific subcategories.

The findings demonstrate that advanced neural architectures (CNN, LSTM, Transformers) are particularly effective in capturing the nuanced language of medical conversations, and they hold promise for improving automated healthcare communication analysis.****
