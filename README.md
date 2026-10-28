# 📊 FinTracker — AI-Powered Personal Finance Dashboard

FinTracker is a secure, full-stack web application designed to help users **track, analyze, and predict their expenses**.  
It goes beyond traditional finance apps by integrating **Machine Learning models** and a **Large Language Model (LLM)** for personalized financial advice.

---
## Deployed link
https://fin-tracker-hazel.vercel.app/

## 🚀 Key Highlights

- 📈 Predict future spending using ML (burn-rate forecasting)
- 🚨 Detect unusual expenses using anomaly detection
- 🤖 AI-powered financial assistant (FinBot)
- 🔐 Secure authentication with JWT
- 📊 Interactive dashboards and visualizations

---

## 🧠 Machine Learning Features

### 📈 Predictive Analytics (Burn Rate)
- Uses **Linear Regression** on daily spending data  
- Forecasts end-of-month expenses  
- Displays predicted trajectory on charts  

### 🚨 Anomaly Detection
- Uses **Isolation Forest**  
- Identifies unusual transactions (spikes/outliers)  
- Helps detect unexpected expenses  

### 🧹 Data Processing
- Outlier filtering using **IQR (Interquartile Range)**  
- Clean time-based dataset for better predictions  

---

## 🤖 FinBot — AI Financial Assistant

FinBot acts as an intelligent financial assistant that analyzes the user's spending behavior and provides personalized financial guidance.

- Built using **Google Gemini API (gemini-2.5-flash)**
- Uses **RAG (Retrieval-Augmented Generation)** to provide responses based on the user's actual financial data
- Retrieves relevant **real-time SQL insights** such as spending patterns, transaction history, and category-wise expenses
- Injects the retrieved financial context into the LLM prompt before generating a response
- Provides **context-aware and personalized** financial recommendations instead of generic financial advice

Provides:
- Spending insights
- Budget suggestions
- Smart recommendations
- Identification of spending patterns
- Personalized financial guidance

### 🔄 How FinBot Works

**User Query → PostgreSQL Data Retrieval → Relevant Financial Context → Gemini LLM → Personalized Response**

For example, when a user asks *"Why did I spend more this month?"*, FinBot can retrieve the user's recent transaction and category data, analyze the spending pattern, and use Gemini to generate an understandable explanation and recommendation. 

---

## 🏗️ Tech Stack

### Frontend
- React.js  
- React Router DOM  
- Custom CSS (dark theme + animations)  

### Backend
- Python (Flask)  
- Flask-JWT-Extended  
- Flask-CORS  

### Database
- PostgreSQL  
- psycopg2  

### Machine Learning
- pandas, numpy  
- scikit-learn  

### Deployment
- Render  

---

## 🔐 Security Features

- JWT-based authentication  
- Password hashing (Werkzeug)  
- Protected routes  
- Input validation  
- Chronological lock (no future transactions)  

---

## ⚙️ Core Features

### 1. Secure Authentication
- User registration & login  
- Encrypted passwords  
- JWT-based sessions  

### 2. Smart Transaction Management
- Add expenses with category & timestamp  
- Real-time balance updates  
- Strict validation system  

### 3. Predictive Analytics
- Daily spending aggregation  
- Monthly forecast  
- Interactive charts  

### 4. Anomaly Detection
- Flags unusual spending automatically  

### 5. AI Assistant (FinBot)
- Context-aware financial advice  
- Uses real-time database insights  
- Fallback system for reliability  

---

## 📊 System Architecture

User → React → Flask API → PostgreSQL  
                             ↓  
                     ML Models (Regression + Isolation Forest)  
                             ↓  
                     Gemini API (FinBot)  

---



## 🚀 Future Improvements

- ARIMA / LSTM models  
- Mobile app  
- Bank API integration  
- Budget planning features  

---

## 🛠️ Setup

```bash
git clone <your-repo-url>

cd frontend
npm install
npm run dev

cd backend
pip install -r requirements.txt
python app.py
```

---

