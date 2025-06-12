# 🎓 Yazan Ayyoub – Final Year Project - Multimodal Option Pricing with Deep Learning

This repository implements a modular pipeline for multimodal option price prediction using deep learning techniques. The models integrate macroeconomic indicators, market sentiment, and option-specific features to improve pricing accuracy over traditional methods like Black-Scholes.

> ⚠️ Due to licensing restrictions, raw financial data is **not included** in this repository. A safe, irreversible processed dataset (`inference_eval.csv`) is provided for model evaluation only.

---

## 🧠 Overview

This project explores multimodal neural architectures for option pricing prediction. Several model types are implemented, including:

- Feed-forward networks (FNN)
- LSTMs (unimodal and multimodal)
- Attention-based fusion and cross-attention models
- Black-Scholes benchmark (code included but disabled by default)

The key goal is to evaluate the effectiveness of combining multiple data sources (macroeconomic, sentiment, and option-specific) for improved pricing accuracy.

---

## 📁 Repository Structure

```bash
├── models/              # Pretrained model checkpoints (.pt)
    └── CrossAttention_LSTM.pt
    └── FNN_AllFeatures.pt
    └── LSTM_AttnFusion.pt (chosen)               
├── data/
│   └── inference_eval.csv          # Scaled, processed test set for evaluation
├── scalers/
    └── target_scaler.pkl         # Pre-saved target scaler (feature scalers hidden)
├── Multimodal_Option_Pricing_Workbook.ipynb          # Full training pipeline (data excluded)
├── Inference_Demo_public.ipynb           # Safe model evaluation (runs end-to-end)
├── README.md
```

## 🚀 Getting Started

### Clone the Repository
```bash
git clone https://github.com/yayyzan/Yazan-Ayyoub-FYP.git
cd Yazan-Ayyoub-FYP
```

### Run the script
Run `Inference_Demo.ipynb` book on local CPU or Colab to reproduce results. 

## 📌 Notes on Data

- Raw market and options data are **licensed from OptionMetrics IvyDB USA** and cannot be redistributed.
- All modeling was originally conducted using private datasets.
- The `inference_eval.csv` file contains **processed and scaled data** with only the **target scaler** provided.
- Input scalers and **dates have been excluded** to ensure irreversibility.


## 🧪 Reproducibility

- The training pipeline is available in `Multimodal_Option_Pricing_Workbook.ipynb` but **will not run fully** without the private datasets.
- You may inspect the code for **architecture**, **preprocessing strategy**, and **model design**.
- Model evaluation results shown in the **paper/presentation** can be reproduced using `Inference_Demo.ipynb`.

