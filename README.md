# My Voice Assistant (Offline, Private)

A fully offline voice assistant using:

- 🎤 [Whisper.cpp](https://github.com/ggerganov/whisper.cpp) — Speech to Text  
-  [LLaMA.cpp](https://github.com/ggerganov/llama.cpp) — Language Model (e.g. DeepSeek)  
-  Optional [mem0](https://github.com/mem0ai/mem0) — Persistent memory  

---

## 🔧 Requirements

- macOS (M1/M2 recommended)
- Python 3.10+
- Whisper model (`ggml-base.en.bin`)
- LLaMA model (`deepseek-llm-7b-chat.Q4_K_M.gguf`)

---

## Run

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
<img width="1470" alt="Screenshot 2025-06-02 at 12 29 14 AM" src="https://github.com/user-attachments/assets/54a8b865-0d5e-4f7d-b111-69226123f8be" />
<img width="800" alt="Screenshot 2025-06-02 at 12 40 07 AM" src="https://github.com/user-attachments/assets/a117e1d1-8a4d-421c-a0ed-0f710b9e1d8a" />

![demo](./examples/demo.png)

---

## Coming Soon

- Text-to-Speech replies
- Electron GUI
