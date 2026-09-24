# 🏥 Multimodal Medical Chatbot

<div align="center">
  <img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Whisper-000000?style=for-the-badge&logo=openai&logoColor=white" alt="Whisper" />
  <img src="https://img.shields.io/badge/Groq-000000?style=for-the-badge" alt="Groq" />
  <img src="https://img.shields.io/badge/Meta_Llama-0467DF?style=for-the-badge&logo=meta&logoColor=white" alt="Meta Llama" />
</div>

<br/>

**Medical Chatbot** is an advanced, multimodal AI application built to assist users with medical queries through text, voice, and image inputs. Built on a blazing-fast **FastAPI** backend, it utilizes **OpenAI's Whisper** for transcription, and the **Groq API** running **Meta's Llama Vision models** to perform intelligent medical analysis and image breakdown in real-time.

---

## ✨ Features

- **🎙️ Voice Interaction & Translation**: Supports recording audio in multiple languages (e.g., Tamil). Transcribes using the robust `Whisper` base model and seamlessly translates non-English inputs into English before passing them to the AI.
- **👁️ Vision & Image Analysis**: Allows users to upload images alongside their queries. Encodes images to Base64 and passes them directly to advanced Llama Vision models (`llama-4-scout` and `llama-4-maverick`) for visual medical analysis.
- **⚡ Ultra-Fast Inference**: Uses the Groq API for highly optimized, low-latency LLM inference, returning instant answers from complex multi-modal Llama models.
- **🚀 Asynchronous Backend**: Built entirely with FastAPI, utilizing non-blocking async routes and Python background tasks to ensure high scalability and performance.

## 🛠️ Technology Stack

| Technology | Purpose |
| ---------- | ------- |
| **FastAPI** | Core asynchronous web framework |
| **OpenAI Whisper** | Accurate local voice transcription |
| **Googletrans** | Text translation to unify inputs to English |
| **Groq API** | Low-latency inference platform |
| **Meta Llama Vision** | The intelligence and image processing backend |
| **FFmpeg** | Audio format conversion to `.wav` for Whisper |

## 🚀 Getting Started

### Prerequisites
- Python 3.10+
- FFmpeg installed on your system (Required for Whisper audio conversion)
- A [Groq API Key](https://console.groq.com/keys)

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/Nishanthtamil/medical-chatbot.git
cd medical-chatbot
```

2. **Create a virtual environment & install dependencies:**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install fastapi uvicorn requests pillow python-dotenv openai-whisper googletrans==4.0.0-rc1 python-multipart jinja2
```
*Note: Make sure `ffmpeg` is installed and in your system PATH.*

3. **Environment Setup:**
Create a `.env` file in the root directory:
```env
GROQ_API_KEY=your_groq_api_key_here
```

4. **Start the Server:**
```bash
python app.py
```
Or run via Uvicorn:
```bash
uvicorn app:app --host 0.0.0.0 --port 8000
```

The application will be available at [http://localhost:8000](http://localhost:8000).

## 🏗️ Project Structure

```text
medical-chatbot/
├── app.py             # FastAPI backend with Whisper, Translation, and Groq routes
├── main.py            # (Alternative script / Entry point)
├── templates/         # Jinja2 HTML templates for the frontend UI
├── .env               # Secrets and API keys
└── README.md          # Project documentation
```

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.
