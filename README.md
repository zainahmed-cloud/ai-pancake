# ai-pancake

# 🛡️ ResearchConcierge: Automated Fraud Research Pipeline

An autonomous Python-based intelligence pipeline that **fetches**, **summarizes**, and **synthesizes** Open Access research papers. This tool is designed for security researchers and Data Science Managers to stay ahead of evolving threats like **Account Takeover (ATO)**, **Smishing**, and **Payment Fraud**.

---

## 🚀 Key Features

* **Automated Sourcing:** Queries the **OpenAlex API** to identify high-authority, Open Access papers.
* **Structured Extraction:** Leverages **Gemini 2.5/3.0** to parse complex academic metadata into structured JSON (Methodology, Data Sources, Key Findings).
* **CISO-Level Synthesis:** Collates findings from multiple papers into a high-level security brief with tactical industry action items.
* **Zero-Paywall:** Exclusively filters for legally free-to-read research (Open Access).

---

## 🏗️ Architecture

The pipeline follows a modular three-stage logic:

1.  **The Fetcher:** Pings OpenAlex for topics like `phishing` and `identity fraud`, filtering for `is_oa:true`.
2.  **The Summarizer:** Processes the OpenAlex "Inverted Index" and uses Gemini to populate a structured schema.
3.  **The Concluder:** Aggregates all data into a final report identifying research gaps and engineering action items.

---

## 🛠️ Tech Stack

| Component | Technology |
| :--- | :--- |
| **Language** | Python 3.10+ |
| **Data Source** | [OpenAlex API](https://openalex.org/) |
| **LLM Engine** | Google Gemini (2.5-Flash or 3-Flash) |
| **SDK** | `google-genai` (2026 Standard) |
| **Data Modeling** | Pydantic (Structured Data) |

---

## 🚦 Getting Started

### 1. Prerequisites
You will need a Google AI Studio API Key. [Get one for free here](https://aistudio.google.com/).

### 2. Installation
```bash
pip install -U google-genai requests pydantic
