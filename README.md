# paper-checking
# 📄 Resume ATS Score Checker

Upload a resume (PDF, DOCX or TXT) and get:

- An overall **ATS score** out of 100
- Scores for formatting, keywords, experience, skills, education and impact
- Strengths, missing keywords and specific improvements
- Optional **job description** input for better keyword matching
- A downloadable text report

Built with **Streamlit** and the **Gemini Flash** model.

## Run locally

1. Get a free API key from [Google AI Studio](https://aistudio.google.com/apikey).
2. Install and run:

```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Create `.streamlit/secrets.toml` (never commit this file):

```toml
GEMINI_API_KEY = "your-key-here"
# GEMINI_MODEL = "gemini-flash-latest"   # optional
```

4. Start the app:

```bash
streamlit run app.py
```

## Deploy on Streamlit Community Cloud

1. Push this project to a GitHub repository.
2. Go to [share.streamlit.io](https://share.streamlit.io) and sign in with GitHub.
3. Click **Create app**, choose your repo, branch `main` and main file `app.py`.
4. Open **Advanced settings → Secrets** and paste: `GEMINI_API_KEY = "your-key-here"`
5. Click **Deploy**.

## Files

| File | Purpose |
|------|---------|
| `app.py` | The Streamlit app |
| `requirements.txt` | Python dependencies |
| `README.md` | This guide |

## Notes

- Scanned (image-only) PDFs cannot be read. Use a text-based PDF or DOCX.
- The score is an AI estimate, not the result of a real company's ATS.
