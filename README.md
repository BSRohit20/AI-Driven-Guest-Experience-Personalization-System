
# Sentiment Analysis Using Transformers for AI-Driven-Guest-Experience-Personalization-System

## Overview

This repository contains Python code for performing sentiment analysis on a customer feedback dataset using Hugging Face's pre-trained `distilbert-base-uncased-finetuned-sst-2-english` model. The analysis enriches the dataset by adding sentiment labels and confidence scores for each review.

## Requirements

### Prerequisites
Ensure you have the following installed on your system:
- Python 3.9+
- Pip (Python package manager)

### Python Libraries
All dependencies are listed in the script. To ensure a clean setup, it is recommended to use a virtual environment.

---

## Setting Up a Virtual Environment

Using a virtual environment helps keep your Python dependencies isolated and avoids conflicts with other projects.

### Step 1: Create a Virtual Environment
Run the following command in your terminal to create a virtual environment:
```bash
python -m venv venv
```
Here, `venv` is the name of the virtual environment folder.

### Step 2: Activate the Virtual Environment
- **Windows**:
  ```bash
  venv\Scripts\activate
  ```
- **Mac/Linux**:
  ```bash
  source venv/bin/activate
  ```

Once activated, your terminal prompt will change to indicate the active environment (e.g., `(venv)`).

### Step 3: Install Required Libraries
With the virtual environment activated, install the required libraries using:
```bash
pip install pandas transformers
```

---

## Input File

The input file, `diverse_customer_feedback.csv`, is expected to have the following structure:
- **Columns**: At minimum, a column named `Reviews` that contains textual feedback.
- **Format**: The file should be in CSV format.

### Example Input File
| Reviews                        |
|--------------------------------|
| "The service was excellent!"   |
| "Product quality was terrible."|

## Output File

The output file, `sentiment_analysis_results.csv`, will include the original `Reviews` column along with the sentiment analysis results:
- **Sentiment**: The predicted sentiment label (`POSITIVE` or `NEGATIVE`).
- **Confidence**: The confidence score of the prediction.

### Example Output File
| Reviews                        | Sentiment | Confidence |
|--------------------------------|-----------|------------|
| "The service was excellent!"   | POSITIVE  | 0.9998     |
| "Product quality was terrible."| NEGATIVE  | 0.9973     |

## Code Explanation

1. **Import Libraries**:  
   The code uses `pandas` for data manipulation and `transformers` for sentiment analysis.

   ```python
   import pandas as pd
   from transformers import pipeline
   ```

2. **Load Dataset**:  
   The dataset is loaded from a CSV file specified by the `data_path` variable.

   ```python
   data_path = 'diverse_customer_feedback.csv'
   data = pd.read_csv(data_path)
   ```

3. **Initialize Sentiment Analysis Pipeline**:  
   The pipeline uses the `distilbert-base-uncased-finetuned-sst-2-english` model for sentiment analysis.

   ```python
   sentiment_pipeline = pipeline("sentiment-analysis", model="distilbert-base-uncased-finetuned-sst-2-english")
   ```

4. **Define Sentiment Analysis Function**:  
   The `analyze_sentiment` function applies the sentiment pipeline to a given review, returning the label and confidence score.

   ```python
   def analyze_sentiment(review):
       result = sentiment_pipeline(review)[0]
       return result['label'], result['score']
   ```

5. **Apply Sentiment Analysis**:  
   Sentiment analysis is applied to each review in the `Reviews` column. Results are stored in new columns: `Sentiment` and `Confidence`.

   ```python
   data[['Sentiment', 'Confidence']] = data['Reviews'].apply(lambda x: pd.Series(analyze_sentiment(x)))
   ```

6. **Save Results**:  
   The updated dataset, including sentiment analysis results, is saved to `sentiment_analysis_results.csv`.

   ```python
   output_path = 'sentiment_analysis_results.csv'
   data.to_csv(output_path, index=False)
   ```

7. **Completion Message**:  
   A message is printed to confirm successful execution.

   ```python
   print(f"Sentiment analysis complete. Results saved to {output_path}.")
   ```

---



## Deactivating the Virtual Environment

Once you’re done, deactivate the virtual environment using:
```bash
deactivate
```

---

