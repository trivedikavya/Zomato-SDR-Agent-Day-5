# Zomato SDR Agent 💼

Zomato SDR Agent is an AI-powered voice application designed to function as a Sales Development Representative (SDR) for Zomato for Business. The agent, named Marcus, engages with potential leads via voice, answers their questions using a company knowledge base, and naturally collects qualifying information for a CRM.

## 🚀 Features

* **Professional Voice Interface**: Uses the "Marcus" professional promo voice from Murf AI to provide a high-quality, sales-oriented experience.
* **Intelligent Lead Qualification**: Powered by Google Gemini 2.0 Flash to naturally gather details such as name, company, role, team size, use case, and timeline during conversation.
* **Real-time CRM Dashboard**: A live frontend display that updates as the agent extracts information from the user's speech.
* **Knowledge-Based FAQs**: Marcus answers specific questions about listing costs, advertising (Zomato Ads), and platform benefits based on official company data.
* **Automated Lead Capture**: Once a session is completed (e.g., the user says "thanks" or "bye"), the finalized lead data is automatically saved to a local `leads.json` file.

## 🛠️ Tech Stack

### Backend

* **Framework**: FastAPI.
* **Conversational AI**: Google Gemini 2.0 Flash (SDR Reasoning).
* **Speech-to-Text**: AssemblyAI (Transcription).
* **Text-to-Speech**: Murf AI (Professional Voice Generation).
* **Data Storage**: JSON-based logging (`leads.json`).

### Frontend

* **Styling**: Tailwind CSS with a clean, CRM-inspired design.
* **Logic**: Vanilla JavaScript with ES Modules.
* **API Client**: Axios for handling voice and data transmission.

## 📂 Project Structure

```text
├── backend/
│   ├── main.py             # FastAPI app entry and CORS config
│   ├── routes.py           # SDR logic and API endpoints
│   ├── company_data.json   # Knowledge base and FAQ data
│   ├── requirement.txt     # Python dependencies
│   └── leads.json          # Captured lead data (auto-generated)
├── frontend/
│   ├── index.html          # Split-screen UI (Agent/CRM)
│   ├── index.js            # Voice recording and UI update logic
│   └── package.json        # Frontend dependencies
└── .env                    # API keys for Google, AssemblyAI, and Murf

```

## ⚙️ Setup & Installation

### Backend

1. Navigate to the `backend` directory.
2. Install required packages:
```bash
pip install -r requirement.txt

```


3. Add your API keys to a `.env` file:
```env
GOOGLE_API_KEY=your_gemini_key
ASSEMBLYAI_API_KEY=your_assemblyai_key
MURF_AI_API_KEY=your_murf_key

```


4. Run the server:
```bash
python main.py

```



### Frontend

1. Navigate to the `frontend` directory.
2. Install dependencies:
```bash
npm install

```


3. Open `index.html` using a local development server (e.g., Live Server).

## 📖 How to Use

1. **Start Call**: Click "Start Call" to initiate the session with Marcus.
2. **Engage**: Use the microphone button to talk. You can ask about Zomato for Business or tell Marcus about your restaurant.
3. **Monitor CRM**: Watch the "Live Lead Data" panel on the right update in real-time as Marcus identifies your role, company, and needs.
4. **Finish**: End the conversation naturally. Marcus will summarize the call and save your details for the sales team.
