![AI](https://img.shields.io/badge/AI-LLM--Powered-blue)
![Automation](https://img.shields.io/badge/Automation-n8n-orange)
![Platform](https://img.shields.io/badge/Bot-Telegram-26A5E4)
![Visualization](https://img.shields.io/badge/Output-Visual%20Diagrams-purple)
![Status](https://img.shields.io/badge/Status-Early%20MVP-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

# MindFlow Visual Tutor 🧠

MindFlow Visual Tutor is an **AI-powered visual learning and Q&A bot** that helps learners understand **complex YouTube lectures** by converting them into **structured learning flows, visual diagrams, and interactive explanations**.

It focuses on clarity over summaries:
**Watch → Structure → Visualize → Ask → Understand**

---

## 🚩 Problem Statement

Long-form educational videos are difficult to learn from effectively.
Not because the content is bad, but because:

* Core ideas are hidden inside long explanations
* Learning order is unclear
* Diagrams are missing or too abstract
* Learners don’t know *which part to focus on*
* Questions require rewatching the entire lecture

MindFlow Visual Tutor solves this by **rebuilding the teaching logic** of a lecture into a **clear visual learning flow** with interactive Q&A.

---

## 🚀 What MindFlow Visual Tutor Does

* Accepts a YouTube lecture link via Telegram
* Extracts and cleans the video transcript
* Identifies the **core learning sequence**
* Rewrites concepts for **beginner understanding** (without removing technical terms)
* Generates a **visual flow diagram** from the learning steps
* Sends the diagram directly to the learner
* Allows users to **ask questions about any step or node**
* Answers questions using **only the generated diagram and learning flow**

No hype. No hallucinations. Just understanding.

---

## 🧠 How It Works (High-Level Flow)

1. User sends a YouTube lecture link on Telegram
2. Link is validated by the system
3. Transcript is fetched from YouTube
4. Transcript text is cleaned and normalized
5. Core learning flow is extracted
6. Learning flow is rewritten for beginners
7. Visual diagram is generated
8. Diagram is rendered as an image
9. Diagram and learning steps are delivered
10. User asks questions about the diagram
11. System explains until doubts are cleared

---

## 🧱 Architecture Overview

* **Telegram Bot** → User interaction layer
* **n8n** → Workflow orchestration and routing
* **Groq-hosted LLMs** → Concept extraction and diagram generation
* **Local LLaMA 3.2 (Ollama)** → Interactive question answering
* **Mermaid.js** → Diagram creation
* **Kroki** → Diagram rendering
* **Supadata API** → YouTube transcript extraction

All logic and reasoning are handled inside n8n workflows.

---

### 🖼️ Automation Workflow

![Workflow Screenshot](assets/mindflow-workflow.png)

---

## 🛠️ Tools & Technologies

* **n8n** – Automation and workflow orchestration
* **Telegram Bot API** – User interaction
* **Supadata API** – YouTube transcript extraction
* **Groq LLMs** – Reasoning and diagram generation
* **Ollama (LLaMA 3.2)** – Local Q&A model
* **Mermaid.js** – Diagram language
* **Kroki** – Diagram rendering service

---

## 📂 Repository Structure (Suggested)

```
mindflow-visual-tutor/
│
├── workflows/
│   └── mindflow-visual-tutor.json
│
├── prompts/
│   ├── EXTRACT CORE LEARNING FLOW.md
│   ├── LEARNING ARCHITECT.md
│   ├── VISUAL ARCHITECT..md
│   └── Answer Question Using Diagram.md
│
├── assets/
│   ├── demo.mp4
│   └── mindflow-workflow.png
│
└── README.md
```

---

## 🤖 Telegram Bot (Demo)

Bot link:

```
[https://t.me/MindFlow_VisualTutor_bot]
```

### ⚠️ Note

This bot runs on a **locally self-hosted n8n setup**.
Availability may vary depending on runtime and tunneling.

---

## ⚠️ Important Disclaimers

* This tool is for **learning assistance only**
* Diagrams represent **one logical teaching flow**, not all interpretations
* Explanations are grounded strictly in extracted lecture content
* No external knowledge is injected during Q&A

---

## 🧪 Project Status

* Current stage: **Early / MVP version**
* Focus: Learning clarity, correctness, and visual understanding

---

## 🤝 Contributions

This is a personal build-in-public project.
Feedback, suggestions, and improvements are welcome.

---

## 📬 Contact

If you tested the system or have feedback:

* Reach out via LinkedIn
* Open an issue in this repository

---

## ⭐ Acknowledgement

Built to explore how **visual structure and interaction** can improve learning from long-form educational content.

---

**MindFlow Visual Tutor** — learn by seeing, not rewatching.
