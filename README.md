# Simple Stock based Chat:  (OpenAI, DeepSeek, Gemini, GitHub)

## 🚀 Quick Start (Docker)

```bash
# Set up environment variables
cp .env.example .env
# Edit .env with your API keys (OPENAI_API_KEY or DEEPSEEK_API_KEY or GEMINI_API_KEY or GITHUB_TOKEN required)

docker-compose up --build
```
And the app will be running on http://localhost:5173.

## ✨ Key Components

- 🧠 **DSPy Integration** - Built-in financial analysis pipelines
- 📈 **Trading Signals** - Real-time visualization of technical indicators
- 📊 **Market Data Processing** - Extensible data ingestion framework
- 🔍 **Research Cache** - SQLite-based analysis result storage
- 🌐 **Data Saving** - Users can save their analysis through a specific URL endpoint
- 🧠 **TA-Lib Integration** - Professional technical analysis calculations

## 🛠️ Local Development Setup

First, install TA-Lib to your computer according to [TA-Lib Python Install Guide](https://ta-lib.github.io/ta-lib-python/install.html).

### Backend Service
```bash
cd stockchat-backend
python -m venv venv
source venv/bin/activate  # Unix/MacOS
# .\venv\Scripts\activate  # Windows

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys (either one required):
# OPENAI_API_KEY=your_openai_api_key
# DEEPSEEK_API_KEY=your_deepseek_api_key
# GEMINI_API_KEY=your_gemini_api_key
# GITHUB_TOKEN=your_github_token

pip install -r requirements.txt
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

### Frontend Application
```bash
cd stockchat-frontend
npm install
npm run dev
```
And the app will be running on http://localhost:5173.

## 🧩 System Architecture

[![System Architecture](https://mermaid.ink/img/pako:eNqdVMtu2zAQ_BWCRoAEsAG3ARxHhwJ6GQ3QAG6cXlr1wEgri7BMuuQqjuH437N6WiniQ6yTuDs73J0hueexToA7PM31Ns6EQfYYRIrRd3HB7oVUzNfrjVag0NbxXxbMZcRT4aRiVNCiikT8qk7PjFYIKukgCdgV6g3zM4HsjnImFTF0eE_Eqz6cuJ6Jswkzd37XQR90QdX7FmnKJXOVyHdW2iYb8UMNDhbzXUf6ZMpJyhBbEL_s7X8vzAqwQ1YajHKpoMmwQKB414Yv4gyO41H6SVhgD2BBmDir8x068P5c_odc_PwhqfOgWV_9jVQnua-VghilVj252Wj0rRP2vcxl6rXtRRijtyMjlxmy74-Pc-rpXwGWnOOvraLvVK-IG-F6Ep8knRsdg7VsKzErOUtFj3KfLJsBki7l_Cw1el1W1uL2LfigOocUaQYsjKqrUX9i1wVqA8yALXK0TKqytPbmaOOpTWnQZ5lAf9dT-n24dyANucjcuJSr6tnrmbzAHZ2wZSUji8lIIyyWAYQXpECuTeO-JSQczU5lnjuD23EY3o6HFo1egTO4vr5u_kdbmWDmfN28DCsSZzCuvj5X23lNNb3xw9A7k6pSv-aZzbyJ_-VMnubQtUzu-MY9k6n2tCYKAnccBOeO5rXtjMPJ1D-Tpbq7NU84CSezc8dqLkjj_nTm3U4_wcSHfA1mLWRC7_y-5I04ZrCmN8qh34TIIx6pA-FEgXqxUzF30BQw5PTELjNOhzu3tCo2dB0gkGJpxLqLboT6rXW7PrwBECQNfA)](https://mermaid.live/edit#pako:eNqdVMtu2zAQ_BWCRoAEsAG3ARxHhwJ6GQ3QAG6cXlr1wEgri7BMuuQqjuH437N6WiniQ6yTuDs73J0hueexToA7PM31Ns6EQfYYRIrRd3HB7oVUzNfrjVag0NbxXxbMZcRT4aRiVNCiikT8qk7PjFYIKukgCdgV6g3zM4HsjnImFTF0eE_Eqz6cuJ6Jswkzd37XQR90QdX7FmnKJXOVyHdW2iYb8UMNDhbzXUf6ZMpJyhBbEL_s7X8vzAqwQ1YajHKpoMmwQKB414Yv4gyO41H6SVhgD2BBmDir8x068P5c_odc_PwhqfOgWV_9jVQnua-VghilVj252Wj0rRP2vcxl6rXtRRijtyMjlxmy74-Pc-rpXwGWnOOvraLvVK-IG-F6Ep8knRsdg7VsKzErOUtFj3KfLJsBki7l_Cw1el1W1uL2LfigOocUaQYsjKqrUX9i1wVqA8yALXK0TKqytPbmaOOpTWnQZ5lAf9dT-n24dyANucjcuJSr6tnrmbzAHZ2wZSUji8lIIyyWAYQXpECuTeO-JSQczU5lnjuD23EY3o6HFo1egTO4vr5u_kdbmWDmfN28DCsSZzCuvj5X23lNNb3xw9A7k6pSv-aZzbyJ_-VMnubQtUzu-MY9k6n2tCYKAnccBOeO5rXtjMPJ1D-Tpbq7NU84CSezc8dqLkjj_nTm3U4_wcSHfA1mLWRC7_y-5I04ZrCmN8qh34TIIx6pA-FEgXqxUzF30BQw5PTELjNOhzu3tCo2dB0gkGJpxLqLboT6rXW7PrwBECQNfA)

## 📦 Technical Stack

| Category       | Technologies                                                                 |
|----------------|-----------------------------------------------------------------------------|
| Frontend       | React, TypeScript, TailwindCSS, Vite                                        |
| Backend        | FastAPI, Python, DSPy, TA-Lib                                              |
| Database       | SQLite                                                                      |
| Deployment     | Docker, Docker Compose                                                      |
| AI Integration | Custom DSPy pipelines for financial analysis                               |

## 🎯 Component Structure

```
src/
├── components/
│   ├── ui/          # Shadcn UI components
│   ├── Header.tsx   # App header with theme toggle
│   ├── LandingPage.tsx  # Welcome screen with examples
│   ├── LoadingPage.tsx  # Loading state display
│   ├── MessageInput.tsx # Chat input component
│   ├── MetricCard.tsx   # Financial metrics display
│   ├── ResultPage.tsx   # Analysis results view
│   ├── ShareButton.tsx  # Share functionality
│   ├── StockChart.tsx   # Interactive stock chart
│   ├── StockHeader.tsx  # Stock price header
│   └── TradingSignal.tsx # Trading indicators
├── util/
│   ├── api.ts      # API client
│   ├── theme.ts    # Theme management
│   └── utils.ts    # Utility functions
└── App.tsx         # Main application
```

## 📄 License

MIT Licensed - See [LICENSE](LICENSE) for details.
