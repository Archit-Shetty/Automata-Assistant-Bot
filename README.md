##🤖 AutomataBot: An LLM-Powered Chatbot for Automata Theory & Compiler Design
AutomataBot is an AI assistant that leverages the Google Gemini API to provide intelligent support for topics in Automata Theory and Compiler Design. It features a lightweight Flask backend and an interactive JavaScript frontend to deliver a real-time chat experience.

🧠 Project Architecture & Working Process
The system follows a clear three-layer architecture:

Frontend — The user interacts via a browser-based chat interface.
Backend — A Flask server receives and processes requests.
AI Model — The backend sends queries to the Gemini LLM and returns its responses.

🔄 Query Flow:

User Input — The user submits a message through the chat interface.
Frontend → Backend — JavaScript (fetch API) sends the input to the Flask server.
Backend → AI — The server authenticates using the API key and sends the query to Gemini.
AI Response — Gemini processes the query and returns a response.
Backend → Frontend — The server sends the AI response back to the frontend.
Frontend Displays — JavaScript renders the message in the chat UI.

💻 Technologies Used
Frontend:
HTML, CSS, JavaScript — For the UI and client-side behavior
AJAX — To send and receive data from the backend asynchronously

Backend:
Python — Core server language
Flask — Handles routing and API requests
flask-cors — Manages cross-origin requests for frontend-backend communication
google-generativeai — Connects to the Google Gemini API

AI:
Google Gemini API — Provides LLM capabilities
Model: gemini-1.5-flash — Optimized for speed and cost-effectiveness


⚙️ How to Run the Project
✅ Prerequisites:
1. Python 3.6+
2. A valid Google Gemini API key

📦 Step 1: Clone & Set Up the Backend

> git clone https://github.com/YourUsername/automata-llm-bot.git
> cd automata-llm-bot
> python -m venv venv

Activate the virtual environment:

Windows: venv\Scripts\activate
macOS/Linux: source venv/bin/activate

Install dependencies:

> pip install -r requirements.txt

🔐 Step 2: Configure Your API Key
In app.py, find this line:

genai.configure(api_key=os.environ.get("GOOGLE_API_KEY"))

Replace it (for local testing only) with:

genai.configure(api_key="YOUR_ACTUAL_API_KEY_HERE")

🚀 Step 3: Run the Server

> python app.py
Then open index.html in your browser to start chatting with AutomataBot!

🧪 Features:

✅ LLM-based Q&A on formal languages and compiler topics
✅ Streamlined client-server communication
✅ Fast and responsive chat UI
✅ Easy local setup and API integration
✅ Clean and modular architecture
