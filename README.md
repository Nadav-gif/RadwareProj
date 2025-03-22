# 🔐 WAF Log Analyzer with LLM-Powered Attack Summarization

**WAF-Analyzer** investigates Web Application Firewall (WAF) logs to detect and summarize malicious activity, using rule-based filtering and a Large Language Model (LLM).

---

## 📌 Features
- **Log Filtering**: Removes false positives and low-severity incidents, and detects significant attacks like multi-step sequences.
- **LLM Integration (Groq API)**: Generates natural-language summaries of attacker behavior and mitigation strategy.
- **JSON Mode**: Console-based mode for structured output in automation-friendly format.
- **Interactive Streamlit Dashboard**: Visualize attacker stories and filter by IP.

---

## ⚙️ Requirements
- Python 3.10+
- Groq API key

Install dependencies:
```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run

When running the project, you must provide the following **three required arguments**:

| Argument       | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `--output`     | Output mode: `UI` for the interactive dashboard or `JSON` for console output. |
| `--api_key`    | Your API key for authenticating with the LLM (Groq) API.                    |
| `--file_path`  | Path to the WAF log CSV file you want to analyze.

### Option 1: JSON Mode
```bash
python proj.py --output JSON --api_key GROQ_API_KEY --file_path path/to/security_events.csv
```
🖼 Example Output:
![image](https://github.com/user-attachments/assets/8ac94162-4302-4913-8e9f-d8df915fd499)


### Option 2: UI Mode
```bash
python proj.py --output UI --api_key GROQ_API_KEY --file_path path/to/security_events.csv
```
🖼 Example Output:
![image](https://github.com/user-attachments/assets/f08eea90-16f1-4148-bcc6-19c90f956b9f)
