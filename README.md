# 🎥 AI Video Assistant

An end-to-end AI-powered meeting intelligence system that converts YouTube videos, local video files, audio recordings, and meeting recordings into structured insights using Whisper AI, Sarvam AI, LangChain, Mistral AI, and ChromaDB.

The application automatically transcribes meetings, generates summaries, extracts action items, identifies key decisions, highlights open questions, and allows users to chat with their meetings using Retrieval-Augmented Generation (RAG).

---

## 🚀 Features

### 🎙️ Meeting Transcription
- Accepts YouTube URLs
- Accepts local audio/video files
- English transcription using OpenAI Whisper (Local)
- Hindi & Hinglish transcription using Sarvam AI

### 📝 AI Meeting Summary
- Generates structured meeting summaries
- Extracts key discussion points
- Creates concise bullet-point outputs

### ✅ Action Item Extraction
- Detects tasks discussed in meetings
- Extracts responsible owners
- Identifies deadlines when available

### 🎯 Key Decisions Extraction
- Captures important decisions made during discussions
- Creates a structured decision log

### ❓ Open Questions Detection
- Finds unanswered questions
- Identifies follow-up discussion points

### 💬 Chat With Your Meeting
- Ask questions about meeting content
- Uses RAG (Retrieval-Augmented Generation)
- Context-aware answers from meeting transcript

### 📄 Report Export
- Export meeting report as TXT
- Export meeting report as PDF


# 🛠 Tech Stack

| Technology | Purpose |
|------------|----------|
| Python | Core Development |
| Streamlit | User Interface |
| OpenAI Whisper | English Speech-to-Text |
| Sarvam AI | Hindi/Hinglish Transcription |
| LangChain LCEL | AI Workflow Pipeline |
| Mistral AI | Summarization & Extraction |
| ChromaDB | Vector Database |
| HuggingFace Embeddings | Embedding Generation |
| RAG | Context-Aware Question Answering |

---

# 🏗 System Architecture

```text
Input (YouTube / Audio / Video)
            │
            ▼
      Audio Processing
            │
            ▼
       Transcription
            │
            ▼
      Meeting Transcript
            │
   ┌────────┼────────┐
   ▼        ▼        ▼
Summary  Extraction  Vector DB
                    (ChromaDB)
                         │
                         ▼
                   RAG Chatbot
```

---

# 📂 Project Structure

```text
AI Video Assistant/
│
├── core/
│   ├── extractor.py
│   ├── rag_engine.py
│   ├── summarizer.py
│   ├── transcriber.py
│   └── vector_store.py
│
├── utils/
│   └── audio_processor.py
│
├── downloads/
│
├── vector_db/
│
├── app.py
├── mein.py
├── .env
├── requirements.txt
└── README.md
```

---

# ⚙️ Installation

## 1️⃣ Clone Repository

```bash
git clone https://github.com/ajaygangwar8807/AI-Video-Assistant.git
cd AI-Video-Assistant
```

## 2️⃣ Create Virtual Environment

```bash
python -m venv .venv
```

Activate:

### Windows

```bash
.venv\Scripts\activate
```

### Mac/Linux

```bash
source .venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
uv pip install -r requirements.txt
```

---

## 4️⃣ Create .env File

```env
MISTRAL_API_KEY=your_api_key_here
SARVAM_API_KEY=your_api_key_here
```

---

# 🔑 API Setup

## Mistral AI

1. Create account on Mistral AI
2. Generate API Key
3. Add key in `.env`

## Sarvam AI

1. Create account on Sarvam AI
2. Generate API Key
3. Add key in `.env`

---

# 📚 Module Breakdown

## utils/audio_processor.py

### Responsibilities

- Download audio from YouTube
- Extract audio from video
- Convert files to WAV
- Audio preprocessing
- Audio chunking

---

## transcriber.py

### Responsibilities

- Speech-to-Text conversion
- Whisper integration
- Sarvam AI integration
- Generate meeting transcript

---

## summarizer.py

### Responsibilities

- Transcript summarization
- Structured summary generation
- Bullet-point formatting

---

## extractor.py

### Responsibilities

- Extract Action Items
- Extract Key Decisions
- Extract Open Questions
- Structured information extraction

---

## vector_store.py

### Responsibilities

- Generate embeddings
- Store vectors in ChromaDB
- Create searchable knowledge base

---

## rag_engine.py

### Responsibilities

- Retrieval-Augmented Generation
- Semantic search
- Context-aware answering

---

## mein.py

### Responsibilities

- Complete AI pipeline execution
- Generate summaries
- Generate action items
- Generate decisions
- Chat with meeting transcript

---

## app.py

### Responsibilities

- Streamlit UI
- User interactions
- Report display
- Meeting chat interface

---

# ▶️ Run Application

## Streamlit UI

```bash
streamlit run app.py
```

---

## CLI Version

```bash
python mein.py
```

---

# 💡 Example Workflow

1. Paste YouTube URL
2. Audio downloaded automatically
3. Meeting transcribed
4. Summary generated
5. Action items extracted
6. Decisions extracted
7. Open questions identified
8. Vector database created
9. Chat with meeting using RAG

---

# 🔮 Future Improvements

- Multi-language support
- Speaker diarization
- Meeting sentiment analysis
- Automatic email reports
- Cloud deployment
- Real-time transcription
- Meeting analytics dashboard

---

# 👨‍💻 Author

**Ajay Gangwar**

GitHub:
https://github.com/ajaygangwar8807

LinkedIn: [Ajay Gangwar](https://www.linkedin.com/in/ajay-gangwar-538765394/)

---

# ⭐ Support

If you found this project useful, consider giving it a ⭐ on GitHub.