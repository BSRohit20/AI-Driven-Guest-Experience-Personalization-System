

# 🏨 Hotel Management System  

## Feedback Sentiment Analyzer  

### 🌟 Overview  
The **Hotel Feedback Sentiment Analyzer** is an AI-powered tool designed to help hotel management analyze guest feedback efficiently. It categorizes feedback into **Positive**, **Negative**, or **Neutral** sentiments, and for negative feedback, identifies specific areas of concern. This empowers hotels to address customer issues proactively and enhance service quality.  

---

## 💡 Key Features  

### Core Functionality  
- **Sentiment Classification**: Automatically categorizes guest feedback as Positive, Negative, or Neutral.  
- **Responsibility Identification**: For negative feedback, pinpoints areas for improvement, such as:  
  - Room Quality  
  - Cleanliness  
  - Staff Service  
  - Food & Beverage  
  - Amenities  
  - Check-in/Check-out Process  
  - Location, etc.  
- **Real-Time Analysis**: Analyze individual feedback instantly through an interactive interface.  
- **Batch Processing**: Analyze large datasets of feedback in CSV format.  

### User-Friendly Interface  
- Interactive feedback analysis via **Gradio**.  
- Real-time analysis with results displayed in JSON format.  
- Batch feedback processing with automated output updates.  

---

## 🚀 How It Works  

1. **Input Feedback**:  
   - Enter feedback directly in the interface or upload a dataset for batch processing.  
2. **AI Analysis**:  
   - The AI determines sentiment and identifies areas needing improvement (if applicable).  
3. **Output Results**:  
   - View real-time results in JSON format.  
   - Save batch processing results to a CSV file.  

---

## 🛠️ Setup and Installation  

### Prerequisites  
- Python 3.9 or higher.  
- API key from OpenAI or OpenRouter.  

### Installation Steps  
1. Clone the repository:  
   ```bash
   git clone https://github.com/BSRohit20/AI-Driven-Guest-Experience-Personalization-System.git
   ```  
2. Navigate to the project directory:  
   ```bash
   cd Feedback-Sentiment-Analysis  
   ```  
3. Install dependencies:  
   ```bash
   pip install gradio openai pydantic pandas  
   ```  
4. Replace `Your_API_Key` in the script with your OpenAI/OpenRouter API key.  

---

## 📖 Usage  

### Interactive Feedback Analysis  
1. Run the Gradio app:  
   ```bash
   python app.py  
   ```  
2. Open the Gradio URL in your browser.  
3. Enter feedback or use sample feedback to test the tool.  
4. View sentiment analysis and responsible areas in JSON format.  

### Batch Feedback Analysis  
1. Prepare a CSV file with guest feedback (e.g., column named `Reviews`).  
2. Run the batch analysis script:  
   ```bash
   python analyze_feedback.py  
   ```  
3. Input:  
   - Path to your dataset (e.g., `/path/to/feedback.csv`).  
   - Column name containing feedback.  
4. Output: Updated CSV file (`feedback_analysis_output.csv`) with analysis results.  

---

## 🖥️ Example  

### Interactive Analysis Example  
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
- **Python 3.9+**  
- **Gradio**: Interactive UI framework.  
- **OpenAI**: API for AI sentiment analysis.  
- **Pydantic**: Data validation and management.  
- **Pandas**: Data manipulation and analysis.  

---

## 🌍 Acknowledgements  
- **Gradio**: For an interactive UI experience.  
- **OpenAI**: For advanced sentiment analysis models.  
- **Pandas**: For simplifying data processing.  
- Guests: For their valuable feedback to improve services.  

---  

# 🚀 Customer Recommendation System  

### 🌟 Overview  
An AI-powered system that classifies users, analyzes preferences, and generates personalized recommendations for enhanced customer satisfaction.  

---

## 💡 Features  

- **User Classification**: Categorizes customers into:  
  - **Loyal**  
  - **Dissatisfied**  
  - **Young**  
  - **General**  
- **Personalized Recommendations**: Combines **TF-IDF** (text analysis) and **Cosine Similarity** (numerical data analysis) to suggest tailored products/services.  
- **Database Management**: Stores customer profiles and recommendation history securely using **SQLite**.  
- **Dynamic Interaction**:  
  - Add new customers.  
  - Retrieve existing recommendations.  
  - Update customer preferences seamlessly.  

---

## 🛠️ Setup and Installation  

1. Clone the repository:  
   ```bash
   git https://github.com/BSRohit20/AI-Driven-Guest-Experience-Personalization-System.git  
   cd Recommendation_using_hybrid_filtering_
   ```  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt  
   ```  
3. Ensure `diverse_synthetic_customer_data.csv` is in the project directory.  

---

## 🎮 How to Use  

1. Run the application:  
   ```bash
   python main.py  
   ```  
2. Interact with the UI:  
   - Add new customers.  
   - Retrieve recommendations for existing customers using their **Customer ID**.  
   - Update customer preferences dynamically.  

---

## 🗂️ Project Structure  

| File/Folder                 | Description                         |  
|-----------------------------|-------------------------------------|  
| `main.py`                   | Core recommendation system logic.   |  
| `diverse_synthetic_customer_data.csv` | Dataset for customer profiles.        |  
| `requirements.txt`          | Required dependencies.              |  

---

## ⚙️ Technologies Used  

- **Python Libraries**:  
  - `pandas`  
  - `numpy`  
  - `scikit-learn`  
  - `sqlalchemy`  
  - `ipywidgets`  
- **Machine Learning Techniques**:  
  - **TF-IDF** for analyzing textual data.  
  - **Cosine Similarity** for preference matching.  
- **Database**: SQLite for secure storage.  
- **UI**: Built with `ipywidgets`.  

---

🎉 Start today and enhance customer satisfaction with tailored recommendations!  

---  
