
```markdown
#  AI Career Coach — Interactive Notebook Platform

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini-2.5--flash-blueviolet.svg)](https://aistudio.google.com/)
[![FAISS](https://img.shields.io/badge/FAISS-Vector_Search-green.svg)](https://faiss.ai)
[![Gradio](https://img.shields.io/badge/Interface-Gradio--UI-orange.svg)](https://gradio.app)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

>  A complete, end-to-end intelligent career guidance ecosystem built entirely within a single interactive Jupyter Notebook. It features AI-powered resume parsing, semantic vector job matching and a multi-turn coaching chatbot window. Powered by Google Gemini 2.5-Flash, FAISS, and wrapped in an interactive web application framework using Gradio.

---

##  Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Notebook Architecture & Cell Layout](#notebook-architecture--cell-layout)
- [Installation & Local Setup](#installation--local-setup)
- [How to Run](#how-to-run)
- [Project Directory Structure](#project-directory-structure)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

##  Overview

The **AI Career Coach** notebook simplifies tech hiring preparation. Instead of manually cross-referencing capabilities against job profiles, this application provides:
1. **Structured Profile Extraction:** Instantly translates unformatted, plain-text resumes into organized JSON data maps via Gemini's native structural output controls.
2. **Semantic Similarity Matching:** Encodes candidate history and requirements into vector spaces using a local sentence-transformer model, ranking alignments against a job database using an L2-normalized FAISS Index.
3. **Upskilling Visualizations:** Highlights missing technical dependencies using Matplotlib donut and horizontal distribution charts.
4. **Conversational Mentorship Interface:** Hosts a multi-turn chat environment injected with individual candidate profile history to provide customized roadmap coaching.

---

## ✨ Key Features

* **JSON Enforced Parsing:** Uses high-speed LLM integration parameters with strict JSON execution tracking to dynamically structure profile details.
* **Vector Vectorbase Indexing:** Bypasses basic keyword matching by analyzing the contextual semantic meaning of text segments via an Inner Product (`FlatIP`) FAISS space.
* **Automated Graph Generation:** Dynamically builds and updates alignment diagnostics graphics, auto-saving data metrics as external image artifacts.
* **Dynamic Conversation State:** Preserves message histories across turns so users can smoothly transition from initial gap analysis straight into deep mock-interview prep sessions.
* **Dual-Tab Browser Layout:** Wraps everything cleanly into two simple, distinct interactive views: **Resume Analyzer & Matcher** and the **Conversational AI Career Coach Session**.

---

## 🛠️ Tech Stack

* **Generative Large Language Model:** Google Gemini 2.5-Flash (via `google-generativeai`)
* **Embedding Model Vectorizer:** Hugging Face `sentence-transformers` (`all-MiniLM-L6-v2`)
* **Vector Similarity Database:** Meta FAISS (`faiss-cpu`)
* **Data Layout Manipulation:** Pandas, NumPy, Python Set Algebra
* **Plotting UI Visualizers:** Matplotlib (optimized with headless non-GUI `'Agg'` operational overrides)
* **Application Framework Engine:** Gradio

---

## 📊 Notebook Architecture & Cell Layout

The `AI_Career_Coach.ipynb` notebook is organized into **11 sequential blocks** designed to run systematically from top to bottom:

| Cell # | Type | Name / Content | Purpose |
| :--- | :--- | :--- | :--- |
| **Cell 1** | 📝 Markdown | **Documentation & TOC** | Introduction badges, system summary, and the structural Table of Contents. |
| **Cell 2** | 💻 Code | **Dependency Installation** | Automatically runs `%pip install` for Gemini, FAISS, Gradio, Matplotlib, and Rich. |
| **Cell 3** | 💻 Code | **Imports & Configuration** | Loads standard libraries, configures the `all-MiniLM-L6-v2` embedding engine, and maps API environment keys. |
| **Cell 4** | 💻 Code | **Data Structures & Mock Jobs** | Establishes the core class layouts (`ResumeData`, `JobListing`) and seeds the baseline target job matrix. |
| **Cell 5** | 💻 Code | **Resume Parser (Gemini)** | Leverages Gemini's structured schema outputs to transform text strings into valid JSON formats. |
| **Cell 6** | 💻 Code | **FAISS Job Matcher** | Compiles local semantic vector models to map candidate attributes against target jobs. |
| **Cell 7** | 💻 Code | **Skill Gap Analyzer** | Performs mathematical set arithmetic to evaluate overlaps and generates Matplotlib analytics plots. |
| **Cell 8** | 💻 Code | **AI Career Coach Agent** | The central orchestration hub managing the internal subsystems and maintaining chatbot state memory threads. |
| **Cell 9** | 💻 Code | **Demo & Evaluation** | Validates the background logic end-to-end using a custom internal plain-text profile sample profile. |
| **Cell 10** | 📝 Markdown | **Project Summary Matrix** | A quick reference matrix showing components, tools, and developer next-step priorities. |
| **Cell 11** | 💻 Code | **Gradio Interactive UI** | Launches the browser-accessible interface containing separate interactive analysis panels and the chatbot console. |

---

## ⚙️ Installation & Local Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/yourusername/AI_Career_Coach.git](https://github.com/yourusername/AI_Career_Coach.git)
cd AI_Career_Coach

```

### 2. Configure a Virtual Environment

```bash
# Windows (Command Prompt / PowerShell)
python -m venv venv
.\venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate

```

### 3. Install Required Dependencies

```bash
pip install google-generativeai sentence-transformers faiss-cpu gradio pandas numpy matplotlib scikit-learn rich

```

### 4. Setup Your API Access Key

Get a free API access key string from [Google AI Studio](https://aistudio.google.com/).
Inside **Cell 3** of the notebook, replace the placeholder text with your secret key:

```python
os.environ["GEMINI_API_KEY"] = "sk-ant-api03-YourSecretKeyHere..."

```

---

## 🚀 How to Run

1. Open your terminal or workspace environment inside your virtual environment.
2. Launch your Jupyter interface server:
```bash
jupyter notebook

```


3. Open `AI_Career_Coach.ipynb`.
4. Click on **Kernel -> Restart Kernel and Run All Cells**.
5. Scroll down to the bottom of the notebook to **Cell 11**. Gradio will output a local browser URL link (typically `http://127.0.0.1:7860`). Click it to launch the interactive interface dashboard!

---

## 📁 Project Directory Structure

```text
AI_Career_Coach/
├── AI_Career_Coach.ipynb      # Complete notebook containing all 11 sequential execution cells
├── requirements.txt           # Python application ecosystem dependencies manifest
└── outputs/                   # Directory where analytics distribution graphs are auto-saved
    └── skill_gap_analysis.png # Generated skill-gap visualization plot

```

## 📄 License

Distributed under the MIT License. See `LICENSE` inside the repository root for further usage documentation allowances.

```

```
