🌐 AI Language Translator Web App

A powerful AI-based Language Translator Web Application built using Flask and Google Gemini API. This platform enables users to translate text across multiple languages with authentication and a basic membership/payment system.

🚀 Features
🌍 Multi-language Translation
Supports multiple languages including English, Hindi, Spanish, French, German, Punjabi, Telugu, etc.
🤖 AI-Powered Translation
Uses Gemini 1.5 Flash Model for accurate and fast translations
🔍 Automatic Language Detection
Detects source language automatically using AI
🔐 User Authentication
Signup & Signin system with secure password hashing
💳 Membership System
Simulated payment integration for subscription plans
📦 Database Integration
SQLite database to manage users
⚡ REST API Support
JSON-based API endpoints for translation and language retrieval
🛠️ Tech Stack
Backend: Flask (Python)
AI Model: Google Gemini API
Database: SQLite (SQLAlchemy ORM)
Authentication: Werkzeug Security
Language Detection: langdetect
Frontend: HTML (Flask Templates)
📂 Project Structure
├── main.py              # Main Flask application
├── templates/           # HTML templates (index, signup, signin, payment)
├── users.db             # SQLite database (auto-created)
├── envori.env           # Environment variables (API key)
⚙️ Installation & Setup
1️⃣ Clone the Repository
git clone https://github.com/your-username/language-translator.git
cd language-translator
2️⃣ Install Dependencies
pip install flask flask_sqlalchemy langdetect google-generativeai werkzeug
3️⃣ Setup Environment Variables

Create a .env file and add your Gemini API key:

GEMINI_API_KEY=your_api_key_here

⚠️ Your current project stores API key directly in code — for production, move it to environment variables.

4️⃣ Run the Application
python main.py

App will run on:

http://localhost:5000
🔌 API Endpoints
📌 Get Supported Languages
GET /available_languages
📌 Translate Text
POST /translate

Request Body:

{
  "text": "Hello world",
  "source_language": "auto",
  "target_language": "hi"
}

Response:

{
  "success": true,
  "translated_text": "नमस्ते दुनिया",
  "detected_source_language": "en"
}
🔐 Authentication Routes
/signup → Register new user
/signin → Login
/logout → Logout
💳 Payment Module
/payment → Membership page
/process_payment → Handles payment (simulated)

⚠️ Currently uses mock payment logic. Can be integrated with:

Stripe
Razorpay
PayPal
📊 Key Highlights
Handles up to 5000 characters per translation
AI-based language detection improves usability
Secure password storage using hashing
Modular Flask architecture
🔮 Future Enhancements
✅ Real payment gateway integration (Stripe/Razorpay)
✅ Speech-to-text translation
✅ Text-to-speech output
✅ Translation history dashboard
✅ Multi-user roles (Admin/User)
✅ Deployment on cloud (AWS/Render)
