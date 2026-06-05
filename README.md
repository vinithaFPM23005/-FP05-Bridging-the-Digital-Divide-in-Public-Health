# Bridging the Digital Divide in Public Health:A Comparative Evaluation of Retrieval-Augmented Generation for Universal Health Coverage Intelligence in LMIC Nations**

# Journal: Journal of the American Medical Informatics Association (JAMIA)
# Submission Date: May–June 2025
# Authors: Vinitha T, Prof. Ashok Kumar Harnal
# Institution: FORE School of Management, New Delhi
# ORCID (Vinitha T): 0000-0002-5162-0678
# ORCID (Prof. Harnal): 0009-0002-1860-7444
---
# Repository Contents
| title_page/Final title page including author details, affiliations, and CRediT authorship contributions|
| manuscript/Main manuscript (final revised version), abstract, supplementary files, and reporting checklists|
| appendix/ Appendix materials including system prompt specifications (Appendix 1)|
| data/ Query–response logs (CSV) and knowledge base document index |
| config/ Full parameter configurations for Config A (permissive) and Config B (restrictive) across RAGFlow and AnythingLLM |
| docker/ Docker scripts and environment setup files for full reproducibility (see INSTALL.md) | 
| figures/ All manuscript figures in high-resolution TIFF format (300/600 DPI) |
| Additional_Supplementary/ Detailed PRISMA framework, conceptual and theoretical analysis, experimental design, statistical outputs, and reproducibility documentation |

# Study Overview
This study evaluates two open-source Retrieval-Augmented Generation (RAG) platforms (AnythingLLM and RAGFlow) across two language models (Llama 3.2 3B and Gemma 3 27B) and two parameter configurations. The evaluation is based on 200 query–response pairs derived from WHO SDG documents (2005–2025).

# Key finding: 
Restrictive configuration (Config B) reduced hallucination by 62.5% for RAGFlow with Llama 3.2 (Cohen’s d = 0.89; F = 384.2, p < 0.001; η² = 0.046).

# Primary contribution: 
The RAG-PHI governance framework, a three-layer empirically grounded framework for responsible RAG deployment in LMIC health systems.

# Experimental Configuration
  Config A (Permissive) vs Config B (Restrictive):
  | Parameter | Config A (Permissive) | Config B (Restrictive) |
|-----------|----------------------|----------------------|
| Temperature | 0.8 | 0.0 |
| Similarity Threshold | 0.2 | 0.75 |
| Top N Retrieval | 10 | 1 |
| Top P | 1.0 | 0.1 |
| Presence Penalty | 0.2 | 0.0 |
| Frequency Penalty | 0.3 | 0.0 |
| Max Tokens | 20,000 | 20,000 |

# Hardware and Software
- **Processor:** AMD EPYC 7502P (32 cores)  
- **GPU:** NVIDIA A100 40 GB  
- **RAM:** 128 GB DDR4 ECC  
- **OS:** Ubuntu 22.04 LTS  
- **Docker:** 24.0.5  
- **Model Serving:** Ollama 0.1.23  
- **Platforms:** RAGFlow | AnythingLLM  

Refer to docker/INSTALL.md for full setup and replication instructions.

# Knowledge Base
- **Source:** WHO SDG monitoring reports + UHC publications + MOHFW/NHM 
  technical reports (2005–2025)  
- **Size:** 21,629 overlapping segments  
- **Chunking:** ~1,000 tokens with 20% overlap  
- **Note:** Raw WHO documents are publicly available at who.int. 
  The file index is provided in `data/knowledge_base/KB_Document_Index.csv`

---

# Note: Source documents are publicly available via WHO (who.int). The indexed file list is provided in data/knowledge_base/KB_Document_Index.csv

---
# Ethical Statement
This study is exempt from institutional review board (IRB) oversight. All data sources are publicly available and contain no personally identifiable information. All models were executed locally, and no data was transmitted to external servers.
---
# Citation
Vinitha T, Harnal AK. Bridging the Digital Divide in Public Health: A Comparative Evaluation of Retrieval-Augmented Generation for Universal Health Coverage Intelligence in LMIC Nations. Journal of the American Medical Informatics Association. 2025 (under review).
---
# Checklist Compliance
GRAMMS (O’Cathain et al., 2008): All criteria satisfied
APA JARS-Mixed Methods (2020): All required items addressed
PRISMA 2020: 335 records identified; 20 studies included
JAMIA AI Use Policy | ✓ Gemini AI declared (figures only) |

# JAMIA AI Policy: AI tool (Gemini) used only for figure visualization and fully disclosed

*This repository is maintained for transparency and reproducibility 
per JAMIA data availability requirements.*
