
# 🏨 Hotel Feedback Sentiment Analyzer

## 🌟 Overview
The **Hotel Feedback Sentiment Analyzer** is an advanced AI-powered tool for hotel management teams to analyze guest feedback efficiently. It provides sentiment analysis to classify feedback as **Positive**, **Negative**, or **Neutral**, and for negative feedback, identifies specific areas of concern. This tool enables hotels to address customer issues proactively and improve service quality.

---

## 💡 Features
### Core Functionality:
- **Sentiment Classification**: Determines whether feedback is Positive, Negative, or Neutral.
- **Responsibility Identification**: Pinpoints specific areas for improvement if feedback is negative:
  - Room Quality
  - Cleanliness
  - Staff Service
  - Food & Beverage
  - Amenities
  - Check-in/Check-out Process
  - Location, and more.
- **Interactive Feedback Analysis**: Analyze feedback in real-time using a user-friendly interface.
- **Batch Processing**: Analyze large datasets of feedback in CSV format.

### User-Friendly Gradio Interface:
- Enter guest feedback directly.
- Get real-time analysis in JSON format.
- View examples for quick testing.

### Batch Processing:
- Process multiple feedback entries at once from a CSV file.
- Automatically updates the file with sentiment analysis results.

---

## 🚀 How It Works
1. **Feedback Input**: 
   - Provide feedback through the Gradio interface or upload a dataset for batch processing.
2. **AI Model Processing**: 
   - The AI analyzes feedback, determines sentiment, and identifies responsible areas for negative feedback.
3. **Output Results**:
   - For the Gradio interface, results are displayed in JSON format.
   - For batch processing, results are saved to an updated CSV file.

---

## 🔧 Installation

### Prerequisites:
- Python 3.9 or higher.
- An API key from OpenAI or OpenRouter.

### Steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/BSRohit20/AI-Driven-Guest-Experience-Personalization-System.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Feedback-Sentiment-Analysis
   ```
3. Install required dependencies:
   ```bash
   pip install gradio openai pydantic pandas
   ```

---

## 🛠️ Setup
1. Obtain an API key from [OpenAI](https://openai.com/) or [OpenRouter](https://openrouter.ai/).
2. Open the script file and replace `Your_API_Key` with your API key.

---

## 📖 Usage

### **Interactive Feedback Analysis**
1. Run the Gradio app:
   ```bash
   python app.py
   ```
2. Open the Gradio URL provided in the terminal.
3. Enter guest feedback in the input box or try the example feedback.
4. View the JSON-formatted analysis result.

### **Batch Feedback Analysis**
1. Prepare a CSV file containing guest feedback. The feedback column can have any name (e.g., `Reviews`).
2. Run the batch analysis script:
   ```bash
   python analyze_feedback.py
   ```
3. Provide:
   - The file path to your dataset (e.g., `/path/to/feedback.csv`).
   - The column name containing feedback.
4. Results will be saved to a new file: `feedback_analysis_output.csv`.

---

## 🖥️ Example

### **Interactive Analysis Example**
#### Input:
**Feedback**: "The room was dirty, and the staff were rude."
#### Output:
```json
{
  "sentiment": "Negative",
  "responsible_area": "Room Quality, Staff Service"
}
```

---

## ⚙️ Dependencies
- **Python 3.9+**: Programming language.
- **Gradio**: Interactive UI framework.
- **OpenAI**: API for AI-powered sentiment analysis.
- **Pydantic**: Data validation and settings management.
- **Pandas**: Data processing and analysis.


---


## 🌍 Acknowledgements
- **Gradio**: For enabling a seamless user interface.
- **OpenAI**: For the sentiment analysis model.
- **Pandas**: For efficient data manipulation.
- Hotel guests for their invaluable feedback, driving service improvements.


```
