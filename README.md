<div align="center">

<img src="https://img.shields.io/badge/Python-3.9+-blue.svg" alt="Python">
<img src="https://img.shields.io/badge/FastAPI-0.109.0-green.svg" alt="FastAPI">
<img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License">
<img src="https://img.shields.io/badge/HuggingFace-Spaces-purple.svg" alt="HuggingFace">

# 🌍 Burme Dev Speak App

> AI-powered web application for Burmese text-to-speech and intelligent chat responses.

![Burme Dev Speak](https://huggingface.co/spaces/amkyawdev/BurmeAi-Space-Backend/embed)

</div>

---

## ✨ Features

- 💬 **AI Chat** - Intelligent conversational AI powered by Groq API (Mixtral-8x7B)
- 🔊 **Text-to-Speech** - Convert Burmese text to natural speech using Facebook MMS-TTS
- 📱 **Responsive Design** - Modern UI with Bootstrap, optimized for all devices
- 🎨 **Beautiful Theme** - Custom gold and black color scheme with smooth animations
- ⚡ **Fast & Lightweight** - Built with HTML, CSS, and JavaScript for optimal performance

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                        Frontend (Vercel)                     │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐  ┌─────────┐        │
│  │  Home   │  │  Chat   │  │  Speak  │  │  Docs   │  About  │
│  └─────────┘  └─────────┘  └─────────┘  └─────────┘        │
└─────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────┐
│                   Backend (HuggingFace Spaces)              │
│  ┌─────────────────────────────────────────────────────┐   │
│  │                   FastAPI Server                     │   │
│  │  ┌─────────────┐        ┌─────────────────────┐    │   │
│  │  │  /api/chat  │        │    /api/speak       │    │   │
│  │  │  Groq API   │        │  MMS-TTS (Myanmar)  │    │   │
│  │  └─────────────┘        └─────────────────────┘    │   │
│  └─────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
```

---

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- [Groq API Key](https://console.groq.com) (for chat)
- [HuggingFace Token](https://huggingface.co/settings/tokens) (for TTS)

### Local Development

1. **Clone the repository**
```bash
git clone https://github.com/amkyawdev/BurmeAi.git
cd BurmeAi
```

2. **Backend Setup**
```bash
cd BurmeAi-Space-Backend
pip install -r requirements.txt
export GROQ_API_KEY=your_groq_api_key
export HF_TOKEN=your_hf_token
uvicorn app:app --host 0.0.0.0 --port 7860
```

3. **Frontend (static files)**
Simply open `index.html` in your browser, or serve with any static file server:
```bash
python -m http.server 8000
```

---

## 🔌 API Reference

### Health Check

```http
GET /
```

**Response:**
```json
{
  "status": "ok",
  "message": "BurmeAi Space Backend is running"
}
```

### Chat Endpoint

```http
POST /api/chat
Content-Type: application/json

{
  "message": "Hello, how are you?"
}
```

**Response:**
```json
{
  "response": "I'm doing well, thank you for asking! How can I help you today?"
}
```

### Text-to-Speech Endpoint

```http
POST /api/speak
Content-Type: application/json

{
  "text": "မင်္ဂလာပါ"
}
```

**Response:**
```json
{
  "audio": "data:audio/wav;base64,..."
}
```

---

## 📂 Project Structure

```
BurmeAi/
├── index.html          # Landing page
├── chat.html           # AI Chat interface
├── speak.html          # Text-to-Speech interface
├── docs.html           # Documentation page
├── about.html          # About page
├── css/
│   └── style.css       # Custom styles
└── js/
    └── app.js          # JavaScript (if needed)

BurmeAi-Space-Backend/
├── app.py              # FastAPI application
├── requirements.txt    # Python dependencies
├── Dockerfile          # Docker configuration
└── README.md           # Backend documentation
```

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| HTML5 | Semantic markup |
| CSS3 | Styling & animations |
| JavaScript | Interactivity |
| Bootstrap 5 | Responsive framework |

### Backend
| Technology | Purpose |
|------------|---------|
| FastAPI | Web framework |
| Python 3.9+ | Runtime |
| Groq API | Chat AI (Mixtral-8x7B) |
| HuggingFace | Text-to-Speech |

---

## 📊 Usage Examples

### Burmese Text-to-Speech

```javascript
const response = await fetch('https://amkyawdev-burmeai-space-backend.hf.space/api/speak', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ text: 'မင်္ဂလာပါ' })
});
const { audio } = await response.json();
// audio is a base64-encoded WAV file
```

### AI Chat

```javascript
const response = await fetch('https://amkyawdev-burmeai-space-backend.hf.space/api/chat', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ message: 'What is Burmese?' })
});
const { response } = await response.json();
console.log(response);
```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Aung Myo Kyaw (Burme Dev)**
- GitHub: [@amkyawdev](https://github.com/amkyawdev)
- HuggingFace: [amkyawdev](https://huggingface.co/amkyawdev)

---

## 🙏 Acknowledgments

- [HuggingFace Spaces](https://huggingface.co/spaces) for hosting the backend
- [Groq](https://groq.com) for providing fast AI inference
- [Facebook AI](https://ai.facebook.com) for MMS-TTS model
- [Bootstrap](https://getbootstrap.com) for the UI framework

---

<div align="center">

⭐ Star this repo if you find it helpful!

Made with ❤️ by [Burme Dev](https://github.com/amkyawdev)

</div>
