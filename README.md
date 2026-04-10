# ChatBot: Conversational AI with Persistent SQL Memory

> A Chatbot system that combines configurable training pipelines with SQL-backed conversation memory for repeatable, domain-adaptable dialogue workflows.

## Overview

This project implements an end-to-end conversational AI workflow using ChatterBot, designed for practical assistant use cases where response quality and persistence matter more than one-off notebook demos.

It focuses on:
- Training flexibility (custom conversation lists and corpus-driven training)
- Stateful conversation storage via SQL adapter
- Configurable inference behavior through logic adapter composition

Real-world use cases:
- FAQ assistants for internal teams
- Lightweight customer-support copilots for SMB products
- Prototype conversational interfaces before moving to larger LLM stacks

## Architecture

The system follows a modular inference pipeline:

`User Input -> Text Processing -> Logic Adapters -> Response Selection -> SQL Storage -> Bot Response`

Core components:
- **Input Layer**: Interactive CLI loop captures user prompts and session flow.
- **Training Layer**: Supports both `ListTrainer` (domain-specific seed dialogs) and `ChatterBotCorpusTrainer` (broad language corpus).
- **AI Layer**: Uses `BestMatch` and `MathematicalEvaluation` logic adapters for intent matching and deterministic math handling.
- **Persistence Layer**: SQL-backed statement store retains dialogue state and enables incremental learning workflows.
- **Output Layer**: Returns ranked responses in an interactive conversational loop.

Design decisions:
- **Dual training strategy** to balance domain precision and general coverage.
- **Adapter-based inference** for controlled behavior instead of monolithic black-box generation.
- **Persistent storage** to keep conversation continuity across runs.

### Architecture Diagram

![ChatBot Architecture Flowchart](./assets/ChatBot%20Architecture%20Flowchart.png)

Figure: End-to-end chatbot flow showing user input processing, logic adapter routing, training pathways, response generation, and SQL-backed persistence.

## Features

- Configurable chatbot instance with pluggable logic adapters
- Two training modes for fast experimentation and broader language coverage
- SQL persistence for reusable conversation memory
- Interactive runtime loop for rapid behavior validation
- Custom storage adapter implementation to improve SQL backend reliability

## Technical Highlights

- Built around an explicit system pipeline rather than a single script execution path.
- Includes a custom SQL storage adapter (`sql_storage.py`) with SQLite runtime tuning (`PRAGMA journal_mode=WAL`, `synchronous=NORMAL`) for safer concurrent access and improved write behavior.
- Uses model abstraction (`Statement`, `Tag`, session lifecycle methods) to keep data operations structured and maintainable.
- Separates training concerns (data preparation) from inference concerns (logic adapter response generation), which supports cleaner production migration.

## Tech Stack

- Python
- ChatterBot
- NLTK
- spaCy
- SQLAlchemy
- SQLite
- Jupyter Notebook (experimentation and iteration)

## Getting Started

### 1) Clone Repository

```bash
git clone https://github.com/kershrita/ChatBot.git
cd ChatBot
```

### 2) Install Dependencies

```bash
pip install chatterbot nltk spacy
pip install --upgrade sqlalchemy
```

### 3) Apply Custom SQL Storage Adapter

This repository includes a custom storage adapter implementation in `sql_storage.py`.

Copy it to your local ChatterBot storage path (example for Anaconda on Windows):

```text
[python-install-path]\Lib\site-packages\chatterbot\storage\sql_storage.py
```

### 4) Run the Notebook Workflow

Open `chatbot.ipynb` and execute:
- Custom list training flow for domain-specific bootstrapping
- Corpus training flow for broader conversational coverage
- Interactive chat loop (`exit` to stop)

## Results

Current project outcomes:
- Validated end-to-end chatbot pipeline from training to live response loop
- Demonstrated persistent conversational storage using SQL backend
- Verified mixed reasoning behavior through logic adapters (best-match + mathematical evaluation)

Example interaction pattern:

```text
User: Hello
Bot: Hi there!
```

> Note: Quantitative evaluation metrics (e.g., response relevance score, fallback rate, latency distribution) are not yet benchmarked in this repository and are a recommended next step for production hardening.

## License

Released under the MIT License. See [LICENSE](LICENSE).