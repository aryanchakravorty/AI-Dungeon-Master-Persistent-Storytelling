# AI Dungeon Master for Persistent Storytelling

![Language](https://img.shields.io/badge/Language-Python-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-success)

An intelligent AI Dungeon Master developed for the Inter IIT Tech Meet 14.0 AI/ML Bootcamp, focused on solving the challenge of long-term narrative coherence in LLM-driven storytelling.  
The system employs a dual-memory architecture to track player choices, world state, and character evolution, enabling immersive and consistent role-playing experiences across extended gameplay sessions.

---

## Live Demo

A short demonstration showcasing the system’s short-term and long-term memory recall capabilities:

https://drive.google.com/file/d/1J6FM3J5vCr2LwdM3pcEdNn-H7sn_IwbU/view?usp=sharing

---

## Core Features

### Dual-Memory Architecture
- Working Memory (Short-Term): Maintains recent scene details and player actions over the last few turns to preserve immediate conversational context.
- Persistent Memory (Long-Term): Stores and retrieves critical past events, character information, and world states using a Retrieval-Augmented Generation (RAG) pipeline, ensuring narrative continuity over 30+ turns.

### Dynamic World Evolution
- Player decisions permanently influence the game world.
- Characters and environments evolve coherently based on prior interactions and events.

### Modular LLM Integration
- Designed to support modern LLM backends.
- Compatible with self-hosted models via llama.cpp and external inference APIs such as Groq.

### Stability and Robustness
- Engineered for long gameplay sessions without crashes or context degradation.
- Prevents incoherent or contradictory narrative outputs during extended interactions.

### Character Memory
- NPCs remember previous encounters with players.
- Dialogue and behavior dynamically adapt based on shared history.

---

## System Architecture

1. User Input: Player actions are received.
2. Memory Processing: Short-term memory is updated and long-term memory is queried for relevant historical events.
3. Context Augmentation (RAG): Retrieved memories are combined with the current prompt.
4. LLM Generation: The augmented context is passed to the LLM to generate the next narrative segment.
5. State Update: Key events are summarized and stored in persistent memory.
6. Narrative Output: The generated story is presented to the player.

---

## Technical Report

For detailed methodology, memory design, system architecture, and evaluation results, refer to the full technical report:

[https://drive.google.com/file/d/1hmGbxDA8xb_eX9uxctse224pD_Y1vCO9/view?usp=drive_link](https://drive.google.com/file/d/1TpbStUP17lMWx97vcJoxxAeOvSE83nD5/view?usp=sharing)

---

## Getting Started

### Prerequisites
- Python 3.8+
- Git

### Installation

Clone the repository:

    git clone https://github.com/naveenthumati95/AI-Dungeon-Master-Persistent-Storytelling.git
    cd AI-Dungeon-Master-Persistent-Storytelling

Create a virtual environment:

    python -m venv venv
    source venv/bin/activate
    (Windows: venv\Scripts\activate)

Install dependencies:

    pip install -r requirements.txt

---

## Environment Setup

Create a `.env` file in the project root and add your API keys:

    GOOGLE_API_KEY="YOUR_API_KEY_HERE"
    TAVILY_API_KEY="YOUR_API_KEY_HERE"

---

## Usage

Open and run the `ai_dungeon_master.ipynb` notebook using Jupyter Notebook or VS Code.  
Follow the instructions inside the notebook to start your adventure.

---

## Project Structure

    .
    ├── ai_dungeon_master.ipynb     # Main notebook containing the full implementation
    ├── Technical_Report.pdf        # Detailed technical documentation
    ├── requirements.txt            # Python dependencies
    ├── .gitignore                  # Git ignore rules
    └── README.md                   # Project documentation

---

## Team Members

- Naveen Chandra  
- Aryan Chakravorty
