# Financial Multi-Agent System

This project uses the `agno` framework to create a multi-agent system capable of analyzing financial data and conducting web searches. It includes two specialized agents:

- **Web Agent**: Searches the web for information using DuckDuckGo.
- **Finance Agent**: Uses Yahoo Finance to retrieve company financials, stock prices, analyst recommendations, and company info.

The agents are orchestrated as a team to collaboratively analyze companies like Tesla, Nvidia (NVDA), and Apple, and provide investment suggestions for long-term strategies.

---

## 🧠 Agents Overview

### Web Agent
- **Purpose**: Search the web for relevant and recent information.
- **Model**: `qwen-2.5-32b` via Groq.
- **Tool**: `DuckDuckGoTools`
- **Special Instructions**: Always include sources.

### Finance Agent
- **Purpose**: Retrieve detailed financial data.
- **Model**: `gpt-4o` via OpenAI.
- **Tools**: `YFinanceTools` with access to:
  - Stock price
  - Analyst recommendations
  - Stock fundamentals
  - Company information
- **Special Instructions**: Use tables to display data.

### Agent Team
- Combines both agents with a shared goal.
- Runs on `qwen-2.5-32b`.
- Responds using markdown with tool call visibility for transparency.

---

## 🔧 Setup

### 1. Clone the repository
```bash
git clone https://github.com/your-username/financial-agent-system.git
cd financial-agent-system
