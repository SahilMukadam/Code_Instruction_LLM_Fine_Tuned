# 🧠 Mini GitHub Copilot — Instruction-to-Code Fine‑Tuning Project

Fine‑tune a small language model (TinyLlama‑1.1B or Phi‑2) on instruction–code pairs so it can generate code from natural‑language descriptions.  
The goal is to build a lightweight, local version of GitHub Copilot while learning the full fine‑tuning pipeline:

- Data preparation  
- Tokenization  
- LoRA / QLoRA configuration  
- Training  
- Evaluation  
- Model comparison  

---

## ⚙️ Tech Stack Overview

| **Component** | **Technology** | **Why** |
|--------------|----------------|---------|
| **Base Model** | TinyLlama‑1.1B (local) + CodeLlama‑7B (Colab) | TinyLlama fits on a GTX 1650; CodeLlama runs on free Colab T4 |
| **Fine‑tuning** | PEFT (LoRA / QLoRA) + HuggingFace Transformers | Parameter‑efficient fine‑tuning with low VRAM requirements |
| **Dataset** | Code Alpaca + CodeSearchNet (HuggingFace Datasets) | High‑quality instruction–code pairs, free and well‑structured |
| **Training Framework** | PyTorch + HuggingFace Trainer | Hands‑on PyTorch fundamentals with a stable training loop |
| **Experiment Tracking** | Weights & Biases (W&B) | Industry standard; free tier is more than enough |
| **Evaluation** | HumanEval (pass@k) + custom test cases | Standard benchmark for code generation |
