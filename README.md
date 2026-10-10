# MeetBrief AI — Meeting Notes to Action Items

A Streamlit prototype for Use Case #9. It accepts meeting notes, uses the Groq API to generate a summary and extract decisions, action items, owners, due dates, open questions, and risks, and exports editable action items as CSV.

## Run locally

1. Install Python 3.10 or newer.
2. Open this folder in VS Code.
3. Create and activate a virtual environment:
   - Windows PowerShell: `py -m venv .venv` then `.venv\Scripts\Activate.ps1`
   - macOS/Linux: `python3 -m venv .venv` then `source .venv/bin/activate`
4. Install dependencies: `pip install -r requirements.txt`
5. Copy `.env.example` to `.env` and add your Groq API key.
6. Run: `streamlit run app.py`

If no API key is configured or the API fails, the app shows a clearly labeled basic fallback preview. Full AI functionality requires a valid API key and an available model.

## Privacy and limitations

When configured, meeting notes are sent to the selected third-party AI provider. Do not enter confidential or sensitive information. The app does not use a database; results are held in Streamlit session state. AI may omit or misinterpret action items, owners, and deadlines, so users must verify the output against the original notes.
