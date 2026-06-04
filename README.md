# 📋 Handwritten Prescription Digitizer — Vision OCR + Urdu Voice

> **Production AI pipeline** that converts handwritten doctor 
> prescriptions into structured digital PDFs with Urdu voice 
> summaries — making medical prescriptions accessible to 
> low-literacy patients at Pakistan's largest digital health platform.

![GPT-4o](https://img.shields.io/badge/GPT--4o_Vision-412991?style=flat-square&logo=openai&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-000000?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![ElevenLabs](https://img.shields.io/badge/ElevenLabs_TTS-000000?style=flat-square&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)

---

## 📊 Production Impact

| Metric | Value |
|--------|-------|
| Patient support queries reduced | 35% |
| Input type | Handwritten doctor prescriptions |
| Output | Structured digital PDF + Urdu voice summary |
| Languages | English extraction · Urdu voice output |
| Deployment | AWS · Docker · Production |

---

## 🏗️ LangGraph Pipeline Architecture

![System Architecture](architecture/system architecture.png)

> **Smart 8-step pipeline** — validates image quality first, then 
> structures data, generates Urdu summary, renders PDF, cleans 
> voice text, synthesizes voice, and finalizes output. Rejects 
> gracefully if prescription cannot be processed.

---

## ⚡ Key Features

- **GPT-4o Vision OCR** — reads real-world handwritten prescriptions 
  regardless of handwriting quality, ink type, or paper condition
- **NER pipeline** — extracts medicine names, dosages, frequency, 
  and doctor instructions as structured entities
- **Structured PDF generation** — converts unreadable handwriting 
  into clean, organized digital records
- **Urdu voice summary** — ElevenLabs TTS reads the prescription 
  aloud in Urdu for patients who cannot read English
- **Healthcare accessibility** — bridges the literacy and language 
  gap for millions of patients across Pakistan
- **Production deployed** — handling real prescriptions at 
  Pakistan's largest digital health platform daily

---

## 🔄 How It Works

```mermaid
sequenceDiagram
    participant P as 👤 Patient
    participant API as FastAPI
    participant V as GPT-4o Vision
    participant N as NER Agent
    participant T as ElevenLabs TTS

    P->>API: Upload photo of prescription
    API->>V: Send for handwriting recognition
    V-->>N: Raw extracted text
    N->>N: Extract medicines, dosages, instructions
    N-->>API: Structured prescription data
    API->>API: Generate structured PDF
    API->>T: Send Urdu text for voice generation
    T-->>API: Urdu audio file
    API-->>P: ✅ Digital PDF + Urdu voice summary
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Vision & OCR | GPT-4o Vision |
| Entity Extraction | NER Pipeline, LangChain |
| Voice Generation | ElevenLabs TTS |
| PDF Generation | pdfplumber, Python |
| Backend | FastAPI, Python |
| Deployment | Docker, AWS |

---

## 📊 Sample Results

### 🖼️ Prescription Comparison — Handwritten vs Digital Output
![Prescription Comparison](results/prescription_comparison_arrow.png)

### 📄 Generated Digital PDF
[View Prescription Output PDF](results/prescription_output%20(1).pdf)

### 🎙️ Urdu Voice Summary
> 🔊 [Listen to Urdu Voice Summary](results/urdu_summary.mp3)
>
> *AI-generated Urdu audio reading of the prescription — 
> making doctor instructions accessible to low-literacy patients*

---

> ⚠️ **Note:** This repository showcases the architecture and 
> design of a production system. Source code 
> is proprietary.

---

## 📫 Contact

**Adnan Abdullah** — Agentic AI Engineer & AI Team Lead

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/adnan-abdullah-700899b)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:muhammad.adnannust@gmail.com)

---

*Built with GPT-4o Vision + ElevenLabs · Deployed at Pakistan's 
largest digital health platform · 35% reduction in patient 
support queries*
