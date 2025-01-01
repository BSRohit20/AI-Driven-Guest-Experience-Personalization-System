# Sentiment Analysis and Feedback Classification

This project leverages pre-trained models from Hugging Face to analyze customer feedback data. It performs sentiment analysis to identify whether feedback is positive or negative and classifies negative feedback into predefined categories based on areas of concern. The tool can process datasets or allow for real-time interactive feedback analysis.

## Features

1. **Sentiment Analysis**:
   - Determines whether feedback is positive or negative.
   - Uses the Hugging Face model `distilbert-base-uncased-finetuned-sst-2-english`.

2. **Area Classification**:
   - For negative feedback, identifies the specific area of concern.
   - Predefined categories include:
     - Dining
     - Reception
     - Facilities
     - Cleanliness
     - General
   - Utilizes the `facebook/bart-large-mnli` model for classification.

3. **Dataset Analysis**:
   - Processes a CSV file containing customer feedback data.
   - Outputs detailed sentiment and area classification results.
   - Generates statistical insights into customer sentiment and areas of concern.

4. **Interactive Feedback Tool**:
   - Provides a user-friendly interface for real-time feedback analysis.
   - Classifies feedback sentiment and areas of concern instantly.

## About Large Language Models (LLMs)

Large Language Models (LLMs) like the ones used in this project are advanced AI systems trained on vast amounts of textual data. They can perform a variety of natural language processing tasks, such as:

- Sentiment Analysis: Understanding the emotional tone of text.
- Text Classification: Categorizing text into predefined categories.
- Question Answering, Text Generation, and more.

In this project:
- The `distilbert-base-uncased-finetuned-sst-2-english` model is a fine-tuned version of the DistilBERT model specialized in sentiment analysis.
- The `facebook/bart-large-mnli` model is a variant of the BART transformer model fine-tuned for Natural Language Inference (NLI), enabling multi-label text classification.

These models enable efficient and accurate processing of customer feedback, allowing businesses to gain actionable insights.

## Technologies Used

- **Python**: For implementation and scripting.
- **Pandas**: For data manipulation and statistical analysis.
- **Requests**: For API interactions with Hugging Face models.
- **Hugging Face Transformers**: Pre-trained models for NLP tasks.

## Prerequisites

- Python 3.9 or higher.
- A Hugging Face account with an API token.

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/BSRohit20/AI-Driven-Guest-Experience-Personalization-System
   cd AI-Driven-Guest-Experience-Personalization-System
   ```

2. **Install Dependencies**:
   ```bash
   pip install pandas requests
   ```

3. **Set API Token**:
   Replace `API_TOKEN` in the script with your Hugging Face API token.

4. **Prepare the Dataset**:
   - Place your feedback dataset (CSV format) in the project directory.
   - Default filename: `updated_customer_feedback.csv`.

## Usage

### Dataset Analysis

1. Run the script to analyze a dataset:
   ```bash
   python Feedback_Sentiment_Analysis.py
   ```

2. The script performs the following steps:
   - Loads the dataset from the specified CSV file.
   - Analyzes feedback for sentiment and area classification.
   - Generates statistical summaries for sentiment and areas of concern.
   - Saves the results to:
     - `feedback_analysis_results.csv` (CSV format)
     - `feedback_analysis_results.json` (JSON format)

3. Sample Output:
   - Example rows from the CSV output:

| Feedback                          | Sentiment | Area       |
|-----------------------------------|-----------|------------|
| "The room was spotless."         | Positive  | N/A        |
| "The dining service was terrible." | Negative  | Dining     |

### Interactive Feedback Tool

1. Run the interactive feedback tool:
   ```bash
   python feedback_tool.py
   ```

2. Enter feedback as prompted in the terminal:
   - Input: "The reception service was too slow."
   - Output: "The feedback sentiment is Negative. Area of concern: Reception."

3. Exit the tool by typing `exit`.

## Output Examples

### Dataset Analysis Results
| Feedback                          | Sentiment | Area       |
|-----------------------------------|-----------|------------|
| "The room was spotless."         | Positive  | N/A        |
| "The dining service was terrible." | Negative  | Dining     |

### Interactive Feedback Tool Example
```
Please enter your feedback (or type 'exit' to quit): The room was perfect!
The feedback sentiment is Positive. Thank you for your feedback!

Please enter your feedback (or type 'exit' to quit): The reception was unhelpful.
The feedback sentiment is Negative. Area of concern: Reception.
```

## Known Issues

1. **Internet Dependency**:
   - A stable internet connection is required for API calls to Hugging Face models.

2. **Feedback Format**:
   - Unexpected or ambiguous feedback may result in classification errors.
