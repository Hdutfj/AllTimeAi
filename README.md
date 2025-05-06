# 🤖 AllTimeAi

AllTimeAi is an interactive AI-powered assistant built using **Chainlit** and **Gemini API**, designed to respond to user queries in a smart and structured way. It maintains conversation history, handles session-based chat, and sends responses through a visually friendly interface.


## ✨ Features

- 🔁 **Real-time Chat** interface with conversational history.
- 🤝 **Session-based memory** using Chainlit's user session.
- 🤖 **Gemini API** integration for intelligent responses.
- 💬 Friendly greeting and clear, structured output.
- ✅ Easily extendable for advanced assistants.

---

## 🛠️ Tech Stack

- Python
- [Chainlit](https://docs.chainlit.io/)
- Google Gemini API
- `dotenv` for secure API key management

---

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- Git
- pip

### Setup Steps

```bash
# 1. Clone the repo
git clone https://github.com/Hdutfj/AllTimeAi.git
cd AllTimeAi

# 2. Install dependencies
pip install -r requirements.txt

# 3. Add your API key
Create a .env file and add:
GEMINI_API_KEY=your_api_key_here

# 4. Run the bot
chainlit run probi.py



