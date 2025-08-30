# 🎨 AI PPT Generator – Auto-Generate Presentations from Text

**Your Text, Your Style – Instantly turn bulk text or markdown into a professional PowerPoint presentation.**

AI PPT Generator is a lightweight web app that lets anyone paste long-form text (markdown, prose, reports, notes) and convert it into a fully styled, ready-to-present PowerPoint deck. Upload your own template, add optional guidance, and use your preferred LLM API key — the app takes care of the rest.

---

## ✨ Features

* 📝 **Flexible Input** – Paste large chunks of text, markdown, or prose.
* 🎯 **Guidance Option** – Add a one-line instruction for tone or structure (e.g., *“make it an investor pitch deck”*).
* 🔑 **Bring Your Own API Key** – Works with OpenAI, Anthropic, Gemini, and others (keys are never stored or logged).
* 🎨 **Template Reuse** – Upload a `.pptx` or `.potx` file to apply its colors, fonts, and layouts.
* 🖼️ **Image Reuse** – Recycles existing images from your uploaded template.
* 📥 **Instant Download** – Generates a `.pptx` you can download right away.
* ⚡ **Smart Slide Splitting** – Breaks text into a reasonable number of slides automatically.
* 🔒 **Privacy First** – No storage or logging of your text, keys, or files.

---

## 🚀 Quick Start

### 1. Clone the repo

```bash
git clone https://github.com/ASTITVAAG2005/AI_PPT_Generator.git
cd AI_PPT_Generator
```

### 2. Install dependencies

```bash
# Backend (Flask + python-pptx)
pip install -r requirements.txt

# Frontend is static HTML/JS/CSS
# no build step required
```

### 3. Run locally

```bash
uvicorn app:app --reload
```

Then open: [http://localhost:5000](http://localhost:5000)

### 4. Deploy (Vercel/Render/Railway/Heroku)

Works out-of-the-box — just connect your repo and deploy.

---

## 🖥️ Usage

1. Paste your text or markdown.
2. (Optional) Add a one-line guidance like *“make it a research summary”*.
3. Enter your LLM API key (OpenAI, Anthropic, Gemini).
4. Upload a `.pptx` or `.potx` template.
5. Click **Generate** → Download your styled presentation!

---

## 🛠️ Architecture

* **Frontend**

  * Responsive HTML + Bootstrap UI
  * Handles text input, template upload, history, and file downloads
  * Provides toasts, progress feedback, and theme toggle

* **Backend (Flask)**

  * Accepts text, guidance, API key, and template
  * Splits input intelligently into slide sections
  * Maps content onto the uploaded template’s style, fonts, and images
  * Generates `.pptx` output using `python-pptx`

---

## 🌟 Optional Enhancements

* Auto-generate speaker notes
* Prebuilt guidance templates (*sales deck, investor pitch, research summary*)
* Live slide previews before download
* Retry logic and stronger error handling for API calls

---

## 📄 License

MIT License – free to use, modify, and share.
