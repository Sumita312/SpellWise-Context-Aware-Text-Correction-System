# SpellWise - Context-Aware Text Correction System

SpellWise is a hybrid text correction system that combines **SymSpell-based spelling correction** with **Google Gemini-powered contextual correction**.

The system detects both traditional spelling mistakes and **real-word errors**, where a word is correctly spelled but incorrect according to the context of the sentence.

---

## ✨ Features

- ⚡ Fast spelling correction using **SymSpell**
- 🧠 Context-aware correction using **Google Gemini**
- 🔍 Detects spelling and real-word errors
- 📝 Displays original and corrected text
- 📊 Shows corrections made at each stage
- 📄 Supports PDF, DOC, and DOCX files
- 📥 Allows users to download corrected documents
- 🖥️ Interactive **Streamlit** web interface
- 🔄 Hybrid SymSpell + LLM correction pipeline

---

## 🔧 How It Works

SpellWise uses a two-stage correction pipeline.

### 1. SymSpell Correction

The first stage uses SymSpell for fast spelling correction.

SymSpell uses a frequency dictionary and edit-distance-based candidate generation to identify possible spelling errors efficiently.

**Example:**

**Input:**

```text
I lik to buy a pear of shoes.

SymSpell Output:

I like to buy a pear of shoes.

Correction:

lik → like
2. Gemini Context-Aware Correction

After SymSpell correction, the resulting text is passed to the Google Gemini LLM.

Gemini analyzes the complete sentence and identifies errors that require contextual understanding.

Example:

SymSpell Output:

I like to buy a pear of shoes.

Gemini Output:

I like to buy a pair of shoes.

Correction:

pear → pair

The word pear is correctly spelled, but it is incorrect in the context of buying shoes. Gemini uses the surrounding sentence context to identify pair as the intended word.

📝 Complete Example
Input
I lik to buy a pear of shoes.
Correction Process
Wrong Word	Corrected Word	Fixed By
lik	like	SymSpell
pear	pair	Gemini
Final Output
I like to buy a pair of shoes.
📁 Project Structure
SpellWise-Context-Aware-Text-Correction-System/
│
├── README.md
├── requirements.txt
├── streamlit_app.py
│
├── autocorrect_logic.py
├── llm_correction.py
├── correction_pipeline.py
│
├── document_processor.py
│
├── .env.example
└── .gitignore
📄 Document Correction

SpellWise also supports document-based text correction.

Supported Formats
PDF
DOC
DOCX
Document Workflow
Upload Document
      |
      v
Extract Text
      |
      v
SymSpell Correction
      |
      v
Gemini Context Correction
      |
      v
Generate Corrected Document
      |
      v
Download Corrected File

Users can upload a supported document, allow SpellWise to process and correct the text, and then download the corrected document.

📊 Correction Results

SpellWise displays the corrections made during the processing pipeline.

Example:

Original	Corrected	Correction Stage
lik	like	SymSpell
pear	pair	Gemini

This makes the correction process transparent and allows users to understand how each error was corrected.

🛠️ Technology Stack
Python
Streamlit
SymSpell
Google Gemini
Google GenAI SDK
PDF/DOC/DOCX processing libraries
🏗️ System Architecture
                    +------------------+
                    |    User Input    |
                    | Text / Document  |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    | Text Extraction  |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    |     SymSpell     |
                    |                  |
                    | Fast Spelling    |
                    | Error Detection  |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    | Candidate        |
                    | Corrections      |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    |   Gemini LLM     |
                    |                  |
                    | Context Analysis |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    | Final Corrected  |
                    |      Text        |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    |  Streamlit UI    |
                    | + Corrections    |
                    +------------------+
💡 Why a Hybrid Approach?

Traditional spelling correction systems are fast and efficient, but they mainly depend on dictionaries, word frequencies, and edit distance.

They may fail to identify real-word errors.

For example:

I want to buy a pear of shoes.

Both pear and pair are valid dictionary words.

A traditional spelling checker may therefore not identify the error.

The Gemini LLM analyzes the sentence context and can identify:

pear → pair

SpellWise combines both approaches:

SymSpell
   |
   v
Fast Spelling Correction
   |
   v
Gemini
   |
   v
Context-Aware Correction

This combines the speed of traditional spelling correction with the contextual capabilities of an LLM.

✅ Advantages
Fast initial spelling correction
Context-aware error detection
Detection of real-word errors
Combination of traditional NLP and LLM technology
Text and document correction
PDF, DOC, and DOCX support
Transparent correction results
Corrected document download
Simple Streamlit interface
Modular project architecture

🚀 Future Enhancements
Grammar correction
Sentence restructuring
Multi-language support
Correction confidence scores
Custom vocabulary support
Advanced grammar and style correction
Real-time text correction
Browser extension
Text editor integration
Additional document formats
Improved document formatting preservation

🎯 Project Highlights
Developed a hybrid spelling correction system using SymSpell with a frequency dictionary and edit-distance-based candidate generation for fast error detection.
Integrated Google Gemini as a context-aware correction layer to select or improve candidate corrections based on sentence context.
Implemented detection of real-word errors that traditional dictionary-based spell checkers may miss.
Built an interactive Streamlit web application that displays the original text, intermediate SymSpell output, final corrected text, and corrections made.
Added support for PDF, DOC, and DOCX document correction.
Enabled users to download corrected documents after processing.
Designed a modular architecture separating spelling correction, LLM correction, document processing, and the user interface.
📌 Conclusion

SpellWise demonstrates a hybrid approach to text correction by combining the efficiency of SymSpell with the contextual capabilities of Google Gemini.

The system handles both conventional spelling mistakes and context-dependent word errors while providing users with a transparent view of the corrections performed.

With support for text and document processing through an interactive Streamlit interface, SpellWise provides a foundation for future grammar, writing, and language-correction features.

👨‍💻 Project

SpellWise - Context-Aware Text Correction System


