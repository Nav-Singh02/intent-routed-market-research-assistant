# Intent-Routed AI Market Research Assistant 🧠📊

This project showcases a scalable, AI-powered market research workflow built using **n8n**, **OpenAI**, and **Cursor** prompt engineering.

It automates topic classification, industry-specific summarization, and email delivery of insights — all based on real-time user inputs.

---

## 🧩 Workflow Overview

1. **User Input**  
   The user submits a research topic (e.g. "Pfizer stock margin").

2. **Intent Classification**  
   OpenAI classifies the input into one of three categories:
   - Finance
   - Healthcare
   - General

3. **Topic Routing**  
   The workflow uses a switch node to route content to the corresponding summarizer agent.

4. **Industry-Specific AI Agent**  
   Each agent has a unique prompt (created in Cursor) fine-tuned for:
   - Financial analysis
   - Clinical healthcare trends
   - General market insights

5. **Summary Output**  
   The selected LLM returns a clean, structured summary relevant to the topic and industry.

6. **Email Dispatch**  
   A formatted email is automatically sent containing the topic and AI-generated insight.

---

## 💡 Why This Was Built

This project simulates how research teams or business units could automate inbound questions or early-stage topic exploration. Its modular structure allows organizations to plug in any number of specialized summarizers — for law, tech, retail, etc.

A single input field + AI routing + industry agents = scalable internal automation.

---

## 📬 Example Output

> **Subject**: *Pfizer stock margin – Insight Digest*  
>  
> **🧠 Market Research Summary**  
> **Topic**: Pfizer stock margin  
>  
> **Summary**: Pfizer Inc. (PFE) has recently captured investor attention... *(see screenshot in repo)*

---

## 🛠️ Tech Stack

- **n8n** for workflow orchestration
- **OpenAI GPT-4** for classification + summarization
- **Cursor** for prompt engineering
- **Gmail Integration** for delivery

---

## 📁 Files Included

- `intent_routed_market_research.json` – Full n8n workflow
- `example_email.png` – Screenshot of final email
- `README.md` – This file

---

## 🧪 Example Inputs to Try

- **Finance**: `"Pfizer stock margin"`  
- **Healthcare**: `"Breakthrough in gene therapy for rare diseases"`  
- **General**: `"Rise of sustainable consumer products"`

---

## 📈 Future Improvements

- Add additional industry branches (e.g., Tech, Legal)
- Connect to Slack or Notion instead of email
- Build a front-end UI to trigger the workflow with user prompts

---

