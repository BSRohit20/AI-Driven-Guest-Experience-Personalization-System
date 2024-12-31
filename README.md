# Feedback Analysis Project

This project performs sentiment analysis and area classification on customer feedback using machine learning models hosted on Hugging Face. It processes customer reviews to determine their sentiment (Positive/Negative) and categorize them into specific areas of interest.

## Features

- **Sentiment Analysis**: Classifies feedback as either `Positive` or `Negative`.
- **Area Classification**: Categorizes feedback into predefined areas like `Dining`, `Reception`, `Facilities`, `Cleanliness`, and `General`.
- **LLM-Powered Analysis**: Leverages large language models (LLMs) from Hugging Face for advanced text classification and sentiment detection.
- **Statistical Insights**: Generates summary statistics for sentiment and area classifications.
- **Output Formats**: Saves results in both CSV and JSON formats for further analysis.

## Requirements

- Python 3.9 or later
- Required libraries: `pandas`, `requests`

## Setup and Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/BSRohit20/AI-Driven-Guest-Experience-Personalization-System.git
   cd AI-Driven-Guest-Experience-Personalization-System
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up the Hugging Face API token:
   - Obtain your API token from [Hugging Face](https://huggingface.co/).
   - Replace the `API_TOKEN` variable in the script with your token.

## Usage

1. Place your feedback dataset in the project directory (e.g., `updated_customer_feedback.csv`).

2. Run the analysis script:
   ```bash
   python feedback_analysis.py
   ```

3. Outputs will be saved in the `results` directory:
   - CSV: `feedback_analysis_results.csv`
   - JSON: `feedback_analysis_results.json`

## Simulated Output Example

If the API is inaccessible, the script can simulate results for demonstration purposes. Simulated outputs are also saved in the same format.

## Statistical Insights

The script generates statistical summaries for the analyzed dataset, including:

- **Sentiment Statistics**: A breakdown of the number of `Positive` and `Negative` feedback entries.
- **Area Statistics**: Counts of feedback categorized into areas like `Dining`, `Reception`, etc.

Example Output:

### Sentiment Statistics:
- Positive: 70%
- Negative: 30%

### Area Statistics:
- Dining: 25%
- Reception: 20%
- Facilities: 30%
- Cleanliness: 15%
- General: 10%

These statistics provide a quick overview of customer sentiment and focus areas, enabling better decision-making.

## Files

- `feedback_analysis.py`: Main script for analyzing feedback.
- `updated_customer_feedback.csv`: Example input dataset.
- `results/`: Directory for saving output files.

## Example Dataset

| Reviews                                 | Sentiment | Area         |
|-----------------------------------------|-----------|--------------|
| "The dining experience was exceptional" | Positive  | Dining       |
| "Reception was slow to respond"         | Negative  | Reception    |
| "Facilities were clean and well-kept"   | Positive  | Facilities   |



## Contributions

Contributions are welcome! Please create a pull request or open an issue for any suggestions or improvements.

