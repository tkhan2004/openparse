# OpenParse - Universal Document Intelligence Platform

## Overview

OpenParse is an **open-source Document Intelligence Platform** designed to transform unstructured documents (PDFs, scanned documents, contracts, invoices, reports, mixed-content files) into structured, AI-ready knowledge. Unlike traditional OCR tools that only extract text, OpenParse preserves hierarchy, tables, diagrams, and semantic relationships.

---

## Problem Statement

Modern AI systems struggle with:
- PDFs, scanned documents, regulations, contracts, invoices, reports
- Mixed-content files with tables, figures, and complex layouts
- Existing tools extract text but **lose structure** (hierarchy, tables, diagrams, cross-references)

---

## Mission

> Enable developers to process any document through a **single API** and receive structured outputs: Markdown, JSON, tables, chunks, metadata, and knowledge representations.

---

## Core Capabilities (9 Modules)

| Capability | Description |
|------------|-------------|
| **Document Classification** | Detects file type, language, scan quality, tables, forms, handwriting, complexity, category |
| **OCR Orchestration** | Supports PaddleOCR, SuryaOCR, Tesseract; confidence scoring, fallback strategies, benchmarking |
| **Layout Analysis** | Identifies headings, paragraphs, lists, tables, figures, footnotes, captions, references, page structure |
| **Structure Recovery** | Reconstructs logical hierarchy: Chapters, Articles, Clauses, Sections, nested content |
| **Table Intelligence** | Extracts tables, reconstructs merged cells, exports to JSON, CSV, Markdown, DataFrames |
| **Image Understanding** | Extracts metadata, OCR from embedded images, chart descriptions |
| **Diagram Understanding** | Extracts diagram nodes/edges, visual relationships for AI retrieval |
| **Semantic Chunking** | Creates hierarchy-aware chunks preserving document structure & context |
| **RAG Optimization** | Optimizes output for retrieval-augmented generation pipelines |

---

## System Architecture

```
Document Analyzer → OCR Engine Manager → Layout Understanding
       ↓                    ↓                    ↓
Structure Recovery → Table Intelligence → Image & Diagram Understanding
       ↓                    ↓                    ↓
         Semantic Chunking → Output Formats (MD, JSON, HTML, AI Chunks, Knowledge Graph)
```

---

## Technology Stack

| Layer | Technologies |
|-------|--------------|
| **Core** | Python 3.12, FastAPI, Pydantic, Typer |
| **PDF/OCR** | PyMuPDF, pdfplumber, PaddleOCR, Docling, LayoutParser |
| **AI/LLM** | LiteLLM |
| **Infrastructure** | PostgreSQL, Redis, RabbitMQ |
| **DevOps** | UV, Ruff, Pytest |

---

## Roadmap

| Phase | Focus | Status |
|-------|-------|--------|
| **Phase 1** | Parsing & Chunking | 🔄 In Progress |
| **Phase 2** | OCR Orchestration & Benchmarking | ⏳ Planned |
| **Phase 3** | Legal/Contract/Financial Parsers | ⏳ Planned |
| **Phase 4** | MCP, LangChain, LlamaIndex Integrations | ⏳ Planned |
| **Phase 5** | Enterprise & Distributed Processing | ⏳ Planned |

---

## Success Metrics

- ✅ High parsing accuracy across document types
- ✅ Low token usage for downstream LLM tasks
- ✅ Benchmark leadership on document understanding tasks
- ✅ Strong open-source adoption & community
- ✅ Production-ready enterprise deployments

---

## Target Use Cases

- **RAG Systems** - High-quality chunking for retrieval
- **Legal/Contract Analysis** - Clause extraction, hierarchy preservation
- **Financial Document Processing** - Invoice/report table extraction
- **Knowledge Graph Construction** - Entity/relation extraction from documents
- **Enterprise Document Pipelines** - Scalable, distributed processing

---

## Getting Started

```bash
# Installation (when available)
pip install openparse

# Basic usage
from openparse import OpenParse

parser = OpenParse()
result = parser.parse("document.pdf")
print(result.markdown)
print(result.chunks)
print(result.tables)
```

---

## License

Open Source (License TBD)

---

## Contributing

Contributions welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

*Generated from OpenParse Product Vision v1.0*