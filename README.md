# 🧠 My Voice Assistant (Offline, Private)

A fully offline voice assistant using:

- 🎤 [Whisper.cpp](https://github.com/ggerganov/whisper.cpp) — Speech to Text  
- 🧠 [LLaMA.cpp](https://github.com/ggerganov/llama.cpp) — Language Model (e.g. DeepSeek)  
- 💾 Optional [mem0](https://github.com/mem0ai/mem0) — Persistent memory  

---

## 🔧 Requirements

- macOS (M1/M2 recommended)
- Python 3.10+
- Whisper model (`ggml-base.en.bin`)
- LLaMA model (`deepseek-llm-7b-chat.Q4_K_M.gguf`)

---

## 🚀 Run

```bash
python3 assistant.py
```

---

## 🗣️ What It Can Do

- Listen to your mic
- Transcribe locally (no cloud)
- Respond using LLM
- Can remember things (optional)

---

## 📸 Screenshot

![demo](./examples/demo.png)

---

## 🧠 Coming Soon

- Text-to-Speech replies
- Electron GUI
