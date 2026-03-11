# 230121 — Advanced Machine Learning Mid-Semester Assignment

**Student:** Eranki Sai Vikas  
**Roll Number:** 230121  
**Paper Reproduced:** Brunner et al. (2012) — *Pairwise Support Vector Machines and their Application to Large Scale Problems* (JMLR)

---

## Structure

```
230121-midsem/
├── partA/
│   ├── brunner12a.pdf          # Paper being reproduced
│   └── llm_usage_partA.json   # LLM disclosure for Part A
│
└── partB/
    ├── task_1_1.ipynb          # Core contribution / architecture
    ├── task_1_2.ipynb          # Key assumptions
    ├── task_1_3.ipynb          # What the paper claims to improve
    ├── task_2_1.ipynb          # Dataset preparation & pair construction
    ├── task_2_2.ipynb          # Implementation of balanced kernel (K_DL)
    ├── task_2_3.ipynb          # Results, comparison table, reproducibility checklist
    ├── task_3_1.ipynb          # Ablation 1: cross-term removal from K_DL
    ├── task_3_2.ipynb          # Ablation 2: PCA dimensionality
    ├── task_3_3.ipynb          # Failure mode analysis
    ├── report.pdf              # 4-page IEEE-format reproduction report
    ├── report.tex              # LaTeX source for the report
    ├── requirements.txt        # Python dependencies
    ├── results/                # All generated plots and figures
    ├── llm_task_1_1.json  )
    ├── llm_task_1_2.json  )
    ├── ...                )    # LLM usage disclosure (one per task)
    └── llm_task_4_2.json  )
```

---

## Setup

```bash
pip install -r partB/requirements.txt
```

## Running the Notebooks

Run in order from the `partB/` directory:

```
task_2_1 → task_2_2 → task_2_3 → task_3_1 → task_3_2 → task_3_3
```

Tasks 1.1, 1.2, 1.3 are written analysis only — no code to run.

All output figures are saved to `partB/results/`.