# 📝 Burmese Grammar Error Correction — Deep Learning Model

- Built an end-to-end seq2seq pipeline for Burmese grammatical error correction
- Created a training dataset using academic grammar rules, AI-generated synthetic pairs, and manual validation
- Fine-tuned and compared three transformer models (mT5-base, mBART-50, ByT5-small) across multiple epochs

---

## ✨ Highlights
- Focused on **Burmese (Myanmar) language**, addressing a critical NLP gap  
- Designed to process real error-annotated Burmese text (testdata.csv) and correct grammar with minimal human intervention  
- Delivered a usable proof‐of‐concept that can be extended into language tools for education, editing or localisation  

---
## 📊 Model Performance (BLEU on Test Set)

| Model          | Trend Summary                             | Best Observed BLEU (≈ from plot) |
|----------------|--------------------------------------------|----------------------------------|
| **mBART-50**   | Strong from early epochs, stable plateau   | **≈ 82–85** ⭐ Best overall |
| **mT5-base**   | Peaks early (~80) then degrades with more epochs | ≈ 70–80 |
| **ByT5-small** | Improves steadily with longer training     | ≈ 75 |

> **mBART-50 achieved the strongest and most stable BLEU performance**, making it the best candidate for downstream deployment.

---
## 🧠 What I Learned
- mBART-50’s multilingual denoising objective gives it a real advantage on Burmese GEC
- More epochs do not guarantee gains — mT5 degraded past peak BLEU
- Byte-level models like ByT5 are competitive even without tokenization
---
<details>
<summary>📚 Data Sources & Ethical Considerations</summary>

- **Data:** Includes Burmese error-annotated sentences (input) and corrected ground-truth (output).  
- **Languages & Biases:** The model is trained on specific text sources; performance may vary on other domains.  
- **Usage Warning:** This is a research prototype and **not** suited for high-stakes or fully autonomous editing systems without further validation.

</details>

<details>
<summary>🚀 Future Directions</summary>

- Deploy a **simple web UI** or editing plugin for Burmese grammar correction  
- Experiment with **multilingual training** (Burmese + related languages)  
- Add **explainability** (highlight corrected spans) to support human reviewers  
- Develop a **light-weight mobile model** for on-device correction  

</details>

---

⭐ ***Techstack: Python, PyTorch (HuggingFace Transformers).***
