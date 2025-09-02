# PIVOT-Product-Image-Visual-Query-Optimization-Tool-

# 🧾 Donut Fine-Tuning for Document Understanding (Amazon ML Challenge)

This project fine-tunes the [Donut (Document Understanding Transformer)](https://arxiv.org/abs/2204.06917) model using [LoRA (Low-Rank Adaptation)](https://arxiv.org/abs/2106.09685) on the **Amazon ML Challenge** dataset. It leverages PyTorch Lightning and HuggingFace Transformers for scalable training, with tracking and logging via Weights & Biases (W&B).

---

## 📌 Features

- ✅ **OCR-free document understanding** using Donut.
- ✅ **Parameter-efficient fine-tuning** with LoRA.
- ✅ **Custom dataset loading** from HuggingFace Datasets.
- ✅ **Mixed precision & memory-efficient training** with bitsandbytes.
- ✅ **W&B integration** for logging metrics and visualizations.
- ✅ **Pytorch Lightning** modular pipeline.

---

## 📁 Dataset

- Source: [`Vk333ML/Amazon_ml_challenge_flitered_dataset`](https://huggingface.co/datasets/Vk333ML/Amazon_ml_challenge_flitered_dataset)
- Format: JSON-like documents with image URLs and metadata.
- Loaded via `load_dataset()` from HuggingFace Datasets library.

---

## 🛠️ Setup

### 1. Install Requirements

```bash
pip install -r requirements.txt
```

Requirements include:

- `pytorch-lightning`
- `transformers`
- `datasets`
- `peft` (LoRA)
- `wandb`
- `bitsandbytes`
- `aiohttp` (for async image loading)

### 2. Authenticate with Weights & Biases

```bash
wandb login
```

---

## 🚀 Run Training

```bash
python PIVOT.ipynb  # or run it step-by-step in Jupyter/Colab
```

---

## 🔍 Key Components

### 🧠 Model
- Base: `VisionEncoderDecoderModel` (Donut)
- Fine-tuned using LoRA to reduce training cost and memory.

### 📊 Evaluation
- Edit distance and accuracy metrics on parsed document text.
- Tracked using W&B dashboard.

---

## 🧪 Example Use-Case

- Input: E-commerce product label/image.
- Output: Parsed product info like brand, model, price, and specifications without OCR.

---

## 🤝 Contributors

-Adhyatm Singh

---
