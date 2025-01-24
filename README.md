

# 🏨 Hotel Management System  


# 📝 Sentiment Analysis & 🚨 Slack Alert System

Analyze hotel guest feedback seamlessly and get real-time alerts for negative sentiments directly in your Slack workspace! 🎯

---

## 🌟 Features

✨ **Interactive Feedback Input**  
Easily input guest feedback using a clean and simple interface powered by `ipywidgets`.

🤖 **AI-Powered Sentiment Analysis**  
Leverages OpenAI's advanced models to detect feedback sentiment as **Positive**, **Neutral**, or **Negative**.

🔍 **Identify Areas of Concern**  
In case of negative feedback, the system pinpoints the responsible areas (e.g., Room Quality, Staff Service, etc.).

📢 **Real-Time Slack Alerts**  
Automatically sends a detailed alert to Slack for negative feedback, keeping your team informed and proactive.

---

## 🚀 Quick Start

### 🛠️ Prerequisites

Make sure you have Python installed and install the following packages:  

```bash
pip install pydantic slack_sdk ipywidgets openai
```

### 🔑 Setup

1. **API Key Configuration**  
   - Get your OpenAI API key from [OpenAI](https://beta.openai.com/signup/).  
   - Replace `Your_API_Key` in the code with your actual API key.

2. **Slack Webhook URL**  
   - Set up a webhook URL for your Slack workspace by following the [Slack Webhook Guide](https://api.slack.com/messaging/webhooks).  
   - Replace `WEBHOOK_URL` in the code with your Slack Webhook URL.

3. **Run the Code**  
   - Launch the script in a Jupyter Notebook.  
   - Enter guest feedback in the text area and click "Analyze Feedback" to perform sentiment analysis.

---

## 📋 Example Usage

1. **Input Feedback**  
   Enter feedback like:  
   `"The room was dirty, and the staff was rude!"`

2. **Output in Jupyter Notebook**  
   ```
   ✅ Analysis complete!
   Sentiment: NEGATIVE
   Areas of Concern: Room Quality, Staff Service
   ```

3. **Slack Alert**  
   The following message is sent to Slack:  
   ```
   🚨 *Negative Feedback Alert* 🚨
   *Timestamp:* 2025-01-24 12:30:00
   *Feedback:* "The room was dirty, and the staff was rude!"
   *Sentiment:* NEGATIVE
   *Areas of Concern:* Room Quality, Staff Service
   ```

---


---

## 🛠️ Code Highlights

### Core Components  

- **Pydantic Model for Structure**  
   Ensures feedback analysis results are validated and well-structured:  
   ```python
   class Sentiment(BaseModel):
       sentiment: str
       responsible_area: str
   ```

- **Slack Alert Function**  
   Sends formatted feedback alerts to Slack channels:  
   ```python
   def send_slack_alert(feedback, sentiment, areas_of_concern):
       slack_message = f"""
       🚨 *Negative Feedback Alert* 🚨
       *Feedback:* {feedback}
       *Sentiment:* {sentiment.upper()}
       *Areas of Concern:* {', '.join(areas_of_concern)}
       """
       slack_client.send(text=slack_message)
   ```

- **Sentiment Analysis with OpenAI**  
   Integrates OpenAI’s API for contextual feedback understanding:  
   ```python
   completion = client.chat.completions.create(
       model="google/learnlm-1.5-pro-experimental:free",
       messages=[
           {"role": "system", "content": "Analyze this feedback..."},
           {"role": "user", "content": feedback}
       ]
   )
   ```

---

## 🤝 Contributing

We welcome contributions! Here’s how you can help:

1. Fork the repository 🍴  
2. Create your feature branch: `git checkout -b feature/my-feature`  
3. Commit your changes: `git commit -m 'Add some feature'`  
4. Push to the branch: `git push origin feature/my-feature`  
5. Submit a pull request 🛠️  

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
