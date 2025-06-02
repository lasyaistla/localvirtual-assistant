# localvirtual-assistant
Local Voice Assistant (Offline, Private, and Extendable)

This project is a fully local, privacy-first voice assistant powered by Whisper.cpp for speech-to-text, Llama.cpp for LLM reasoning, and optionally mem0 for persistent memory. It runs completely offline with no cloud dependencies.

Features

Voice input via microphone using Whisper.cpp
Local language model inference using Llama.cpp
Optional memory integration with mem0
Optional graphical interface using Gradio
Entirely offline and privacy-respecting
Project Structure

my-voice-assistant/
├── assistant.py                 # Main Python script
├── mic.wav                     # Auto-generated audio file
├── whisper.cpp/                # Cloned & compiled Whisper.cpp
│   └── models/                 # Whisper model (e.g. ggml-base.en.bin)
├── llama.cpp/                  # Cloned & compiled Llama.cpp
│   └── models/                 # LLM model (e.g. deepseek-llm-7b-chat.Q4_K_M.gguf)
├── build/                      # Compiled binaries from llama.cpp
├── mem0/                       # Optional memory module
└── README.md                   # This file
Setup Instructions

1. Clone the Repositories
git clone https://github.com/ggerganov/whisper.cpp.git
git clone https://github.com/ggerganov/llama.cpp.git
git clone https://github.com/mem0ai/mem0.git  # Optional
2. Download Models
Whisper model: ggml-base.en.bin from Hugging Face
LLM model: Example deepseek-llm-7b-chat.Q4_K_M.gguf from Hugging Face
Place them in the following paths:

whisper.cpp/models/ggml-base.en.bin
llama.cpp/models/deepseek-llm-7b-chat.Q4_K_M.gguf
3. Build the C++ Tools
Build Whisper

cd whisper.cpp
cmake -B build
cmake --build build --config Release
Build Llama

cd llama.cpp
cmake -B build -DLLAMA_METAL=on -DCMAKE_OSX_ARCHITECTURES=arm64
cmake --build build --config Release
4. Install Python Dependencies
pip install -r requirements.txt
Example requirements.txt:

gradio
sounddevice
numpy
5. Run the Assistant
Run from terminal:

python assistant.py
Or launch with Gradio interface:

import gradio as gr
gr.Interface(fn=run_assistant, inputs=[], outputs="text").launch()
Extensions and Ideas

Add text-to-speech output
Stream microphone input instead of recording
Enhance with persistent memory using mem0
Build a GUI using Electron or web-based tools
Deploy on a Raspberry Pi or other edge device
License

MIT License. You are free to use, modify, and distribute this project.
