# 🌾 FarmConnect

**FarmConnect** is a full-stack agricultural marketplace that directly connects farmers with consumers by eliminating middlemen and ensuring fair pricing. Farmers can list their crops, receive ML-based MSP pricing suggestions, chat with buyers, and accept secure online payments.

---

## 🚀 Features

### 👨‍🌾 For Farmers
- OTP-based signup/login
- Crop listing with images, quantity & pricing
- ML-predicted Minimum Support Price (MSP) suggestions (Flask)
- Secure online UPI payments via Razorpay
- Real-time chat with consumers (MERN Stack)

### 🛒 For Consumers
- OTP-based authentication
- Browse/search available crops
- UPI payment support
- Real-time chat with farmers
- View order & payment history



## 🛠️ Tech Stack

| Component         | Technology                                      |
|------------------|--------------------------------------------------|
| Frontend         | React.js (`chat_app_mern/frontend`)              |
| Chat Backend     | Node.js + Express (`chat_app_mern/backend`)      |
| Main Web Backend | Spring Boot + MySQL (`farmersmarket/`)           |
| Chat Database    | MongoDB                                          |
| ML API           | Flask (`model.py`)                               |
| Payment API      | Flask + Razorpay (`payment.py`)                  |



## 📁 Folder Structure
FarmConnect/
├── chat_app_mern/ # MERN stack chat application
│ ├── backend/ # Node.js + MongoDB server
│ └── frontend/ # React UI
├── farmersmarket/ # Spring Boot backend
├── model.py # Flask ML prediction API
├── payment.py # Flask Razorpay integration
├── requirements.txt # Python dependencies
└── README.md # Project documentation



## 📊 Dataset Information

- **Source:** Agmarknet – Price & Arrivals
- **Google Drive Dataset:** *(Insert your link here)*  
- **Configured in:** `model.py`

```python
BASE_PATH = "C:\\Users\\harshada\\Documents\\FarmConnect\\dataset\\"


## ⚙️ Setup Instructions
1. Clone the Repository
    git clone https://github.com/yourusername/FarmConnect.git
    cd FarmConnect

2. Start MERN Application (Frontend + Chat Backend)
    cd chat_app_mern
    npm install
    npm run build      # optional for production build
    npm start          # runs both frontend & backend

3. Run the Spring Boot Backend
    cd farmersmarket
    ./mvnw spring-boot:run

 🔐 Configure Application Properties

    Edit farmersmarket/src/main/resources/application.properties
    
    Email Configuration:

        spring.mail.host=smtp.gmail.com
        spring.mail.port=587
        spring.mail.username=YOUR_EMAIL
        spring.mail.password=YOUR_EMAIL_APP_PASSWORD
        spring.mail.properties.mail.smtp.auth=true
        spring.mail.properties.mail.smtp.starttls.enable=true


MySQL Configuration:

    spring.datasource.url=jdbc:mysql://localhost:3306/YOUR_DB_NAME?useSSL=false&serverTimezone=UTC&allowPublicKeyRetrieval=true
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.datasource.username=root
    spring.datasource.password=YOUR_PASSWORD

4.  Run ML Prediction API
    python model.py

5. Run Razorpay Payment API
    python payment.py


## 🔐 Environment Variables
    For payment.py
    
    RAZORPAY_KEY_ID=your_razorpay_key
    RAZORPAY_KEY_SECRET=your_razorpay_secret
    
    For Chat App (chat_app_mern/.env)
    
    PORT=8000
    MONGO_URI=mongodb://localhost:27017/chatapp

## 📦 Python Requirements

    Install dependencies for ML and Payment Flask apps:
    
    pip install -r requirements.txt

## ✅ requirements.txt contains:

    flask==2.3.3
    flask-cors==4.0.0
    razorpay==1.3.0
    pandas==2.2.1
    numpy==1.26.4
    scikit-learn==1.4.1.post1
    xgboost==2.0.3
    catboost==1.2.5
    joblib==1.4.2

## 🤝 Contributing

    Want to help improve FarmConnect?
    Feel free to fork, open pull requests, or raise issues.
    For major changes, please start a discussion.

##✨ Author
Harshada Patil
🔗 https://www.linkedin.com/in/harshada-patil-970672229/
🐙 https://github.com/harshadap1215/
📧 harshadap1215@gmail.com

