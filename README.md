# Feedback Sentiment Analysis

This project classifies customer feedback based on sentiment (Positive, Negative, Neutral) and categorizes it into different areas such as Dining, Reception, Facilities, and Cleanliness. The analysis uses the Hugging Face `transformers` library for sentiment analysis and keyword-based rules for area classification.

## Features

- **Sentiment Analysis**: Classifies feedback as Positive, Negative, or Neutral.
- **Area Classification**: Categorizes feedback into predefined areas based on keywords.
- **Statistical Summary**: Provides counts for each sentiment and area.
- **CSV Output**: Saves the analysis results in a CSV file for further use.

## Requirements

- Python 3.9+
- Libraries:
  - `transformers`
  - `pandas`
  - `huggingface_hub`

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/BSRohit20/AI-Driven-Guest-Experience-Personalization-System.git
   cd AI-Driven-Guest-Experience-Personalization-System
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required libraries:
   ```bash
   pip install transformers pandas huggingface_hub
   ```

## Usage

1. **Prepare the Dataset**:
   Ensure your dataset is in CSV format with a column named `Reviews` containing customer feedback. Example:
   ```csv
   Reviews
   "The food was amazing, and the service was excellent."
   "The room was clean but noisy."
   ```

2. **Run the Script**:
   Update the `file_path` variable in the script with the path to your dataset, then execute:
   ```bash
   python analyze_feedback.py
   ```

3. **View Results**:
   The results will be saved in `feedback_analysis_results.csv` in the same directory. You can also view the statistical summary in the terminal.

## Code Structure

- **Dataset Loading**: Loads the CSV file into a pandas DataFrame.
- **Sentiment Classification**: Uses the Hugging Face pipeline for sentiment analysis.
- **Area Classification**: Categorizes feedback using keyword-based rules.
- **Statistical View**: Displays counts of each sentiment and area.
- **CSV Output**: Saves the analyzed data to a file.

## Example Output

### Input

```csv
Reviews
"The gym and pool were well-maintained and exceeded expectations."
"Reception staff was rude, and the check-in process took forever."
```

### Output (CSV)

```csv
Feedback,Sentiment,Area
"The gym and pool were well-maintained and exceeded expectations.",Positive,Facilities
"Reception staff was rude, and the check-in process took forever.",Negative,Reception
```

### Statistical Summary

```
Sentiment Statistics:
Positive    1
Negative    1
Name: Sentiment, dtype: int64

Area Statistics:
Facilities    1
Reception     1
Name: Area, dtype: int64
```

## Hugging Face Integration

Log in to Hugging Face before running the script:
```python
from huggingface_hub import login
login("your_huggingface_token")
```
Replace `your_huggingface_token` with your Hugging Face token.


## Acknowledgments

- [Hugging Face](https://huggingface.co/) for providing the sentiment analysis models.
- The Python community for their excellent libraries and tools.
