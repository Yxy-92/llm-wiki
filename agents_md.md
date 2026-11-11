# Agent Guidelines & Wiki Schema

This repository follows the LLM Wiki methodology (inspired by Andrej Karpathy's knowledge management approach).

## 1. Core Principles
- **Self-Contained Knowledge Base**: Every note should be markdown-based, portable, and clean.
- **Bi-Directional Linking**: Use `[[Note-Name.md]]` syntax for internal cross-referencing between papers and concept synthesis.
- **Human-in-the-Loop Maintenance**: Notes are iteratively created, synthesized, and expanded via structured agent loops.

## 2. File Organization Rules
- `wiki/index.md`: Central landing page and directory.
- `wiki/log.md`: Chronological history of updates, passes, and agent execution records.
- `wiki/papers/`: Individual paper digests named as `[Author][Year]-[ShortName].md`.
- `wiki/concepts/`: Topic-level synthesis combining insights from multiple papers.

## 3. Maintenance Loop Process
- **Loop 1 (Ingestion & Extraction)**: Read source PDFs from `raw/papers/`, output raw Markdown summaries in `wiki/papers/`.
- **Loop 2 (Synthesis & Application)**: Cross-link related papers into `wiki/concepts/`, generate presentation artifacts like `llm.html`.