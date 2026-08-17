# XAI: SHAP vs LIME — Multi-Agent LLM Evaluation

**MSc Cybersecurity Dissertation Artefact** | Coventry University | 7005SCN Individual Research Project
Student: Mutahhir | Supervisor: Theodoros Spyridopoulos

## Overview

Compares SHAP and LIME explainability methods for a machine learning-based Intrusion Detection System (Random Forest, XGBoost, SVM on CICIDS2017). Explainability is evaluated using a multi-agent pipeline that simulates three expert personas: SOC Manager, Compliance Auditor, CISO. Rating SHAP vs LIME across three LLM providers (Gemini, Claude, GPT).

## Files

- `notebooks/shap_lime_pipeline.ipynb` - full pipeline: model training, SHAP/LIME generation, multi-agent LLM evaluation
- `dashboard/index.html` - standalone results dashboard, open directly in any browser

## Key Finding

Across all 9 agents (3 personas × 3 LLM providers), LIME was preferred by technical/operational personas (SOC Manager, Compliance Auditor) in every case, while the CISO (non-technical executive) persona preferred SHAP. This preference split held consistently across Gemini, Claude, and GPT, suggesting the pattern reflects genuine differences in explanation style rather than quirks of a single model.

## Requirements

`pip install google-genai anthropic openai pandas`

## Running

Run the notebook top to bottom in Google Colab. Requires `GEMINI_API_KEY`, `ANTHROPIC_API_KEY`, and `OPENAI_API_KEY` set as Colab Secrets.

## Research Note

This is a research artefact for a comparative XAI study. Model versions used: `gemini-3.5-flash`, `claude-sonnet-5`, `gpt-5.5` (Aug 2026).
