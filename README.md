

# 🏨 Hotel Management System  


#  🌟 Hotel Feedback Sentiment Analyzer
The **Hotel Feedback Sentiment Analyzer** is a 🐍 Python-based tool that processes hotel guest feedback, performs sentiment analysis, and sends alerts for negative reviews via Slack and email. It utilizes OpenAI's language model 🤖 to classify sentiments and identify areas of concern.

## 🚀 Features
- **📊 Sentiment Analysis**: Classifies feedback as Positive, Neutral, or Negative.
- **⚠️ Concern Identification**: Detects specific areas of concern in negative feedback (e.g., Room Quality, Cleanliness, Staff Service, etc.).
- **💬 Slack Alerts**: Sends notifications to a Slack channel for negative feedback.
- **📧 Email Alerts**: Sends email notifications for negative feedback.
- **🖥️ Interactive UI**: Uses Jupyter Notebook widgets for input and analysis.

## 🛠 Technologies Used
- **🐍 Python**
- **🤖 OpenAI API** (via OpenRouter)
- **💬 Slack SDK** (Webhook Client)
- **📧 SMTP** (for email notifications)
- **📦 ipywidgets** (for interactive UI in Jupyter Notebook)

## 📥 Installation
### Prerequisites
- 🐍 Python 3.x
- 📓 Jupyter Notebook (for interactive usage)
- 🔑 OpenAI API Key (via OpenRouter)
- 🔗 Slack Webhook URL
- ✉️ Gmail account with App Password enabled

### ⚙️ Setup
1. 🛠️ Clone this repository:
   ```bash
   git clone https://github.com/your-username/hotel-feedback-analyzer.git
   cd hotel-feedback-analyzer
   ```
2. 📦 Install dependencies:
   ```bash
   pip install pydantic slack_sdk ipywidgets openai
   ```
3. 🔧 Set up environment variables or update script with:
   - `🔑 Your_API_Key` (OpenAI API key from OpenRouter)
   - `🔗 WEBHOOK_URL` (Slack Webhook URL)
   - `✉️ your_email@gmail.com` and `🔒 app_password` (Gmail credentials for email alerts)

## 🏃‍♂️ Usage
1. Open 📓 Jupyter Notebook and run the script.
2. Enter feedback in the 📝 text area and click **🔍 Analyze Feedback**.
3. View sentiment results and receive **💬 Slack/email alerts** if feedback is negative.

## 📌 Example
### 📝 Input:
> "The room was dirty, and the staff was very rude."

### ✅ Output:
```
Sentiment: NEGATIVE
Areas of Concern: Cleanliness,  Staff Service
📧 Email alert sent!
🚨 Slack alert sent!
```

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
## 💡 Acknowledgments

- 🤖 Thanks to [OpenAI](https://openai.com) for their cutting-edge AI models.
- 🎯 Kudos to [Slack](https://slack.com) for making real-time alerts so easy!
- 💻 Special thanks to the open-source community for inspiration and support.

---

⭐ **If you find this project helpful, give it a star!** ⭐
``` 


🎉 Start today and enhance customer satisfaction with tailored recommendations!  

---  
