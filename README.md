# 🧠 LangChain Basic Chatbot using LangGraph and Groq API

This repository contains a **basic chatbot** built using **LangChain** and **LangGraph** with the **Groq API** as the backend LLM.  
The project demonstrates how modern LangChain workflows can be designed as **graphs** that manage conversational flow, memory, and logic in a structured, modular way.

---

## 🚀 Overview

This chatbot showcases:
- How to integrate **Groq-hosted LLMs** with LangChain.
- The use of **LangGraph** to design conversational pipelines as graphs.
- How to use **`InSaverMemory`** to persist conversation state between turns.
- The fundamentals of **message passing** and **graph-based agent control**.

Even though this is a simple chatbot, it covers the **core ideas** behind how advanced conversational agents can be built using LangGraph and LangChain — the same frameworks used for modern production-grade AI assistants.

---

## 🧩 Key Concepts Explained

### 🕸️ 1. LangGraph

**LangGraph** extends LangChain by introducing a **graph-based architecture** for defining workflows.  
Instead of chaining steps linearly, LangGraph allows you to create **nodes** and **edges** representing:
- Message flow,
- Model responses,
- Memory state updates, and
- Conditional transitions.

This makes your chatbot’s logic **visual, modular, and easy to extend** — ideal for complex reasoning or multi-turn conversations.

---

### 🧠 2. InSaverMemory

`InSaverMemory` is a **memory store** provided by LangGraph.  
It holds previous user–AI messages directly in memory while you interact with the chatbot.

Key features:
- Stores chat history **in-memory** (not persistent on disk).
- Allows the model to recall past interactions during a single session.
- Integrates directly into the LangGraph node structure.

In simpler terms, this memory lets your chatbot “remember” the conversation context during one run.

---

### ⚙️ 3. LLM (Large Language Model)

An **LLM** is the core intelligence of your chatbot.  
In this project, the LLM is powered by **Groq’s hosted models**, which are known for:
- Extremely low-latency inference,
- Stable API performance,
- Compatibility with LangChain and LangGraph.

These models handle the natural language understanding and response generation for your chatbot.

---

### 🔗 4. Graph Nodes & State Flow

In LangGraph, the chatbot is represented as a **graph of nodes**:
- Each **node** performs a specific operation (e.g., process input, call model, update memory).
- **Edges** define how messages move between nodes.
- The **state** (memory, messages, variables) is passed and updated dynamically.

This design mimics how real-world AI systems orchestrate logic — making it ideal for multi-agent or multi-step reasoning workflows.

---

## 🧰 Project Structure

Inside the notebook:
- The Groq model is initialized.
- A `LangGraph` workflow is defined with memory integration.
- The chatbot runs interactively using state updates.
- Responses are generated with context persistence through `InSaverMemory`.

---

## 🔑 Getting Groq API Keys

You’ll need a **Groq API key** to use the LLM.

1. Go to [https://console.groq.com/keys](https://console.groq.com/keys)  
2. Sign in or create a free account.  
3. Generate a new API key.  
4. Copy the key and store it securely.

You can set it as an environment variable:

```bash
export GROQ_API_KEY="your_api_key_here"
