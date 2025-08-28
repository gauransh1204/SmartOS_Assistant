# 📘 SmartOS – Voice/Chat-Based AI OS Assistant (Prototype v1.0)

**Author:** Gauransh Gautam
**Prepared for:** myOnsite Healthcare, LLC

---

## 📌 Project Overview

SmartOS is a lightweight AI assistant that allows users to control their desktop using **natural language commands**. It supports **file management, application launching, and connectivity control**, with **automatic logging** of all actions for evaluation.

Designed as a *“local ChatGPT meets Windows Spotlight”*, SmartOS demonstrates how AI-driven intent parsing can simplify system tasks, with applications in healthcare (e.g., *“create patient record”*, *“log prescription”*).

---

## ⚙️ Features

* **Natural Language Understanding (NLU):** Regex-based intent detection.
* **Task Execution:** Open apps, create files, write notes, mock Wi-Fi control.
* **Fallback Handling:** Friendly message for unrecognized commands.
* **Logging:** Every task is logged to both JSON and Excel.
* **Sandbox Mode:** File operations are safely contained in `smartos_sandbox/`.

---

## 🚀 How to Run

1. Open `SmartOS_Standalone.ipynb` in Jupyter Notebook.
2. Run all cells step by step.
3. Try sample commands like:

   * `create file called notes.txt`
   * `write patient has fever to notes.txt`
   * `open notepad`
   * `connect to wifi`
   * `how are you?`

---

## 📂 Output & Logs

* Files created in: **`smartos_sandbox/`**
* Logs stored in: **`smartos_logs/`**

  * `results.jsonl` → raw JSON logs
  * `results.xlsx` → structured log for evaluation

**Log schema:**

| Field       | Description              |
| ----------- | ------------------------ |
| Test Name   | Intent executed          |
| Description | Original user command    |
| Status      | Success / Fail           |
| Error       | Error details (if any)   |
| Latency     | Execution timestamp (ms) |

---

## ✅ Evaluation Criteria

* > 90% pass rate on test cases (covered by regex intents).
* <3s response time for majority of tasks (instant execution).
* Fully autonomous task execution without manual correction.

---

## 🔮 Future Improvements

* Add **voice input** (SpeechRecognition).
* Integrate **LLM (Claude/GPT)** for robust intent parsing & fallback chat.
* Add **screenshot/error capture** for logs.
* Extend for **healthcare workflows**: patient records, prescriptions, test reports.

---

💡 **SmartOS Prototype demonstrates the foundation of a healthcare-ready AI OS assistant.**
