# Week 8 — Multimodal AI for Research

10 papers downloaded. Two references (ACM FAccT proceedings, SSRN) are available only via publisher portals and listed as link-only at the end.

## 8.1 — What Multimodal AI Can See, Hear, and Read

| File | Citation |
|------|----------|
| `Wang_2024_CharXiv.pdf` | Wang, Z., et al. (2024). CharXiv: Charting Gaps in Realistic Chart Understanding in Multimodal LLMs. [arXiv:2406.18521](https://arxiv.org/abs/2406.18521) |
| `Rahmanzadehgervi_2024_VLMs-Are-Blind.pdf` | Rahmanzadehgervi, P., et al. (2024). Vision Language Models Are Blind: Failing to Translate Detailed Visual Features into Words. *ACCV 2024*. [arXiv:2407.06581](https://arxiv.org/abs/2407.06581) |

## 8.2 — AI and Scientific Images

| File | Citation |
|------|----------|
| `Jin_2024_GPT-4V-Medical.pdf` | Jin, Q., et al. (2024). Hidden flaws behind expert-level accuracy of multimodal GPT-4 vision in medicine. *npj Digital Medicine*. [DOI:10.1038/s41746-024-01185-7](https://doi.org/10.1038/s41746-024-01185-7) — 81.6 % vs 77.8 % physicians, 35.5 % flawed reasoning, ~27 % image comprehension errors. |
| `Mujahid_2024_Malaria-Detection.pdf` | Mujahid, M., et al. (2024). Efficient deep learning-based approach for malaria detection. *Scientific Reports*. [DOI:10.1038/s41598-024-63831-0](https://doi.org/10.1038/s41598-024-63831-0) — 97–99 % on the NIH thin-blood-smear malaria dataset. |

## 8.3 — Document Intelligence

| File | Citation |
|------|----------|
| `Crosilla_2025_Handwritten-Text-Recognition.pdf` | Crosilla, G., Klic, L., & Colavizza, G. (2025). Benchmarking Large Language Models for Handwritten Text Recognition. [arXiv:2503.15195](https://arxiv.org/abs/2503.15195) — GPT-4o ~1.69 % CER on RIMES, 96–98 % CA on IAM/RIMES. **Citation correction:** the lesson previously attributed this to "Humbel et al."; the actual first author is Crosilla. Fixed in `docs/week-8/Document Intelligence.html` and `Week 8/Document Intelligence.html`. |
| `Poznanski_2025_olmOCR-2.pdf` | Poznanski, J., Soldaini, L., et al. (2025). olmOCR 2: Unit Test Rewards for Document OCR. [arXiv:2510.19817](https://arxiv.org/abs/2510.19817) |

## 8.4 — Transcription and Audio Analysis

| File | Citation |
|------|----------|
| `Imam_2025_African-ASR-Survey.pdf` | Imam, S. H., Belay, T. D., et al. (2025). Automatic Speech Recognition (ASR) for African Low-Resource Languages: A Systematic Literature Review. [arXiv:2510.01145](https://arxiv.org/abs/2510.01145) |
| `Nahabwe_2025_African-ASR-Benchmark.pdf` | Nahabwe, A., Kagumire, S., et al. (2025). Benchmarking Automatic Speech Recognition Models for African Languages. *Deep Learning Indaba 2025*. [arXiv:2512.10968](https://arxiv.org/abs/2512.10968) |

## 8.5 — Video and Multimodal Workflows

| File | Citation |
|------|----------|
| `Liu_2024_Lost-in-the-Middle.pdf` | Liu, N. F., Lin, K., Hewitt, J., Paranjape, A., Bevilacqua, M., Petroni, F., & Liang, P. (2024). Lost in the Middle: How Language Models Use Long Contexts. *TACL 2024*. [arXiv:2307.03172](https://arxiv.org/abs/2307.03172) — also at [DOI:10.1162/tacl_a_00638](https://doi.org/10.1162/tacl_a_00638). |

## 8.6 — Hands-On Activities and Assessment

| File | Citation |
|------|----------|
| `COPCOV_2024_PLOS-Medicine.pdf` | (Activity 3 source paper) — COPCOV Investigators (2024). Hydroxychloroquine and chloroquine prophylaxis for COVID-19. *PLOS Medicine*. [DOI:10.1371/journal.pmed.1004428](https://doi.org/10.1371/journal.pmed.1004428) — used as the data source for the Document Extraction activity (Tables 1 and 2). |

## Linked but not redistributed

| Reference | Sub-lesson | Why not |
|-----------|------------|---------|
| Koenecke, A., et al. (2024). Careless Whisper: Speech-to-Text Hallucination Harms. *FAccT '24*. [DOI:10.1145/3630106.3658975](https://doi.org/10.1145/3630106.3658975) | 8.4 | ACM Digital Library doesn't expose a public PDF endpoint; click through to read or use UCT library/ACM Open Access. |
| Friese, S. (2025). From Coding to Conversation: A New Methodological Framework for AI-Assisted Qualitative Analysis. [SSRN:5232579](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5232579) | 8.4 | SSRN bot-protected. |
| OmniDocBench (CVPR 2025). [arXiv:2412.07626](https://arxiv.org/abs/2412.07626) | 8.3 | Mentioned but the v1.6 hard subset was the focus; the original CVPR paper is on arXiv if students want it. *(Could be added in a future commit if useful.)* |

## Citation correction noted

Sub-lesson 8.3 (`Document Intelligence.html`) and the Amathuba source `Week 8/Document Intelligence.html` previously attributed arXiv:2503.15195 to "Humbel et al., 2025". The actual first author is Crosilla; full author list is Crosilla, Klic & Colavizza. Fixed in both source files and noted in CLAUDE.md (lines 273, 325, 329).
