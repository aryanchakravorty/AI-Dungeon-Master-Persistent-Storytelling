# AI Dungeon Master for Persistent Storytelling

![Language](https://img.shields.io/badge/Language-Python-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)

An intelligent AI Dungeon Master designed for the Inter IIT Tech Meet 14.0 AI/ML Bootcamp. This project tackles the challenge of long-term coherence in LLM-driven narratives by implementing a robust, dual-component memory architecture. The system is designed to act as a true Dungeon Master, remembering player choices, maintaining world consistency, and weaving an engaging, persistent story across dozens of turns.

---

### 🎥 Live Demo

Check out a short demonstration of the AI DM's short-term and long-term recall capabilities. 

[view the file](https://drive.google.com/file/d/1AbpjBWn2itFiLNvhX645HjWyvUvFA35n4/view?usp=sharing)

---

### ✨ Core Features

This AI DM was built to meet the core objectives of the problem statement, focusing on memory, stability, and immersion.

* **🧠 Intelligent Memory Architecture:** The core of the project.
    * **Working Memory (Short-Term):** Accurately retains scene details and player actions over recent turns (~5 turns) to ensure immediate context is never lost.
    * **Persistent Memory (Long-Term):** Recalls crucial past events, character details, and world states over extended gameplay (~30 turns) using a Retrieval-Augmented Generation (RAG) approach to maintain narrative consistency.

* **🌐 Dynamic & Evolving World:** The game world is not static. The AI remembers player decisions and ensures the world and its characters evolve coherently over time.

* **🤖 Modular LLM Integration:** Built to work with modern Large Language Models. The system can be integrated with self-hosted models via `llama.cpp` or fast external APIs like Groq.

* **🛡️ Robust and Stable:** Engineered to sustain long gameplay sessions of 30+ turns without crashing or producing incoherent, context-breaking output.

#### 🏆 Bonus Features Implemented

* **👥 Character Memory:** NPCs remember their previous interactions with the players and evolve their dialogue and behavior accordingly.

---

### ⚙️ System Architecture

The system follows a modular design for clarity, efficiency, and scalability.

1.  **User Input:** The player's action is received.
2.  **Memory Processor:** The input is processed. Relevant short-term memories are updated, and the input is used to query the long-term vector database for relevant past events.
3.  **Context Augmentation (RAG):** The retrieved memories (both short and long-term) are combined with the current prompt to create a rich, context-aware prompt for the LLM.
4.  **LLM Generation:** The augmented prompt is sent to the LLM (e.g., Groq) to generate the next part of the story.
5.  **State Update:** The generated output updates the game state, and key events are summarized and stored in the persistent memory.
6.  **Narrative Output:** The final story segment is presented to the player.

---

### 📄 Technical Report

For a deep dive into the methodology, memory design, implementation challenges, and evaluation, please see our full technical report.

[View the file](https://drive.google.com/file/d/1hmGbxDA8xb_eX9uxctse224pD_Y1vCO9/view?usp=drive_link)

---

### 🚀 Getting Started

Follow these instructions to set up and run the project locally.

#### Prerequisites

* Python 3.8+
* Git

#### Installation & Setup

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/naveenthumati95/AI-Dungeon-Master-Persistent-Storytelling.git
    cd AI-Dungeon-Master-Persistent-Storytelling
    ```

2.  **Create a virtual environment:**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required dependencies:**
    ```sh
    pip install -r requirements.txt
    ```

4.  **Set up environment variables:**
    Create a `.env` file in the root directory and add your API keys (e.g., for Groq).
    ```
    GOOGLE_API_KEY="YOUR_API_KEY_HERE"
    TAVILY_API_KEY="YOUR_API_KEY_HERE"
    ```

#### Usage

Open and run the `ai_dungeon_master.ipynb` notebook using Jupyter Notebook or VS Code. Follow the instructions within the notebook to start your adventure!

---

### 📂 File Structure
```text
.
├── ai_dungeon_master.ipynb     # The main Jupyter Notebook with the full implementation.
├── Technical_Report.pdf        # The 2-4 page technical report.
├── requirements.txt            # A list of all Python dependencies.
├── .gitignore                  # To exclude unnecessary files from Git.
└── README.md                   # You are here!
```

---

### 👥 Team Members

* Naveen Chandra
* Aryan Chakravorty
