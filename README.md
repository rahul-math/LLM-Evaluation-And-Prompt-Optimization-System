# 🧠 LLM Evaluation & Prompt Optimization System

## 📌 Overview

This project implements a system to evaluate and optimize Large Language Model (LLM) responses across different prompt strategies. It compares outputs using quantitative metrics and improves prompt quality through iterative optimization.

The system evaluates multiple models and demonstrates how prompt engineering strategies impact performance.

---

## 🎯 Objectives

* Evaluate LLM responses across multiple prompts
* Compare outputs using measurable metrics
* Optimize prompts systematically
* Analyze performance across models and strategies
* Identify best-performing prompt strategies

---

## ⚙️ Models Used

* **llama3.2:3b** → Robust and consistent performance
* **gemma2:270m (gemma3)** → Lightweight, high peak performance
* **llama3** → Used for prompt optimization

---

## 🔁 System Workflow

### 1. Iteration 1 — Original Prompts

* Raw prompts from dataset
* Baseline evaluation

### 2. Iteration 2 — LLM-Optimized Prompts

* Prompts improved using LLM (llama3)
* Focus on clarity and structure

### 3. Iteration 3 — Score-Optimized Prompts

* Prompts aligned with evaluation metrics
* Enforces concise, precise responses

---

## 📊 Evaluation Metrics

* **BERTScore** → Semantic similarity
* **ROUGE-L** → Text overlap
* **Embedding Similarity** → Cosine similarity

### Final Score:

```math
Final Score = 0.4 × BERTScore + 0.3 × Embedding + 0.3 × ROUGE
```

---

## 📁 Dataset Format

| Column      | Description     |
| ----------- | --------------- |
| prompt      | Input query     |
| prompt_type | Type of prompt  |
| reference   | Expected answer |

---

## 🚀 Installation

```bash
pip install pandas tqdm requests matplotlib evaluate sentence-transformers scikit-learn rouge-score sacrebleu bert-score
```

---

## ▶️ Usage

1. Start Ollama server
2. Update API URL:

```python
OLLAMA_URL = "your_url_here"
```

3. Run pipeline:

* Iteration 1 → Original
* Iteration 2 → Optimized
* Iteration 3 → Score-Optimized

4. Outputs:

* `before_results.csv`
* `after_results.csv`
* `score_results.csv`

---

## 📊 Visualizations

* Model performance comparison
* Prompt strategy comparison
* Improvement distribution
* Leaderboard ranking

---

## 🏆 Key Results

### 🔥 Best Configuration (Peak Performance)

* **Model:** gemma3
* **Prompt Type:** basic
* **Strategy:** Score_Optimized
* **Score:** 0.6785

👉 Indicates that gemma performs best under optimized, task-specific conditions.

---

### 📊 Model Robustness (Average Performance Across Strategies)

```
gemma3      → 0.5559
llama3.2    → 0.6012  ✅
```

### 🏆 Most Robust Model:

* **llama3.2**

👉 Indicates that llama3.2 performs consistently well across all prompt strategies.

---

## ⚖️ Final Interpretation

* **gemma3** → Best for optimized scenarios (highest peak score)
* **llama3.2** → Best for general robustness and consistency

This highlights that model selection depends on the use case:

* Use **gemma3** when prompts are well-optimized
* Use **llama3.2** for stable, general-purpose performance

---

## 🧠 Key Insights

* Prompt optimization must align with evaluation metrics
* Verbose answers can reduce similarity-based scores
* Concise prompts improve quantitative evaluation
* Different models respond differently to prompt changes
* Robustness and peak performance are distinct evaluation criteria

---

## 🔮 Future Improvements

* LLM-as-a-judge evaluation
* Streamlit dashboard
* Multi-round prompt optimization
* Support additional models

---

## 📌 Author

Rahul S Math

---

## ⭐ If you found this useful, give it a star!
