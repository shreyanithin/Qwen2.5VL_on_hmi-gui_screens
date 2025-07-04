#  Qwen2.5-VL Evaluation on HMI/GUI Screens

##  Overview

**Qwen2.5-VL** is a powerful vision-language model from Alibaba's DAMO Academy. It combines image and text understanding to perform tasks such as captioning, visual question answering (VQA), and scene reasoning.

This contains a notebook that:

- Installs all required dependencies
- Downloads the model weights automatically from Hugging Face
- Runs multimodal inference on images using Python

---

## Quick Start 

1. [Open the notebook in Google Colab](https://colab.research.google.com/) or Kaggle
2. Set runtime to **GPU**:  
   `Runtime → Change runtime type → GPU`
3. Run the notebook cells in order.

---

##  Dependencies

These will be installed in the first cell:

```bash
pip install git+https://github.com/huggingface/transformers
pip install qwen-vl-utils
pip install Pillow
pip install --upgrade datasets
```

##  Requirements

| Requirement | Details |
|-------------|---------|
| **Python** | 3.11+ |
| **Runtime** | Google Colab or local machine with GPU (≥ 24 GB VRAM recommended) |
| **Internet**| Required to download model from Hugging Face |

##  Dataset

- **Custom dataset** hosted on Hugging Face: [`shreyanithin/hmi-gui-ocr`](https://huggingface.co/datasets/shreyanithin/hmi-gui-ocr)
- **Ground truth** text is stored in a CSV file: `ground truth.csv`

## Metrics Explained

| Metric | Meaning |
|---------------------|---------------------------------------------------|
| **Character Accuracy** | Percentage of matching characters |
| **Word Accuracy** | Word-level fuzzy matching (threshold ≥ 0.8) |
| **CER** | Character Error Rate using `jiwer` |
| **WER** | Word Error Rate using `jiwer` |
