# -FP05-Bridging-the-Digital-Divide-in-Public-Health
 A Comparative Evaluation of Retrieval-Augmented Generation for Universal Health Coverage Intelligence in LMIC Nations
FP05-Bridging-the-Digital-Divide-RAG-PHI/
│
├── README.md                          ← Start here (write this first)
│
├── manuscript/
│   ├── 01_Title_Page_JAMIA_RAG_PHI.docx
│   ├── 02_Main_Manuscript_Final_22May2025.docx
│   ├── 03_Additional_Supplementary_Final.docx
│   └── 04_GRAMMS_APA_JARS_Checklist_Final.docx
│
├── data/
│   ├── knowledge_base/
│   │   └── README_knowledge_base.md   ← Explain WHO SDG docs used; link to WHO sources
│   ├── query_response_logs/
│   │   ├── RAGFlow_Llama32_ConfigA_responses.csv
│   │   ├── RAGFlow_Llama32_ConfigB_responses.csv
│   │   ├── RAGFlow_Gemma3_ConfigA_responses.csv
│   │   ├── RAGFlow_Gemma3_ConfigB_responses.csv
│   │   ├── AnythingLLM_TinyLlama_ConfigA_responses.csv
│   │   └── AnythingLLM_TinyLlama_ConfigB_responses.csv
│   └── coding_sheets/
│       └── InterRater_Coding_Sheet_200pairs.xlsx
│
├── config/
│   ├── system_prompts/
│   │   ├── AnythingLLM_system_prompt.txt
│   │   └── RAGFlow_system_prompt.txt
│   ├── ConfigA_parameters.json
│   └── ConfigB_parameters.json
│
├── docker/
│   ├── RAGFlow_docker_install.sh
│   ├── AnythingLLM_docker_install.sh
│   └── docker-compose.yml
│
├── analysis/
│   ├── ANOVA_factorial_results.xlsx
│   ├── ICC_calculations.xlsx
│   └── CohenD_effect_sizes.xlsx
│
└── checklists/
    ├── GRAMMS_checklist_completed.docx
    └── APA_JARS_Mixed_checklist_completed.docx
