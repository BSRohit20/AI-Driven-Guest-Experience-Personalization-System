# Feedback Analysis Project

This project demonstrates how to analyze customer feedback using NLP pipelines from the Hugging Face Transformers library. The analysis involves two tasks:

1. Sentiment Analysis: Classifying feedback as Positive, Negative, or Neutral.
2. Area Classification: Identifying the area of concern (e.g., Dining, Reception, etc.) using zero-shot classification.

## Features
- **Sentiment Analysis:** Uses the `distilbert-base-uncased-finetuned-sst-2-english` model for sentiment classification.
- **Area Classification:** Employs the `facebook/bart-large-mnli` model for zero-shot classification.
- **Statistical Insights:** Provides sentiment and area-based statistics.
- **Export Results:** Saves the analysis to CSV and JSON files.

## Prerequisites

1. Python 3.9+
2. Required Python libraries:
   - `transformers`
   - `pandas`
   - `huggingface_hub`

Install the dependencies using pip:
```bash
pip install transformers pandas huggingface_hub
```

3. A Hugging Face account for authentication.

## Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/BSRohit20/AI-Driven-Guest-Experience-Personalization-System.git
   ```
2. Navigate to the project directory:
   ```bash
   cd AI-Driven-Guest-Experience-Personalization-System
   ```
3. Authenticate with Hugging Face:
```python
from huggingface_hub import login
login("<your_huggingface_token>")
```
Replace `<your_huggingface_token>` with your personal access token from [Hugging Face](https://huggingface.co/).

4. Prepare your dataset:
   - Place your CSV file containing customer feedback in the project directory.
   - The file should have a column named `Reviews` containing the feedback text.


## Usage

1. Place your customer feedback CSV file in the project directory.
2. Update the file path in the script if necessary.
3. Run the script:
   ```bash
   python feedback_analysis.py
   ```

## Output

- A CSV file (`feedback_analysis_results.csv`) containing the following columns:
  - Feedback: The original customer feedback.
  - Sentiment: Sentiment classification (Positive, Negative, Neutral).
  - Area: Area classification (Dining, Reception, Facilities, Cleanliness, General).
- A JSON file (`feedback_analysis_results.json`) with the same data.

### Dataset Output Example

Input:
```csv
Reviews
"General service was average, but I loved the helpful staff."
"The receptionist greeted us warmly and ensured our check-in was smooth."
"The dining area was messy and poorly managed."
```

Output (CSV):
```csv
Feedback,Sentiment,Area
"General service was average, but I loved the helpful staff.",Positive,General
"The receptionist greeted us warmly and ensured our check-in was smooth.",Positive,Reception
"The dining area was messy and poorly managed.",Negative,Cleanliness
```

### Statistics for Provided Dataset

#### Sentiment Statistics:
- **Neutral**: 28,853
- **Positive**: 9,591

#### Area Statistics:
- **General**: 11,403
- **Dining**: 7,725
- **Facilities**: 7,680
- **Reception**: 5,824
- **Cleanliness**: 5,812

## Statistical Summary

The script outputs:
- Counts of feedback by sentiment.
- Counts of feedback by area.


## Acknowledgments
- Hugging Face for their powerful NLP models.
- OpenAI for providing assistance in project development.



