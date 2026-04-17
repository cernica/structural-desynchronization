# Structural Desynchronization in LLM Systems

*Structural Desynchronization in Large Language Model Systems: Probabilistic Boundary Inference as a Security Failure Class*

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19625238.svg)](https://doi.org/10.5281/zenodo.19625238)

---

## Overview

This work introduces **Structural Desynchronization**, a failure mode in LLM-based systems where structured data is reconstructed in a way that diverges from the original input.

As a result, models can produce **fabricated entities** that are treated as real across integrated systems.

---

## Key Idea

LLMs do not operate directly on structured input. Instead, they infer structure probabilistically. Under certain conditions, this inferred structure diverges from the original data representation.

This leads to:

- **Entity inflation** — more records than exist in the input  
- **Boundary collapse** — fields merging across logical records  
- **Authority reassignment** — untrusted data treated as trusted  

---

## Real-World Impact

This behavior was observed in real-world integrations, including:

- Email systems (fabricated messages in summaries)  
- Issue tracking systems (fabricated tickets and states)  

An attacker controlling content within a single data field can influence how entire datasets are interpreted by the model.

---

## Important Clarification

This is **not prompt injection**.

The effect occurs **before instruction following**, at the level of structure reconstruction.

---

## Paper

📄 Full paper:  
https://doi.org/10.5281/zenodo.19625238

---

## Citation

```bibtex
@misc{cernica2026structural,
  author = {Cernica, Ionut Cosmin},
  title = {Structural Desynchronization in LLM Systems},
  year = {2026},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.19625238},
  url = {https://doi.org/10.5281/zenodo.19625238}
}
