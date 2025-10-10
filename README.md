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

