# 📝 MeetBrief AI — AI-Powered Meeting Summarizer

**Turn meeting notes and recordings into clear summaries, decisions, and actionable tasks.**

MeetBrief AI is an AI-powered web application built with Python and Streamlit that converts meeting notes into structured meeting briefs. It supports text input, handwritten or printed notes, audio recordings, and video recordings containing speech.

Designed with multilingual Indian workplaces in mind, MeetBrief AI supports transcription workflows involving **English, Hindi, and Hinglish**, while generating professional English meeting summaries and action items.

## ✨ Features

- **📝 Text-Based Input:** Paste meeting notes or transcripts directly into the application.
- **📷 Handwritten Notes Extraction:** Upload images of handwritten or printed meeting notes and extract their text using a vision model.
- **🎙️ Audio Transcription:** Convert audio recordings into text using Groq's Whisper transcription model.
- **🎬 Video Transcription:** Extract audio from video recordings and transcribe the spoken content.
- **🌐 Multilingual Support:** Designed to handle English, Hindi, and Hindi-English code-switching (Hinglish).
- **📌 AI-Generated Meeting Briefs:** Generate concise summaries, key decisions, action items, open questions, and risks or blockers.
- **👥 Task Ownership and Deadlines:** Extract task owners, stated deadlines, priorities, and supporting context when available.
- **📄 Export Options:** Download meeting briefs as Word or PDF documents and export action items as CSV files.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| Streamlit | Interactive web application interface |
| Groq API | Access to AI models |
| Whisper Large v3 | Audio transcription |
| Qwen 3.8 27B | Image-based note extraction |
| GPT-OSS 20B | Meeting analysis and structured output |
| Pandas | Action-item data handling |
| python-docx | Word document generation |
| ReportLab | PDF generation |
| MoviePy | Audio extraction from video |

## 🔄 How It Works

1. **Provide meeting content:** Enter notes, upload an image, or provide an audio or video recording.
2. **Extract the information:** The application reads image-based notes or transcribes spoken content.
3. **Review the transcript:** Check the extracted text and correct any recognition errors.
4. **Generate the meeting brief:** The AI identifies the summary, decisions, action items, owners, deadlines, open questions, and blockers.
5. **Export the results:** Download the brief in Word or PDF format, or export the action-item list as CSV.

## 🏗️ Application Workflow

```text
Meeting Notes / Image / Audio / Video
                 |
                 v
       Text Extraction or
        Audio Transcription
                 |
                 v
       Transcript Review
                 |
                 v
        AI Meeting Analysis
                 |
                 v
       Structured Meeting Brief
                 |
                 v
     Word / PDF / CSV Downloads
```

## 🚀 Run Locally

### Prerequisites

- Python 3.10 or later
- A Groq API key
- FFmpeg or other required video-processing dependencies for your environment, if needed

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/MeetBrief-AI.git
cd MeetBrief-AI
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Configure your API key

Create a `.env` file in the project directory:

```env
GROQ_API_KEY=your_groq_api_key
GROQ_MODEL=openai/gpt-oss-20b
```

Replace the placeholder with your own Groq API key.

**Security:** Never commit your `.env` file or expose your API key in source code, screenshots, or public repositories.

### 5. Launch the application

```bash
python -m streamlit run app.py
```

Open the local URL displayed in the terminal, usually `http://localhost:8501`.

## ☁️ Deployment

MeetBrief AI can be deployed using Streamlit Community Cloud.

1. Push the project to a GitHub repository.
2. Open [Streamlit Community Cloud](https://share.streamlit.io/).
3. Connect your GitHub account and select the `MeetBrief-AI` repository.
4. Set `app.py` as the application entry point.
5. Add your Groq API key and model configuration under the app's **Secrets** settings.

For Streamlit Cloud, secrets can be configured in TOML format:

```toml
GROQ_API_KEY = "your_groq_api_key"
GROQ_MODEL = "openai/gpt-oss-20b"
```

Do not commit actual credentials to GitHub.

## 🌐 Multilingual Meeting Support

MeetBrief AI is designed for meetings where participants switch between Hindi and English.

For example:

> "Kal tak homepage ka design complete karna hai. Rahul Friday se payment gateway testing start karega."

The transcription workflow aims to preserve the original spoken language, while the meeting analysis produces a structured English brief.

**Note:** Speech recognition can make mistakes, especially with noisy audio, names, regional accents, and mixed-language speech. Transcripts and extracted action items should be reviewed before use.

## ⚠️ Limitations

- Transcription accuracy depends on audio quality, speech clarity, accents, and language switching.
- Image extraction may be imperfect for difficult handwriting or low-quality images.
- The application processes audio from videos; it does not independently interpret visual scenes.
- AI-generated summaries and action items may omit or misinterpret information.
- Available model access, API usage limits, and hosting resources may affect performance.

## 🔐 Privacy and Security

- API credentials should be stored in environment variables or deployment secrets.
- Meeting transcripts may contain confidential information; only upload content you are authorized to process.
- Review the privacy policies and data-handling terms of the AI and hosting services before using sensitive workplace recordings.

## 🎯 Project Objective

The objective of MeetBrief AI is to reduce the manual effort required to document meetings by turning unstructured notes and spoken discussions into organized, reviewable, and exportable meeting briefs.

The project demonstrates the practical use of generative AI, speech transcription, image understanding, structured information extraction, and web application development.

## 👩‍💻 Author

**Shivika Khanna**

PGDM — Big Data Analytics  
FORE School of Management

---

*Built with Python, Streamlit, and Groq-powered AI models.*
