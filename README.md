# Youtube lm

Ask questions about any YouTube video and get AI-powered answers based on its captions. Built with RAG, vector search, and Google Gemini.

## ✨ Features

- 📥 Extract captions from any YouTube video (auto or manual subtitles)
- 🧹 Clean and format SRT text with custom regex (preserves timestamps)
- 🧠 Embed sentences using OpenRouter embeddings
- 🔍 Store & search with ChromaDB (persistent vector database)
- 💬 Get answers grounded in video content using Google Gemini

## 🚀 Quick Start

### 1. Clone & Install
```bash
git clone https://github.com/Neska-mz/youtube_lm
cd youtube_lm
pip install -r requirements.txt
```
### 2. Set Up Environment Variables
Create a .env file in the root directory:
```bash
GOOGLE_API_KEY=your_gemini_api_key
OPENROUTER_API_KEY=your_openrouter_api_key
```
### 3. Run the Notebook and use it

### 📦 Requirements
```bash
chromadb
numpy
pandas
bm25s
pytubefix
nltk
google-genai
python-dotenv
ipython
jupyter
```
Install with:
```bash
pip install -r requirements.txt
```

### ⚙️ How It Works
1. Extract: Fetch SRT captions from YouTube using pytubefix
2. Parse: Clean timestamps with regex → "Text (00:00:00,320)"
3. Chunk: Split into sentences using nltk.tokenize.sent_tokenize
4. Embed: Convert to vectors via OpenRouter API
5. Store: Save to ChromaDB with unique IDs
6. Query: Retrieve top-k relevant passages + generate answer with Gemini

### ⚠️ Important Notes
- Works best with videos that have accurate captions (manual > auto-generated)
- Respect YouTube's Terms of Service and copyright laws
- Get your API keys:
      Google AI Studio for Gemini
      OpenRouter for embeddings
