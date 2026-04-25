# �BURME AI - Burmese AI Assistant

<p align="center">
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge" alt="Python">
  <img src="https://img.shields.io/badge/FastAPI-0.104+-green?style=for-the-badge" alt="FastAPI">
  <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge" alt="License">
</p>

<p align="center">
  <a href="https://burme-ai.vercel.app">🌐 Live Demo</a>
  •
  <a href="https://huggingface.co/spaces/amkyawdev/BurmeAi-Space-Backend">🤗 Backend API</a>
  •
  <a href="https://github.com/amkyawdev/BurmeAi">📂 GitHub</a>
</p>

---

## 📖 Overview

**BurmeAi** is an AI-powered web application for Burmese (Myanmar) language support featuring:

- 💬 **AI Chat** - Chat with AI assistant that understands Burmese
- 🔊 **Text-to-Speech** - Convert Burmese text to natural speech
- 📱 **Responsive Design** - Works on desktop and mobile
- 🌙 **Dark Theme** - Beautiful dark UI with gold accents

---

## 🚀 Features

### Chat Feature
- Real-time AI responses using GROQ's LLaMA models
- Support for both Burmese and English
- Responsive chat interface
- Message history within session

### Text-to-Speech Feature
- Natural Burmese voice synthesis
- Multiple voice options (Myanmar, US, German)
- Adjustable speech speed (0.5x - 2.0x)
- Audio download support
- History of generated speeches

### Additional Features
- Smooth animations and particles
- Collapsible sidebar navigation
- Professional documentation page
- Developer contact information

---

## 🛠️ Tech Stack

### Frontend
- **HTML5 / CSS3 / JavaScript** - Core web technologies
- **Bootstrap Icons** - Icon library
- **Vercel** - Frontend hosting

### Backend
- **Python 3.11+** - Programming language
- **FastAPI** - Web framework
- **GROQ API** - LLM (LLaMA 3.1 8B Instant)
- **Edge TTS** - Text-to-Speech (Microsoft)
- **HuggingFace Spaces** - Backend hosting

---

## 📁 Project Structure

```
BurmeAi/
├── README.md                 # Project documentation
├── BurmeAi/                  # Frontend (Vercel)
│   ├── index.html            # Homepage
│   ├── chat.html             # AI Chat page
│   ├── speak.html            # Text-to-Speech page
│   ├── docs.html             # Documentation page
│   ├── about.html            # About/Contact page
│   ├── css/
│   │   └── style.css         # Custom styles
│   ├── js/                   # JavaScript files
│   └── vercel.json          # Vercel config
│
└── BurmeAi-Space-Backend/    # Backend (HuggingFace)
    ├── app.py                # FastAPI application
    ├── requirements.txt      # Python dependencies
    ├── Dockerfile           # Docker config
    └── README.md            # Backend docs
```

---

## 🔧 API Endpoints

### Chat API
```bash
POST /api/chat
Content-Type: application/json

{
  "message": "မင်္ဂလာပါ"
}

# Response
{
  "response": "မင်္ဂလာပါ! ကျွန်တော်က သင့်ကို ကူညီနိုင်ပါသည်။"
}
```

### Speak API
```bash
POST /api/speak
Content-Type: application/json

{
  "text": "မြန်မာစာ"
}

# Response
{
  "audio": "data:audio/mp3;base64,..."
}
```

---

## 🧪 Testing

### Test Chat API
```bash
curl -X POST "https://amkyawdev-burmeai-space-backend.hf.space/api/chat" \
  -H "Content-Type: application/json" \
  -d '{"message": "Hello"}'
```

### Test Speak API
```bash
curl -X POST "https://amkyawdev-burmeai-space-backend.hf.space/api/speak" \
  -H "Content-Type: application/json" \
  -d '{"text": "Hello"}'
```

---

## 👨‍💻 Developer

**Aung Myo Kyaw**  
Full Stack Developer

- 📱 Phone: 0967740154
- 📧 Email: amk.kyaw92@gmail.com
- 🐙 GitHub: [@amkyawdev](https://github.com/amkyawdev)
- 🤗 HuggingFace: [@amkyawdev](https://huggingface.co/amkyawdev)
- 🎵 TikTok: [@amkyaw.dev](https://tiktok.com/@amkyaw.dev)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **GROQ** - For providing free LLM API
- **Microsoft** - For Edge TTS technology
- **HuggingFace** - For hosting infrastructure
- **Vercel** - For frontend hosting

---

<p align="center">
  Made with ❤️ by <strong>Aung Myo Kyaw</strong>
</p>
