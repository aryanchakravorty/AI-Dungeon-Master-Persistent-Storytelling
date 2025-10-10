# 🧙‍♂️ AI Dungeon Master for Persistent Storytelling

![Event](https://img.shields.io/badge/Event-Inter%20IIT%20Tech%20Meet%2014.0-blue)
![Language](https://img.shields.io/badge/Language-Python-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)

An intelligent AI Dungeon Master built for **Inter IIT Tech Meet 14.0 (AI/ML Bootcamp)**.  
This system focuses on **long-term narrative coherence** using a **dual-memory architecture**, enabling immersive, persistent storytelling across long gameplay sessions.

---

## ✨ Features

### 🧠 Dual Memory System
- **Working Memory (Short-Term):**  
  Retains immediate scene details and player actions (~5 turns) for responsive storytelling.
- **Persistent Memory (Long-Term):**  
  Stores and retrieves key events, world states, and character data (~30 turns) via **Retrieval-Augmented Generation (RAG)** for long-term consistency.

### 🌍 Dynamic Evolving World
The world evolves logically based on player decisions — NPCs react, locations change, and past choices matter.

### 🤖 Modular LLM Integration
Supports multiple backends:
- Self-hosted models via `llama.cpp`
- Cloud APIs like **Groq** for low-latency inference

### 🛡️ Stability and Coherence
Optimized for **30+ turns** of continuous play without crashes or loss of narrative logic.

---

## 🏆 Bonus Features

- **👥 Character Memory:**  
  NPCs remember prior interactions and evolve their dialogue and behavior dynamically.

- **📜 Dynamic Quest Log:**  
  The system auto-tracks player objectives, updating quest progress and referencing past goals naturally.

---

## ⚙️ System Architecture

The architecture is modular and designed for efficiency, clarity, and scalability:

1. **Player Input:** User action or dialogue.
2. **Memory Processor:** Updates short-term memory and retrieves relevant long-term memories.
3. **Context Augmentation (RAG):** Combines both memory layers with the latest input for LLM processing.
4. **LLM Generation:** Generates the next narrative segment using the augmented context.
5. **State Update:** Summarizes and stores key events in persistent memory.
6. **Narrative Output:** Presents the next part of the story to the player.

Player → Memory Processor → RAG Context → LLM → Game State Update → Story Output


---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Git

### Installation
```bash
git clone https://github.com/YOUR_USERNAME/AI-Dungeon-Master-Persistent-Storytelling.git
cd AI-Dungeon-Master-Persistent-Storytelling
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt

Configuration

Create a .env file in the root directory:

GROQ_API_KEY="your_api_key_here"

Run the Project
jupyter notebook ai_dungeon_master.ipynb


Follow the notebook instructions to start your AI-driven adventure.

📂 Project Structure
.
├── ai_dungeon_master.ipynb     # Main implementation notebook
├── Technical_Report.pdf        # Full technical report
├── requirements.txt            # Dependencies
├── .gitignore                  # Ignored files
└── README.md                   # Project documentation

👥 Team

[Your Name]

[Your Teammate’s Name] (if applicable)

📚 References

For detailed methodology, memory design, and evaluation, see the Technical Report PDF linked above.

🧩 Keywords

AI Dungeon Master • RAG • Memory-Augmented LLM • Storytelling • Groq • Long-Term Coherence • Python


---

### 💡 Optional (if you want to stand out further)
You can also add a **“📸 Screenshots”** section like this (just before *System Architecture*):
```markdown
## 📸 Screenshots
Here’s a glimpse of the AI Dungeon Master in action:
![Gameplay Screenshot](assets/demo_screenshot.png)
