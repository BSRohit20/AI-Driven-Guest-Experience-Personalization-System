# Feedback Analysis with Hugging Face Models

This project analyzes customer feedback data using Hugging Face's pre-trained models for sentiment analysis and area classification. The feedback is processed to determine its sentiment (Positive/Negative) and the relevant area of concern (Dining, Reception, Facilities, Cleanliness, or General).

## Features

- **Sentiment Analysis**: Classifies feedback as Positive or Negative using the `distilbert-base-uncased-finetuned-sst-2-english` model.
- **Area Classification**: Identifies the area of concern from predefined labels using the `facebook/bart-large-mnli` model.
- **Data Processing**: Analyzes a dataset of customer feedback and outputs results to CSV and JSON files.
- **Statistical Insights**: Generates a summary of sentiment and area statistics.

## Requirements

### Python Libraries

Ensure you have the following Python libraries installed:

- `pandas`
- `requests`

You can install the required libraries using:

```bash
pip install pandas requests
```

### Hugging Face API Token

Sign up for a [Hugging Face](https://huggingface.co/) account to obtain your API token. Replace `Your_API_Key` in the script with your token.

## Usage

### 1. Prepare the Dataset

Prepare a CSV file named `updated_customer_feedback.csv` with at least one column:

- `Reviews`: Contains customer feedback as text.

### 2. Run the Script

Execute the script by running:

```bash
python feedback_analysis.py
```

### 3. Output

The script produces:

- A CSV file: `feedback_analysis_results.csv`
- A JSON file: `feedback_analysis_results.json`

Both files contain the following columns:

- **Feedback**: Original customer feedback.
- **Sentiment**: Sentiment classification (Positive/Negative).
- **Area**: Identified area of concern.

#### Results

- The **CSV file** provides an easy-to-view tabular format of the analysis results.
- The **JSON file** is structured for integration with other applications or for further processing.
- Example output rows include sentiment and area classifications for each piece of feedback:

| Feedback                          | Sentiment | Area         |
|-----------------------------------|-----------|--------------|
| "The reception was very helpful." | Positive  | Reception    |
| "Dining area was not clean."      | Negative  | Cleanliness  |
| "Facilities were top-notch."      | Positive  | Facilities   |

### 4. Statistical Summary

The script outputs statistical summaries of sentiment and area classifications to the console. This includes:

- **Sentiment Statistics**: Distribution of Positive and Negative feedback.
- **Area Statistics**: Frequency of feedback assigned to each area.

## File Structure

```
feedback_analysis/
|
|-- feedback_analysis.py         # Main script
|-- updated_customer_feedback.csv # Input data (example dataset)
|-- feedback_analysis_results.csv # Output results in CSV format
|-- feedback_analysis_results.json # Output results in JSON format
```

## Troubleshooting

### Common Errors

#### Invalid API Token

Ensure your API token is correctly set in the script under the variable `API_TOKEN`.

#### API Rate Limits

The Hugging Face API may enforce rate limits. Upgrade your plan if necessary.

#### Unexpected Output Format

If the API response format changes, the script may fail. Check the raw responses logged in the console for debugging.


## Contributions

Contributions are welcome! Feel free to fork the repository and submit pull requests.


