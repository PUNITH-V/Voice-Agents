# Voice Agents

A real-time AI voice agent application built with LiveKit, featuring ultra-fast text-to-speech using Murf Falcon TTS, and powered by Google Gemini for intelligent conversations.

## 🎯 Features

- **Real-time Voice Interaction** - Natural conversations with AI agents
- **Ultra-Fast TTS** - Powered by Murf Falcon for lightning-fast speech synthesis
- **Smart AI** - Google Gemini integration for intelligent responses
- **Modern UI** - Beautiful React/Next.js frontend with dark/light themes
- **Video Support** - Camera streaming and screen sharing capabilities
- **Audio Visualization** - Real-time audio level monitoring
- **Production Ready** - Complete with Docker support and testing framework

## 🏗️ Architecture

This is a monorepo containing:

```
Voice-Agents/
├── backend/          # LiveKit Agents backend (Python)
├── frontend/         # Next.js frontend (React)
├── challenges/       # Daily challenge tasks
└── start_app.sh      # Quick start script
```

## 🚀 Quick Start

### Prerequisites

- **Python 3.9+** with [uv](https://docs.astral.sh/uv/) package manager
- **Node.js 18+** with pnpm
- **LiveKit Server** - [Download here](https://github.com/livekit/livekit/releases)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/PUNITH-V/Voice-Agents.git
cd Voice-Agents
```

2. **Backend Setup**
```bash
cd backend

# Install dependencies
uv sync

# Configure environment
cp .env.example .env
# Edit .env with your API keys:
# - LIVEKIT_URL=http://127.0.0.1:7880
# - LIVEKIT_API_KEY=devkey
# - LIVEKIT_API_SECRET=secret
# - GOOGLE_API_KEY=your_gemini_key
# - MURF_API_KEY=your_murf_key
# - DEEPGRAM_API_KEY=your_deepgram_key
```

3. **Frontend Setup**
```bash
cd frontend

# Install dependencies
pnpm install

# Configure environment
cp .env.example .env.local
# Edit .env.local with the same LiveKit credentials
```

4. **Download LiveKit Server**

For Windows:
```bash
# Download from: https://github.com/livekit/livekit/releases/latest
# Get: livekit-server-windows-amd64.exe
```

For macOS:
```bash
brew install livekit
```

For Linux:
```bash
curl -sSL https://get.livekit.io | bash
```

### Running the Application

**Option 1: All-in-one script (Linux/macOS)**
```bash
chmod +x start_app.sh
./start_app.sh
```

**Option 2: Manual start (Windows/All platforms)**

Terminal 1 - LiveKit Server:
```bash
livekit-server --dev
# or on Windows:
# livekit-server.exe --dev
```

Terminal 2 - Backend:
```bash
cd backend
uv run python src/agent.py dev
```

Terminal 3 - Frontend:
```bash
cd frontend
pnpm dev
```

Open **http://localhost:3000** in your browser!

## 🔑 API Keys

You'll need API keys from:

- **Google Gemini** - [Get API Key](https://makersuite.google.com/app/apikey)
- **Murf Falcon** - [Sign up](https://murf.ai/api)
- **Deepgram** - [Get API Key](https://console.deepgram.com/)

For local development, LiveKit uses default credentials:
- API Key: `devkey`
- API Secret: `secret`

## 📚 Documentation

- [Backend Documentation](./backend/README.md)
- [Frontend Documentation](./frontend/README.md)
- [LiveKit Agents Docs](https://docs.livekit.io/agents)
- [Murf Falcon API](https://murf.ai/api/docs/text-to-speech/streaming)

## 🧪 Testing

```bash
cd backend
uv run pytest
```

## 🛠️ Tech Stack

**Backend:**
- LiveKit Agents Framework
- Python 3.11+
- Murf Falcon TTS
- Google Gemini LLM
- Deepgram STT

**Frontend:**
- Next.js 15
- React 19
- LiveKit Components
- Tailwind CSS
- TypeScript

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## 👤 Author

**Punith V**
- GitHub: [@PUNITH-V](https://github.com/PUNITH-V)
- Repository: [Voice-Agents](https://github.com/PUNITH-V/Voice-Agents)

## 🙏 Acknowledgments

Built with:
- [LiveKit](https://livekit.io/) - Real-time communication platform
- [Murf.ai](https://murf.ai/) - Ultra-fast TTS API
- [Google Gemini](https://deepmind.google/technologies/gemini/) - AI language model

---

⭐ Star this repo if you find it helpful!
