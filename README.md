# Studysnap 📚
**Snap it. Learn it.**

Studysnap is a study helper app. Take a photo of a problem, diagram, textbook page, or your notes, and the AI explains it in simple language, step by step. When you're done, send the explanation straight to your WhatsApp so you can save it for later.

## Features

- Upload a photo (JPG or PNG) or type a question
- Get a simple, step-by-step explanation from Google Gemini
- Chat back and forth to ask follow-up questions
- Send a summary of the conversation to your WhatsApp with one click

## Built With

- Python
- Streamlit (web interface)
- Google Gemini API (AI explanations)
- Twilio WhatsApp API (sending messages)

## Project Structure

- app.py : main app (chat interface and WhatsApp sending)
- prompts.py : system prompt, welcome message, summary prompt
- requirements.txt : list of Python packages needed
- .streamlit/secrets.toml : your private keys (NOT uploaded to GitHub)

## How to Run It

### 1. Download the project

Run: git clone https://github.com/Mamidipaka-Abhishek/snapstudy 

Then run: cd studysnap

### 2. Install the packages

Run: pip install -r requirements.txt

### 3. Add your keys

Create a file at .streamlit/secrets.toml and add these 5 lines with your own values:

- GEMINI_API_KEY = "your-gemini-key"
- TWILIO_ACCOUNT_SID = "your-twilio-sid"
- TWILIO_AUTH_TOKEN = "your-twilio-token"
- TWILIO_WHATSAPP_FROM = "whatsapp:+14155238886"
- TWILIO_CONTENT_SID = "your-template-sid"

(Write each one as a separate line, without the dash at the start.)

Where to get them:

- Gemini key: Google AI Studio (aistudio.google.com)
- Twilio values: your Twilio Console (console.twilio.com). If you use the WhatsApp sandbox, your phone must join the sandbox first.

### 4. Start the app

Run: streamlit run app.py

The app opens in your browser at http://localhost:8501

## How to Use

1. Enter your name and WhatsApp number (with country code, e.g. +91XXXXXXXXXX)
2. Upload a photo or type a question
3. Read the explanation and ask follow-ups if you need
4. Click **Send to WhatsApp** to get the summary on your phone

## Important Note

Never upload secrets.toml to GitHub. It contains private keys. Add it to your .gitignore file.

## Author

Made by **Abhishek.**