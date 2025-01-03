# Sentiment Analysis Tool

This project analyzes hotel guest feedback to determine the sentiment (Positive, Negative, or Neutral) and, in the case of negative feedback, identifies the specific area responsible for the dissatisfaction. It supports both batch processing of datasets and manual entry for individual feedback analysis.

## Features

- **Sentiment Analysis**: Categorizes feedback into Positive, Negative, or Neutral.
- **Responsible Area Detection**: Pinpoints the area of concern for negative feedback, such as 'Room Quality,' 'Cleanliness,' or 'Staff Service.'
- **Batch Processing**: Processes an entire dataset of feedback and outputs results to a new file.
- **Manual Feedback Entry**: Allows real-time analysis of single feedback entries.

## Requirements

- Python 3.9+
- Required libraries: `openai`, `pandas`, `pydantic`

## About the LLM

This tool leverages a large language model (LLM) provided by OpenAI. The LLM is fine-tuned to understand and analyze textual data, enabling it to identify sentiment and specific areas of concern in feedback. By using natural language processing capabilities, it ensures accurate and context-aware sentiment analysis. The LLM is accessed via OpenAI’s API and can handle both structured datasets and individual inputs effectively.

## Installation

1. Clone this repository.
2. Install dependencies:
   ```bash
   pip install openai pandas pydantic
   ```

## Usage

1. **Setup OpenAI API**:
   Replace `YOUR_API_KEY` with your OpenAI API key in the code.

2. **Prepare Dataset**:
   Ensure your feedback dataset is in CSV format with a column containing guest feedback.

3. **Run the Script**:
   ```bash
   python Feedback_Sentiment_Analysis.py
   ```
   - Enter the file path to your dataset when prompted (e.g., `feedback.csv`).
   - Provide the column name containing the feedback (e.g., `Review`).

4. **Manual Feedback Analysis**:
   Modify the script to call `provide_sentiment()` with a single feedback string for instant results.

5. **Results**:
   - For batch processing, the script will create a new file named `feedback_analysis_output.csv` with the sentiment analysis results and responsible areas.
   - For manual entries, the sentiment and responsible area will be displayed directly in the console.

## Example

### Input
#### Dataset Example (`feedback.csv`):
| Review                         |
|--------------------------------|
| "The room was clean and tidy."|
| "Terrible service at the reception." |
| "The food was okay, but the wait time was long." |

#### Manual Feedback Example:
```bash
python sentiment_analysis.py
Enter feedback: "The staff was very friendly but the room was noisy."
```

### Output
#### Dataset Output (`feedback_analysis_output.csv`):
| Review                         | Sentiment | Responsible Area       |
|--------------------------------|-----------|------------------------|
| "The room was clean and tidy."| Positive  | N/A                    |
| "Terrible service at the reception." | Negative  | Staff Service          |
| "The food was okay, but the wait time was long." | Neutral   | N/A                    |

#### Manual Feedback Output:
```
Sentiment: Mixed
Responsible Area: Staff Service, Noise
```

## Error Handling
- If the API call fails or the response is invalid, the tool assigns `Error` to the `Sentiment` column and `N/A` to the `Responsible Area` column.

