# Installation Instructions for Reproducibility

## Prerequisites
- Ubuntu 22.04 LTS
- Docker 24.0.5+
- NVIDIA A100 GPU (or equivalent with 40 GB VRAM for Gemma 3 27B)
- 128 GB RAM minimum

## Step 1: Install Ollama
```bash
curl -fsSL https://ollama.com/install.sh | sh
ollama pull llama3.2:3b
ollama pull gemma3:27b
ollama pull tinyllama
```

## Step 2: Launch RAGFlow
```bash
docker-compose -f docker-compose-ragflow.yml up -d
# Access at http://localhost:9380
```

## Step 3: Launch AnythingLLM
```bash
docker-compose -f docker-compose-anythingllm.yml up -d
# Access at http://localhost:3001
```

## Step 4: Load Knowledge Base
- Upload WHO SDG documents to each platform
- Apply chunking: 1,000 tokens, 20% overlap
- Verify vector count: 21,629 segments

## Step 5: Apply System Prompts
See `../appendix/Appendix1_System_Prompts_RAG_PHI.docx`

## Step 6: Apply Configuration
Import JSON files from `../config/` directory into each platform's settings panel.
