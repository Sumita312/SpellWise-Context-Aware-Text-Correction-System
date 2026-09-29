
# SpellWise – Context-Aware Text Correction System

## Overview

SpellWise is a context-aware text correction tool designed to detect and correct spelling and word-level errors in user-provided text and documents.

It combines fast dictionary-based spelling correction using SymSpell with Google's Gemini LLM to improve corrections based on sentence context.

The system first identifies possible spelling mistakes using SymSpell and then uses Gemini to analyze the sentence context and select or improve the appropriate correction.

## Key Features

- Fast spelling correction using SymSpell
- Context-aware correction using Gemini LLM
- Handles both spelling errors and real-word errors
- Displays the original and corrected text
- Shows the corrections made at each stage
- Upload and correct PDF files
- Upload and correct DOC/DOCX files
- Download corrected documents
- Interactive web interface using Streamlit
- Simple and user-friendly correction workflow

## How It Works

The correction process consists of two main stages.

### 1. SymSpell Correction

SymSpell detects possible spelling mistakes using a dictionary, word frequency information, and edit-distance-based candidate generation.

For example:

```text
Input:
I lik to buy a pear of shoes

SymSpell Output:
I like to buy a pear of shoes
SymSpell can efficiently correct obvious spelling errors such as:

lik → like
2. Gemini Context Correction
The corrected text from SymSpell is then passed to the Gemini LLM.

Gemini analyzes the complete sentence and identifies errors that require contextual understanding.

SymSpell Output:
I like to buy a pear of shoes

Gemini Output:
I like to buy a pair of shoes
Here, Gemini identifies that pear should be pair based on the context of the sentence.

Example
Input
I lik to buy a pear of shoes
Correction Process
Wrong Word	Corrected Word	Fixed By
lik	like	SymSpell
pear	pair	Gemini
Final Output
I like to buy a pair of shoes
Document Correction
SpellWise also supports document-based spelling correction.

Users can upload:

PDF files

DOC files

DOCX files

The application extracts the text from the uploaded document and processes it through the SpellWise correction pipeline.

After correction, the application generates a corrected version of the document that can be downloaded by the user.

Document Workflow
Upload PDF / DOC / DOCX
        ↓
Extract Text
        ↓
SymSpell Spelling Correction
        ↓
Gemini Context Correction
        ↓
Generate Corrected Document
        ↓
Download Corrected File
Corrections Made
SpellWise provides a correction table showing:

Original incorrect word

Corrected word

Correction stage responsible for the change

For example:

Wrong	Corrected	Fixed By
lik	like	SymSpell
pear	pair	Gemini
This makes the correction process transparent and easy to understand.

Technology Stack
Python

Streamlit

SymSpell

Google Gemini API

Google Generative AI

Python

PDF/DOC/DOCX processing libraries

System Workflow
                User Input
                    ↓
          Text / Document Upload
                    ↓
             Text Extraction
                    ↓
          Text Preprocessing
                    ↓
           SymSpell Correction
                    ↓
          Candidate Corrections
                    ↓
         Gemini Context Analysis
                    ↓
            Final Correction
                    ↓
       Corrections Made Display
                    ↓
       Download Corrected File
SymSpell
SymSpell is used for fast spelling correction.

It generates possible correction candidates using edit distance and selects suitable words using dictionary and frequency information.

This makes the first correction stage fast and efficient.

Gemini LLM
Gemini is used as the context-aware correction layer.

Unlike traditional dictionary-based spell checkers, an LLM can analyze the meaning and context of a complete sentence.

This allows SpellWise to identify real-word errors where the word itself is correctly spelled but is incorrect in the given context.

For example:

I want to buy a pear of shoes.
The word pear is correctly spelled, but the context indicates that pair is intended.

Gemini can identify this contextual error and correct it.

Why a Hybrid Approach?
Traditional spelling correction methods are fast but mainly depend on dictionary and spelling information.

LLMs can understand sentence context but may require more computational resources.

SpellWise combines both approaches:

SymSpell
   ↓
Fast spelling correction
   ↓
Gemini
   ↓
Context-aware correction
This allows the system to use SymSpell for quick spelling corrections and Gemini for errors that require contextual understanding.



Run the Application
Start the Streamlit application using:

streamlit run app.py
The application will open in your browser.

Advantages
Combines traditional spelling correction with LLM-based contextual understanding

Fast initial correction using SymSpell

Handles context-dependent word errors

Supports text and document correction

Supports PDF and DOC/DOCX files

Allows users to download corrected documents

Provides transparent correction results

Simple and interactive Streamlit interface

Can be extended for advanced grammar and writing correction

Future Enhancements
Grammar correction

Sentence restructuring

Support for multiple languages

Improved correction confidence scores

Custom vocabulary support

Advanced error detection

Integration with text editors

Browser extension for real-time correction

Support for additional document formats

Conclusion
SpellWise combines the speed of traditional spelling correction with the contextual understanding of the Gemini LLM.

The hybrid approach allows the system to handle both common spelling mistakes and context-dependent word errors.

With support for text, PDF, and DOC/DOCX files, users can correct their content and download the corrected documents through a simple and interactive interface.


