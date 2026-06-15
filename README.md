# OpenParse

**Universal Document Intelligence Platform**

[![Python 3.12+](https://img.shields.io/badge/python-3.12+-blue.svg)](https://www.python.org/downloads/)
[![License: TBD](https://img.shields.io/badge/license-TBD-green.svg)](#license)
[![Status: Planning](https://img.shields.io/badge/status-planning-orange.svg)](#roadmap)

---

## What is OpenParse?

OpenParse is an open-source document intelligence platform that transforms unstructured documents into structured, AI-ready knowledge. It preserves hierarchy, tables, diagrams, and semantic relationships — going beyond traditional OCR.

### The Problem

Modern AI systems struggle with:
- PDFs, scanned documents, contracts, invoices, reports
- Mixed-content files with tables, figures, and complex layouts
- Existing tools extract text but **lose structure**

### The Vision

Process any document through a **single API** and receive structured outputs: Markdown, JSON, tables, chunks, metadata, and knowledge representations.

---

## Core Capabilities

| Module | Description |
|--------|-------------|
| **Document Classification** | Detects file type, language, scan quality, tables, forms, handwriting, complexity, category |
| **OCR Orchestration** | PaddleOCR, SuryaOCR, Tesseract with confidence scoring & fallback strategies |
| **Layout Analysis** | Identifies headings, paragraphs, lists, tables, figures, footnotes, page structure |
| **Structure Recovery** | Reconstructs logical hierarchy: Chapters, Articles, Clauses, Sections |
| **Table Intelligence** | Extracts tables, merges cells, exports to JSON, CSV, Markdown, DataFrames |
| **Image Understanding** | Extracts metadata, OCR from embedded images, chart descriptions |
| **Diagram Understanding** | Extracts diagram nodes/edges, visual relationships for AI retrieval |
| **Semantic Chunking** | Creates hierarchy-aware chunks preserving document structure & context |
| **RAG Optimization** | Optimizes output for retrieval-augmented generation pipelines |

---

## Architecture

```
Document Analyzer → OCR Engine Manager → Layout Understanding
       ↓                    ↓                    ↓
Structure Recovery → Table Intelligence → Image & Diagram Understanding
       ↓                    ↓                    ↓
         Semantic Chunking → Output Formats (MD, JSON, HTML, AI Chunks, Knowledge Graph)
```

---

## Tech Stack

| Layer | Technologies |
|-------|--------------|
| Core | Python 3.12, FastAPI, Pydantic, Typer |
| PDF/OCR | PyMuPDF, pdfplumber, PaddleOCR, Docling, LayoutParser |
| AI/LLM | LiteLLM |
| Infrastructure | PostgreSQL, Redis, RabbitMQ |
| DevOps | UV, Ruff, Pytest |

---

## Quick Start

```bash
# Installation (when available)
pip install openparse
```

```python
from openparse import OpenParse

parser = OpenParse()
result = parser.parse("document.pdf")

print(result.markdown)   # Markdown representation
print(result.chunks)     # Semantic chunks for RAG
print(result.tables)     # Extracted tables
```

---

## Roadmap

| Phase | Focus | Status |
|-------|-------|--------|
| Phase 1 | Parsing & Chunking | In Progress |
| Phase 2 | OCR Orchestration & Benchmarking | Planned |
| Phase 3 | Legal/Contract/Financial Parsers | Planned |
| Phase 4 | MCP, LangChain, LlamaIndex Integrations | Planned |
| Phase 5 | Enterprise & Distributed Processing | Planned |

---

## Use Cases

- **RAG Systems** — High-quality chunking for retrieval
- **Legal/Contract Analysis** — Clause extraction, hierarchy preservation
- **Financial Document Processing** — Invoice/report table extraction
- **Knowledge Graph Construction** — Entity/relation extraction from documents
- **Enterprise Document Pipelines** — Scalable, distributed processing

---

## Contributing

Contributions welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## License

Open Source (License TBD)

---

<p align="center"><i>Built for Thanh Khang</i></p>
