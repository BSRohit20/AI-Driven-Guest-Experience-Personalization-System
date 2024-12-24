# Feedback Sentiment Analysis with Hugging Sentiment Analysis Pipeline

This project analyzes customer feedback to classify sentiment and identify relevant service areas using the Hugging Face `transformers` library. The results include a categorized dataset and statistical insights into sentiment and service areas.

---

## Features

- **Sentiment Classification**: Determines whether feedback is `Positive`, `Negative`, or `Neutral` using the `distilbert-base-uncased-finetuned-sst-2-english` model.
- **Service Area Identification**: Classifies feedback into `Dining`, `Reception`, or `General` categories based on keywords.
- **Statistical Analysis**: Generates insights into the distribution of sentiments and service areas.
- **CSV Output**: Saves the analyzed results to a CSV file.

---

## Installation

1. Set up a virtual environment (recommended):
   - Create a virtual environment:
     ```bash
     python -m venv venv
     ```
   - Activate the virtual environment:
     - **Windows**:
       ```bash
       venv\Scripts\activate
       ```
     - **macOS/Linux**:
       ```bash
       source venv/bin/activate
       ```

2. Install required Python packages:
   ```bash
   pip install pandas transformers huggingface_hub
   ```

3. Deactivate the virtual environment when done:
   ```bash
   deactivate
   ```

---

## Usage

1. **Log in to Hugging Face Hub**:
   Replace the token in the script with your own Hugging Face API key:
   ```python
   from huggingface_hub import login
   login("your_hugging_face_api_key")
   ```

2. **Prepare the Input Dataset**:
   - Place your input dataset in the root directory of the project.
   - The dataset should be a CSV file named `input_dataset.csv` with a column named `Reviews`.

3. **Run the Analysis**:
   Execute the script:
   ```bash
   python feedback_analysis.py
   ```

4. **Output**:
   - The analyzed results are saved as `feedback_analysis_results.csv`.
   - Sentiment and service area statistics are displayed in the terminal.

---

## Project Workflow

1. **Load Dataset**:
   - Reads feedback data from the `input_dataset.csv` file.

2. **Sentiment Classification**:
   - Uses Hugging Face's sentiment analysis pipeline to label feedback as `Positive` or `Negative`.

3. **Area Classification**:
   - Categorizes feedback into service areas based on predefined keywords.

4. **Generate Results**:
   - Combines sentiment and area classifications into a results DataFrame.
   - Saves results locally to a CSV file.

5. **Generate Statistics**:
   - Displays the sentiment and area distribution as part of the terminal output.

---

## Example

### Input:
A sample `input_dataset.csv`:
```csv
Reviews
"The food was amazing and the waiter was very polite."
"The check-in process took too long and was frustrating."
"Room service was quick and efficient."
```

### Output:
`feedback_analysis_results.csv`:
```csv
Feedback,Sentiment,Area
"The food was amazing and the waiter was very polite.",Positive,Dining
"The check-in process took too long and was frustrating.",Negative,Reception
"Room service was quick and efficient.",Positive,General
```

Terminal Output:
```
Sentiment Statistics:
Positive    2
Negative    1

Area Statistics:
Dining       1
Reception    1
General      1
```

---

## Dependencies

- Python 3.7 or higher
- `pandas`
- `transformers`
- `huggingface_hub`

---
