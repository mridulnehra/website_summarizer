# AI Website Summarizer 🌐🤖

A powerful, interactive Python-based website summarization tool that extracts cleaner web-page content and feeds it into Large Language Models (LLMs) to generate structured Markdown summaries.

This repository showcases dual implementations using both **Cloud-based LLM APIs (Google Gemini)** and **Privacy-First Local Models (Ollama)**.

---

## ✨ Features

### 🔹 DOM Scrubbing Engine
Custom-built parsing utilizing `BeautifulSoup4` that identifies and completely strips non-essential elements (like dynamic `<script>`, `<style>`, `<img>`, and user `<input>` elements) before payload generation.

### 🔹 Dual Inference Platforms

#### ☁️ Cloud-based Processing
Leverages the state-of-the-art Google GenAI SDK (`gemini-2.5-flash`) for lightning-fast, high-quality, and cost-effective cloud summarization.

#### 🖥️ Local & Offline Processing
Leverages Ollama running `llama3.2` locally for absolute privacy, complete data protection, and zero token-cost iterations.

### 🔹 Engineered Context-Aware Prompting
Structured dual-role prompts (System & User) that cleanly partition primary site descriptions from dynamic content, such as recent news, announcements, or blog posts.

---

# 📂 Project Structure

The project is split into two straightforward Jupyter notebooks, allowing you to run and compare both execution frameworks:

---

## 1. `part-2 using gemini api.ipynb`

Demonstrates cloud-based summarization using the official Google GenAI client library.

### Includes:
- Secure API key initialization via `.env` configuration files
- Real-world integration testing on enterprise web applications:
  - Anthropic
  - CNN
  - Canva
  - Personal professional websites

---

## 2. `website summarizer using ollama api.ipynb`

Demonstrates offline local LLM interaction.

### Includes:
- Raw interaction with Ollama local chat endpoints:
  ```python
  http://localhost:11434/api/chat
