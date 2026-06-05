# ✨ Autocorrect Tool — NLP + Document Processing

> *your words, perfected*

A Python-based **NLP + Document Processing** tool with a beautiful web interface built using Streamlit. Uses **LanguageTool** for intelligent spell and grammar correction — automatically handles proper nouns, technical terms, and supports PDF and Word document upload.

---

## 🧠 NLP Techniques Used

- **LanguageTool Engine** — rule-based NLP with 3000+ grammar and spelling rules
- **Edit Distance Algorithm** — finds closest correct word using Levenshtein distance
- **Word Frequency Analysis** — ranks corrections by real-world usage probability
- **Named Entity Awareness** — automatically skips proper nouns, names, places
- **Tokenization** — splits text into tokens for word-level analysis

---

## 🚀 Features

- ✅ Real-time spell and grammar correction
- ✅ PDF upload and text extraction
- ✅ Word (.docx) document upload and correction
- ✅ Download corrected document as .docx
- ✅ Automatically skips names, places, tech words
- ✅ Shows all corrections made with before/after view

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Streamlit |
| NLP Engine | LanguageTool (language_tool_python) |
| PDF Processing | PyMuPDF (fitz) |
| Word Processing | python-docx |
| Language | Python 3.x |

---

## 📂 Project Structure
