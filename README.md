# AI Emotion-to-Art Team2  
Transform Your Emotions into Stunning AI-Generated Artworks

## 🔹 Table of Contents
- [Introduction](#introduction)
- [How-it-works](#how-it-works)
- [README-&-Installation](#readme--installation)
- [Debug-/-Troubleshooting](#debug--troubleshooting)
- [Team-Members](#team-members)

## Introduction  
AI Emotion-to-Art Team2 converts user emotions (**text**, **voice**, or **image**) into symbolic visual art using AI technologies such as **Whisper**, **Ollama (Gemma3:4b)**, and **Replicate**.

## How It Works
**Step 1 – Provide Emotion**  
Input a sentence, record your voice or upload an image.  

**Step 2 – Emotion Recognition**  
A locally running **Gemma3:4b** model through **Ollama** classifies your emotion.  

**Step 3 – Prompt Generation**  
The system builds a symbolic prompt (under 20 words) for visualisation.  

**Step 4 – Art Generation**  
The prompt is sent to **Replicate (Imagen backend)** and a square artwork is generated.


## README & Installation
**Requirements**
- Python 3.13  
- Ollama installed with **Gemma3:4b** model  
- Replicate API token

```bash
# Install Ollama → https://ollama.com/
# Run:   ollama run gemma3:4b

python -m venv env
source env/bin/activate   # (Windows → .\env\Scripts\activate)

pip install openai-whisper replicate ollama gradio

# export REPLICATE_API_TOKEN="your_token_here"
# or  setx REPLICATE_API_TOKEN "your_token_here"

# Open Gradio UI and open the provided URL
```

## Debug / Troubleshooting
```text
# Ollama / Gemma3:4b Errors
“Model not found” → You haven't installed Gemma3:4b
Fix: ollama run gemma3:4b

“Cannot connect to Ollama” → Ollama service not running
Fix: Open Ollama desktop app or run ollama serve

# Replicate API Errors
HTTP 401 Unauthorized → Invalid/expired token
Fix: Generate new token at https://replicate.com/account

Model failed to load → Imagen temporarily unavailable
Fix: wait or switch to another model
```

## Team Members
- Mahyar Alizadeh  
- Sogol Tarnabi  
- Arad Chizari  
- Mohammad Mahdi Omidvar
