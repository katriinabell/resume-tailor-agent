# Resume Tailoring Agent

An AI-powered agent that creates tailored resumes by analyzing your qualifications and matching them to specific job descriptions.

## How It Works

1. Upload your **qualifications file** (all your skills, achievements, experience)
2. Upload your **current resume**
3. Paste a **job posting URL** (or the job description text)
4. Get a tailored resume highlighting the most relevant experience

The agent only uses factual information from your files - it never fabricates or exaggerates.

## Try It Online

**[Launch Resume Tailor](https://share.streamlit.io)** - Enter your own Anthropic API key to use

Get an API key at [console.anthropic.com](https://console.anthropic.com)

## Run Locally

```bash
git clone https://github.com/katriinabell/resume-tailor-agent.git
cd resume-tailor-agent

# Install dependencies
pip install -r requirements.txt

# Launch the web UI
streamlit run app.py
```

Then open http://localhost:8501 and enter your Anthropic API key in the sidebar.

## Web UI Features

- **File upload** - Supports .txt, .md, .pdf, .docx
- **Job URL** - Paste a link and the agent fetches the job description
- **Direct paste** - Or paste the job description text directly
- **Download** - Get your tailored resume as a Markdown file

## Tips for Best Results

### Qualifications file

The more detail you provide, the better:

- Specific metrics (revenue, users, % improvements)
- All technologies and tools you've used
- Soft skills and leadership experience
- Projects, certifications, volunteer work

See `qualifications.txt` for an example format.

### Convert to PDF

```bash
# Install pandoc, then:
pandoc tailored_resume.md -o tailored_resume.pdf
```

## Requirements

- Python 3.8+
- Anthropic API key ([get one here](https://console.anthropic.com))

## Tech Stack

- **Streamlit** - Web UI
- **Anthropic Claude** - AI resume tailoring
- **python-docx** - Word document formatting
