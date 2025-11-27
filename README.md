# 🧬 Darwinian Analyst Swarm
### *AI Agents that Read, Reason, and Trade.*

![Project Thumbnail Header](./images/thumbnail_placeholder.jpg)
*(This image will serve as the project card thumbnail)*

---

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Python](https://img.shields.io/badge/python-3.10%2B-blue) ![LangChain](https://img.shields.io/badge/LangGraph-Agentic-orange) ![Gemini](https://img.shields.io/badge/Powered%20By-Gemini%201.5-8E75B2)

> **"A self-correcting AI workforce that reads, reasons, and trades faster than any human."**

---

## 📖 Project Overview

**The Problem:**
In the financial world, information is infinite, but attention is scarce. By the time a human trader reads a report on a tech regulation change in the EU or a startup breakthrough in Asia, the market has already moved. Traditional trading bots are brittle; they follow strict `if/then` rules and cannot understand nuance, sentiment, or conflicting reports.

**The Solution:**
The **Darwinian Analyst Swarm** is an autonomous multi-agent system fueled by **Google Gemini**. Instead of a single script, it deploys a "team" of AI agents:
1.  **News Hunter:** Scours the web for real-time data.
2.  **Analyst Swarm:** Multiple AI personas debate the significance of the news.
3.  **Portfolio Manager:** A "Judge" agent that weighs the arguments and makes the final executive decision.
4.  **Trader:** Executes the trade via the Alpaca API.

---

## 🏗️ Architecture

This project uses **LangGraph** to create a stateful, cyclic workflow. Unlike linear chains, this graph allows agents to pass "memory" (state) back and forth, enabling complex reasoning.

### The Flow
1.  **Input:** User provides a stock ticker (e.g., `$NVDA`).
2.  **Ingestion:** The **News Hunter** uses DuckDuckGo to fetch live financial news.
3.  **Analysis (The "Swarm"):** The **Analyst Agent** (Gemini 1.5) reads the raw text, filtering out noise and assigning a sentiment score based on reasoning.
4.  **Decision:** The **Portfolio Manager** reviews the Analyst's findings. It acts as a risk gatekeeper—only approving trades with high conviction.
5.  **Execution:** If approved, the **Trader Agent** connects to the **Alpaca Paper Trading API** to execute the buy/sell order in real-time.

![Architecture Workflow Diagram](Gemini_Generated_Image_g8dm7yg8dm7yg8dm.png)
*(Detailed agentic workflow flow diagram)*

---

## 🚀 Features

* **Multi-Agent Collaboration:** Agents have distinct roles and responsibilities.
* **Tool Use:** Agents autonomously use search tools to find fresh data.
* **Reasoning Engine:** Uses **Gemini 1.5 Flash/Pro** to understand context, not just keywords.
* **Real-Time Execution:** Integrated with Alpaca Markets for live paper trading.
* **Modular Design:** Built on LangChain/LangGraph, making it easy to add new "Analyst Personas" later.

---

## 🛠️ Technology Stack

* **Language:** Python 3.10+
* **Orchestration:** LangChain & LangGraph
* **LLM (Brain):** Google Gemini 1.5 Flash
* **Brokerage (Action):** Alpaca Trade API (Paper Trading)
* **Search (Data):** DuckDuckGo Search

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/YOUR_USERNAME/darwinian-analyst-swarm.git](https://github.com/YOUR_USERNAME/darwinian-analyst-swarm.git)
cd darwinian-analyst-swarm
