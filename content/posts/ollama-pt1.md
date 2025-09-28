---
title: 'Ollama Guide For Nerds.'
description: 'Run a AI locally.'
pubDate: 2025-08-27
author: 'Dihan Ramanayaka'
tags: [AI]
---


# How to Install Ollama on Your System

[Ollama](https://ollama.ai) is a lightweight framework that lets you run large language models (LLMs) locally on your computer. It supports models like **Llama 2**, **Mistral**, **Gemma**, and more — all without needing a cloud API.

This guide will walk you through installing Ollama on **macOS**, **Linux**, and **Windows**.

---

## 🔧 Prerequisites

* A modern computer with **at least 8GB RAM** (16GB recommended).
* Operating system: **macOS 11+**, **Linux (Ubuntu/Debian)**, or **Windows 10/11 (with WSL2)**.
* An internet connection (to download Ollama and models).

---

## 🖥️ macOS Installation

1. Open **Terminal**.
2. Install Ollama with Homebrew (recommended):

   ```bash
   brew install ollama/tap/ollama
   ```
s. Start the Ollama service:

   ```bash
   ollama serve
   ```
4. Run your first model (example with Llama 2):

   ```bash
   ollama run llama2
   ```

👉 Ollama will automatically download the model on first run.

---

## 🐧 Linux Installation (Recommened)

Currently, Ollama provides official builds for **Debian/Ubuntu**.

1. Download and install the `.deb` package:

   ```bash
   curl -fsSL https://ollama.ai/install.sh | sh
   ```
2. Start the Ollama service:

   ```bash
   ollama serve
   ```
s. Run a model:

   ```bash
   ollama run mistral
   ```

---

## 🪟 Windows Installation

Ollama doesn’t yet have a **native Windows build**, but you can run it through **WSL2 (Windows Subsystem for Linux)**:

1. Install [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install) with Ubuntu.
2. Open the Ubuntu terminal in Windows.
3. Run the Linux installation steps:

   ```bash
   curl -fsSL https://ollama.ai/install.sh | sh
   ```
4. Once installed, start Ollama inside WSL:

   ```bash
   ollama serve
   ```
5. Run a model:

   ```bash
   ollama run llama2
   ```

---

## ✅ Verifying the Installation

After installing, check if Ollama is working by running:

```bash
ollama list
```

This will show all available models on your system.

---

## 🎯 Next Steps

* Explore different models:

  ```bash
  ollama run mistral
  ollama run gemma
  ```
* Create your own model configuration with `Modelfile`.
* Integrate Ollama into apps using its [REST API](https://github.com/ollama/ollama/blob/main/docs/api.md).

---

## 🚀 Conclusion

With Ollama installed, you now have the power to run advanced AI models **locally**, without depending on cloud providers. Whether you’re a developer, researcher, or just experimenting, Ollama makes local AI accessible and easy.

👉 Visit the [Ollama docs](https://ollama.ai) for more details.
\`\`\`
