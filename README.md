🎥 AI Video Summarizer
Transcribe, summarize, and generate intelligent clips from your video and audio files with ease.

Powered by WhisperX, LLMs (via Replicate and Anthropic), and a sleek web interface.

✨ Features
🎙 Transcription

Fast and accurate speech-to-text using WhisperX

🧠 Smart Summarization

Generate concise, context-aware summaries for:

Meeting Minutes

Podcast Episodes

Lectures

Interviews

General Video Content

🎬 Automatic Clip Creation

Extract key moments as short clips with timestamps and context

🎛 Multi-format Support

Supports most popular video/audio formats

☁️ Cloud-Ready

Uploads and stores files via AWS S3 for streamlined handling

🧩 Modular

Easily swap LLMs or summarization techniques

⚙️ Prerequisites
Ensure the following tools are installed:

Python 3.8+

Node.js & npm (for frontend GUI)

FFmpeg

AWS CLI (configured with access to your S3 bucket)

🚀 Installation
1. Clone the Repo
bash
Copy
Edit
git clone https://github.com/sidedwards/ai-video-summarizer.git
cd ai-video-summarizer
2. Backend Setup (Python)
bash
Copy
Edit
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
Configure settings:

bash
Copy
Edit
cp config/config-example.yaml config/config.yaml
# Edit `config.yaml` with your API keys, S3 info, etc.
3. Frontend Setup (Optional - for GUI)
bash
Copy
Edit
cd frontend
npm install
🧪 Usage
💻 CLI Mode
bash
Copy
Edit
python backend/cli.py
Follow prompts to:

Select a video/audio file

Choose summary type

Output will be saved in a folder named after your input file

🌐 GUI Mode (Web App)
1. Start Backend Server
bash
Copy
Edit
python backend/server.py
2. Start Frontend Server
In a new terminal:

bash
Copy
Edit
cd frontend
npm run dev
Open your browser: http://localhost:5173

Upload files → Choose summary type → Download output as a ZIP file.

⚙️ Configuration
Edit config/config.yaml to customize:

AWS CLI path + S3 bucket

Replicate API key and model

Anthropic API key (optional)

Transcription/summarization options

📍 Roadmap
 Web-based GUI

 Intelligent summarization

 Clip generation

 Export to PDF/DOCX

 Add more LLM options (Mistral, OpenRouter, etc.)

 Batch file processing

🤝 Contributing
Pull Requests and feature suggestions are welcome!
Feel free to fork, clone, and make magic.

📝 License
MIT License

🙏 Acknowledgements
WhisperX — advanced OpenAI Whisper variant

Fast transcription

Speaker diarization

Segment-level accuracy (via Replicate)

