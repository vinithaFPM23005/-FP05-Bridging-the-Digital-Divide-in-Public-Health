# Bridging the Digital Divide in Public Health

**A Comparative Evaluation of Retrieval-Augmented Generation for 
Universal Health Coverage Intelligence in LMIC Nations**

**Journal:** Journal of the American Medical Informatics Association (JAMIA)  
**Submission Date:** May -June 2025  
**Authors:** Vinitha T, Prof. Ashok Kumar Harnal  
**Institution:** FORE School of Management, New Delhi  
**ORCID (Vinitha T):** 0000-0002-5162-0678  
**ORCID (Prof. Harnal):** 0009-0002-1860-7444  

---

## Repository Contents

| Folder | Contents |
|--------|----------|
| Title page /', Title page with Authors Details, CRedit Authorship Details |
|`manuscript/` | , main manuscript (v16, 22 May 2025), supplementary, checklists |
| `appendix/` | System prompt specifications (Appendix 1) |
| `data/` | Query-response logs (CSV); knowledge base document index |
| `config/` | Full parameter files for Config A and Config B (RAGFlow + AnythingLLM) |
| `docker/` | Docker installation scripts for full reproducibility |
| `figures/` | All manuscript figures (high-resolution TIFF 300 /600 DPI) |
| 'Additional Supplementary/' | Details of PRISMA Framework, Concetual Theoretical Analysis, Experimental analysis, Statistical Analysis, and reproducbility | 

---

## Study Overview

This study evaluates two open-source RAG platforms (AnythingLLM; RAGFlow) 
across two language models (Llama 3.2 3B; Gemma 3 27B) and two parameter 
configurations using 200 query-response pairs drawn from WHO SDG documents 
(2005–2025).

**Key Finding:** Restrictive configuration (Config B) reduced hallucination 
by 62.5% for RAGFlow/Llama 3.2 (Cohen's d = 0.89; F[1,7992] = 384.2, 
p < .001; η² = 0.046).

**Primary Contribution:** The RAG-PHI governance framework — a three-layer 
empirically-grounded framework for responsible RAG deployment in LMIC 
health systems.

---

## Experimental Configuration Summary

| Parameter | Config A (Permissive) | Config B (Restrictive) |
|-----------|----------------------|----------------------|
| Temperature | 0.8 | 0.0 |
| Similarity Threshold | 0.2 | 0.75 |
| Top N Retrieval | 10 | 1 |
| Top P | 1.0 | 0.1 |
| Presence Penalty | 0.2 | 0.0 |
| Frequency Penalty | 0.3 | 0.0 |
| Max Tokens | 20,000 | 20,000 |

---

## Hardware & Software

- **Processor:** AMD EPYC 7502P (32 cores)  
- **GPU:** NVIDIA A100 40 GB  
- **RAM:** 128 GB DDR4 ECC  
- **OS:** Ubuntu 22.04 LTS  
- **Docker:** 24.0.5  
- **Model Serving:** Ollama 0.1.23  
- **Platforms:** RAGFlow | AnythingLLM  

See `docker/INSTALL.md` for full setup instructions.

---

## Knowledge Base

- **Source:** WHO SDG monitoring reports + UHC publications + MOHFW/NHM 
  technical reports (2005–2025)  
- **Size:** 21,629 overlapping segments  
- **Chunking:** ~1,000 tokens with 20% overlap  
- **Note:** Raw WHO documents are publicly available at who.int. 
  The file index is provided in `data/knowledge_base/KB_Document_Index.csv`

---

## Ethical Statement

This study is exempt from IRB oversight. All data are publicly available 
WHO SDG monitoring documents. No personally identifiable information was 
collected or processed. All models ran locally — no data was transmitted 
to external servers.

---

## Citation

> Vinitha T, Harnal AK. Bridging the Digital Divide in Public Health: 
> A Comparative Evaluation of Retrieval-Augmented Generation for Universal 
> Health Coverage Intelligence in LMIC Nations. *Journal of the American 
> Medical Informatics Association*. 2025 [Under Review].

---

## Checklist Compliance

| Standard | Status |
|----------|--------|
| GRAMMS (O'Cathain et al., 2008) | ✓ All 6 criteria met |
| APA JARS-Mixed (2020) | ✓ All items 1a–7a addressed |
| PRISMA 2020 | ✓ n=335 identified; n=20 included |
| JAMIA AI Use Policy | ✓ Gemini AI declared (figures only) |

---

*This repository is maintained for transparency and reproducibility 
per JAMIA data availability requirements.*
