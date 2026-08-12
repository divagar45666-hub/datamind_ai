# datamind_ai

# 📊 DataMind AI

> A local AI-powered natural language interface for querying and analyzing SQLite databases.

DataMind AI allows users to interact with a database using natural language instead of manually writing SQL queries.

Ask questions such as:

- "What is our total revenue?"
- "How many orders do we have?"
- "Which customer spent the most?"
- "Which products are the most expensive?"
- "Show me the top 5 products by revenue."

DataMind converts the natural-language question into SQL using a locally running Qwen model, executes the query against SQLite, and presents the result through an interactive Streamlit interface.


📁 Project Structure :


datamind-ai/
│
├── backend/
│   ├── agent.py
│   └── tools/
│       ├── schema_tool.py
│       ├── query_tool.py
│       └── chart_tool.py
│
├── frontend/
│   └── app.py
│
├── data/
│   └── database.db
│
├── docs/
│   └── screenshots/
│       ├── dashboard.png
│       └── bar-chart.png
│
├── README.md
├── requirements.txt
└── .gitignore

---

## 🚀 Features

- 💬 Natural-language database queries
- 🤖 Local Qwen 2.5 7B model through Ollama
- 🗄️ SQLite database integration
- 🔍 Automatic database schema inspection
- 🧠 AI-generated SQL queries
- 🔐 SQL safety validation
- ⚡ Fast local query execution
- 📊 Interactive data tables
- 📈 Interactive Plotly bar charts
- 🖥️ Streamlit web interface
- 🌐 No cloud database required

---

## 🏗️ Architecture

```text
                    ┌─────────────────────┐
                    │     User Query      │
                    │  Natural Language   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Streamlit UI     │
                    │    frontend/app.py   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Agent Layer     │
                    │    backend/agent.py │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │   Schema Inspector  │
                    │    schema_tool.py   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Local Qwen 2.5   │
                    │       7B + Ollama   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    SQL Validation   │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    SQLite Query     │
                    │    query_tool.py    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Query Result    │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │    Data Visualization│
                    │ Streamlit + Plotly  │
                    └─────────────────────┘


## 🛠️ Tech Stack :

- Python
- Streamlit
- SQLite
- Ollama
- Qwen 2.5 7B
- Plotly

## ⚙️ Installation  :

Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
cd datamind-ai


Create a virtual environment:

python -m venv venv

Activate it on Windows:

venv\Scripts\Activate.ps1

Install dependencies:

pip install -r requirements.txt
🤖 Local LLM

DataMind uses Qwen locally through Ollama.

Make sure the required model is available locally before running the
application.

▶️ Run

Start the Streamlit application:

streamlit run frontend/app.py

The application will open in your browser.

💡 Example Queries :
Which products are the most expensive?
What is our total revenue?
How many orders do we have?
Which customer spent the most?
Show me the top 5 products by revenue.



📌 Future Improvements
More visualization types
Automatic chart selection
Query history
Dashboard generation
Multiple database support
Export results to CSV
Improved SQL validation
Authentication
 
 
 
 👨‍💻 Author: 

Divagar N  (SEC25AM172)
Sri Sairam Engineering College
CSE – Artificial Intelligence & Machine Learning


Team Mates :
Jagadeesh V  (SEC25AM065)
Enzel Benin J S (SEC25AM059)
Aneshyacen S (SEC25AM175)
