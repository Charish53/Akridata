Got it 👍 — I’ll simplify and keep it professional, without over-claiming results you haven’t shown yet. Here’s a **cleaner README**:

---

# 🍫 Hazelnut Defect Classification with CLIP

> Zero-shot classification of hazelnut defects using OpenAI’s CLIP.
> Extended from simple anomaly detection (good vs defective) to **fine-grained defect classification** with natural-language prompts.

---

## 🚀 Overview

This project demonstrates how to use **CLIP** for classifying hazelnuts into *good* and multiple defect categories **without retraining**.
The approach uses:

* A **two-stage pipeline**: first detect good vs defective, then identify defect type.
* **Prompt ensembling** for robust text embeddings.
* **Test-time augmentation** (horizontal flip).
* A **config-driven design** for easy extension.

---

## 🛠 Features

* ✅ Zero-shot defect classification (no extra training).
* ✅ Filename → label extraction with synonyms.
* ✅ Configurable class names and prompts in `spec.py`.
* ✅ Works with CLIP backbones like `ViT-B/32` (default).
* ✅ Outputs `y_true` and `y_pred` for evaluation.

---

## 📂 Project Structure

```
├── clip_ac.py        # Main classification pipeline
├── spec.py           # Config with classes, prompts, and model
├── data/             # Hazelnut images (good + defective)
└── README.md         # Project documentation
```

---

## 📊 Classes

* **good** – no defects
* **crack** – fracture on the shell
* **cut** – sliced shell
* **hole** – perforation
* **print** – printed or stamped text

---

## ⚡ Quick Start

```bash
# Install dependencies
pip install torch torchvision ftfy regex tqdm pydantic git+https://github.com/openai/CLIP.git

# Run classification
python clip_ac.py --test_dir ./data/hazelnuts --tau 0.65
```

---

## 🔮 Extending the Project

* Add new defect types by updating `spec.py`.
* Try larger CLIP backbones (e.g., `ViT-L/14`).
* Apply the pipeline to other anomaly detection datasets.

---

## 👨‍💻 Author

Built with ❤️ using CLIP for **hazelnut defect classification**.

---

Do you want me to also add some **badges** (like Python version, license, dependencies) to make the top of the README look even more GitHub-ready?

