# 🤖 AutomataBot: An LLM-Powered Chatbot for Automata Theory & Compiler Design
AutomataBot is an AI assistant that leverages the Google Gemini API to provide intelligent support for topics in Automata Theory and Compiler Design. It features a lightweight Flask backend and an interactive JavaScript frontend to deliver a real-time chat experience.

### 🧠 Project Architecture & Working Process
The system follows a clear three-layer architecture:

1. Frontend — The user interacts via a browser-based chat interface. 
2. Backend — A Flask server receives and processes requests. 
3. AI Model — The backend sends queries to the Gemini LLM and returns its responses.

### 🔄 Query Flow:

1. User Input — The user submits a message through the chat interface. 
2. Frontend → Backend — JavaScript sends the input to the Flask server. 
3. Backend → AI — The server authenticates using the API key and sends the query to Gemini. 
4. AI Response — Gemini processes the query and returns a response.
5. Backend → Frontend — The server sends the AI response back to the frontend.
6. Frontend Displays — JavaScript renders the message in the chat UI.

### 💻 Technologies Used
Frontend:
1. HTML, CSS, JavaScript — For the UI and client-side behavior
2. AJAX — To send and receive data from the backend asynchronously

Backend:
1. Python — Core server language
2. Flask — Handles routing and API requests
3. flask-cors — Manages cross-origin requests for frontend-backend communication
4. google-generativeai — Connects to the Google Gemini API

AI:
1. Google Gemini API — Provides LLM capabilities
2. Model: gemini-1.5-flash — Optimized for speed and cost-effectiveness


## ⚙️ How to Run the Project
### ✅ Prerequisites:
1. Python 3.6+
2. A valid Google Gemini API key

### 📦 Step 1: Clone & Set Up the Backend

> git clone https://github.com/Archit-Shetty/Automata-Assistant-Bot.git
> cd Automata-Assistant-Bot
> python -m venv venv

Activate the virtual environment:

Windows: venv\Scripts\activate
macOS/Linux: source venv/bin/activate

Install dependencies:

> pip install -r requirements.txt

### 🔐 Step 2: Configure Your API Key
In app.py, find this line:

genai.configure(api_key=os.environ.get("GOOGLE_API_KEY"))

Replace it (for local testing only) with:

genai.configure(api_key="YOUR_ACTUAL_API_KEY_HERE")

### 🚀 Step 3: Run the Server

> python app.py
Then open index.html in your browser to start chatting with AutomataBot!

### 🧪 Features:

1. LLM-based Q&A on formal languages and compiler topics
2. Streamlined client-server communication
3. Fast and responsive chat UI
4. Easy local setup and API integration
5. Clean and modular architecture
