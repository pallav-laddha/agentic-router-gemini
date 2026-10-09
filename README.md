# Agentic Router with Gemini

A Colab-ready adaptation of the Module 3 Agentic RAG notebook that uses Google's Gemini API instead of the OpenAI API for routing, RAG answer generation, and sub-query generation.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pallav-laddha/agentic-router-gemini/blob/main/Agentic_Router_Gemini.ipynb)

## Setup

1. Open the notebook in Google Colab.
2. Open **Secrets** using the key icon in the left sidebar.
3. Add `GEMINI_API_KEY` and enable notebook access.
4. Optionally add `SERP_API_KEY` for queries routed to live internet search.
5. Run the notebook from top to bottom.

No API keys or other credentials are committed to this repository. The notebook uses `gemini-3.8-flash` by default and keeps the original local Nomic embedding model and Qdrant collections.

## Source and changes

The notebook is adapted from [`hamzafarooq/multi-agent-course`](https://github.com/hamzafarooq/multi-agent-course), Module 3, `Agentic_RAG_Notebook.ipynb`.

Changes in this version:

- Replaced OpenAI SDK and GPT model calls with the official `google-genai` SDK and Gemini.
- Implements the assignment's sub-query division: compound questions are split and each part is routed and answered independently.
- Reads `GEMINI_API_KEY` exclusively from Colab Secrets.
- Preserves the original notebook's 37-cell structure and instructional sections.
- Removed saved execution output and execution counts before publication.

This repository does not claim ownership of the original course material. Any terms applying to the source material continue to apply to the adapted notebook.
