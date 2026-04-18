# Bidirectional Textless Speech-to-Speech Translation for Rural Clinical Diagnostics

**Team Members:** Mugilan M, Surbhi Shukla, Khushi Bhardwaj, Avanti Mittal, Shreyash Kadam  
**Institution:** Indian Institute of Technology (IIT) Jodhpur

## 📌 Project Overview
This project introduces a bidirectional, completely textless Speech-to-Speech Translation (S2ST) framework optimized for Bhojpuri-Hindi clinical interactions. By bypassing intermediate text transcription (ASR-MT-TTS), we map discrete 256-dimensional HuBERT-soft units directly across linguistic domains using a modified T5-Small transformer and Low-Rank Adaptation (LoRA).

**Key Achievements:**
* **RTF:** 0.291 (3.4x speedup over cascaded baselines)
* **Convergence:** 0.1642 MSE (Optimized via 5-epoch LoRA early stopping)
* **Safety:** Eliminates medical hallucinations in favor of safe phonetic distortion.

## 🚀 Reproducibility & Execution

All experiments, model training, and evaluation scripts have been consolidated into a single Jupyter Notebook (`master_pipeline_s2s.ipynb`) for ease of execution and sequential readability.

### ⚠️ Important Cloud Setup (Google Colab)
To avoid permission errors, reviewers evaluating this notebook in Google Colab must configure their own environment before running the cells:

1. **Hugging Face Token (`HF_TOKEN`):** The notebook requires authenticated access to Hugging Face models. Add your personal Hugging Face access token to your Colab **Secrets** (the key icon on the left sidebar) and name it `HF_TOKEN`. Ensure the "Notebook access" toggle is enabled.
2. **Google Drive Mounting:** The script saves and loads LoRA weights from Google Drive. When the notebook prompts for Drive access, please authorize it to mount **your own** Google Drive. 
3. **Path Configuration:** Update the `base_path` or save directory variables in the notebook (if applicable) to point to a valid folder within your own Drive environment.

### Local Execution (Alternative)
If you prefer to run the project locally rather than on Colab:

1. Clone this repository:
   ```bash
   git clone [https://github.com/your-username/m25de1022_m25de1018_b22ai026_b22es021_m25de1016.git](https://github.com/Mugil6/m25de1022_m25de1018_b22ai026_b22es021_m25de1016.git)
   cd m25de1022_m25de1018_b22ai026_b22es021_m25de1016
2. Create a virtual environment and install dependencies:

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt

Running the Project:
1. Launch Jupyter Notebook:
   jupyter notebook

2. Open master_pipeline_s2s.ipynb

3. Run all cells sequentially.

📜 License
Copyright (c) 2026 Mugilan M, Surbhi Shukla, Khushi Bhardwaj, Avanti Mittal, Shreyash Kadam.
All Rights Reserved.

This code and associated documentation are proprietary and confidential. No part of this repository may be reproduced, distributed, or transmitted in any form or by any means, including photocopying, recording, or other electronic or mechanical methods, without the prior written permission of the authors