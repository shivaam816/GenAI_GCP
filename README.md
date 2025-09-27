# GenAI_GCP Assignment 1
Created this repo for Assignment purpose
# Real-Time Market Sentiment Analyzer Using LangChain + Google Gemini

## Overview
This project implements a **real-time market sentiment analyzer** using **LangChain Chains** and **Google Gemini-2.0-flash** via Vertex AI.  
The pipeline accepts a company name, fetches its stock code, retrieves recent news, analyzes sentiment and entities, and outputs a **structured JSON**. All prompts, outputs, and metadata are logged using **mlflow** for observability and debugging.

---

## Features
- Accepts **company name input**.
- Extracts **stock ticker** using Yahoo Finance.
- Fetches latest **company news** using BraveSearch (LangChain tools).
- Uses **Google Gemini-2.0-flash** for sentiment analysis and entity extraction.
- Outputs a **JSON object** with structured fields:
  ```json
  {
    "company_name": "",
    "stock_code": "",
    "newsdesc": "",
    "sentiment": "Positive/Negative/Neutral",
    "people_names": [],
    "places_names": [],
    "other_companies_referred": [],
    "related_industries": [],
    "market_implications": "",
    "confidence_score": 0.0
  }
