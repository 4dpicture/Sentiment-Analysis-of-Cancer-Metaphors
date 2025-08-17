# Sentiment Analysis of Cancer Metaphors: Comparing Human and Machine Interpretation

This repository contains the resources, code, and documentation for the paper  
**"Sentiment Analysis of Cancer Metaphors: Comparing Human and Machine Interpretation"**, accepted at **HealTAC 2025**.  

---

## 📖 Introduction
Metaphors are pervasive in healthcare discourse, especially in oncology, where they shape how patients articulate personal and clinical experiences of illness. Common metaphors such as:

- ⚔️ *battle*  
- 🥊 *fight*  
- 👹 *enemy*  
- 🛣️ *journey*  
- 🎢 *roller coaster*  
- 💣 *war*  

frame cancer in ways that strongly influence emotions, perceptions, and coping strategies.  

Understanding sentiment embedded in metaphorical language is essential for:  
- 🤝 Enhancing human-computer interaction  
- 💜 Enabling empathic AI systems  
- 🏥 Improving clinical communication  

---

## 🗂 Methods and Data
- **Source**: Narratives were extracted from the [HealthUnlocked](https://healthunlocked.com) platform, focusing on ovarian and prostate cancer communities.  
- **Metaphor filtering**:  
  - ⚔️ *battle*: 2,624  
  - 👹 *enemy*: 336  
  - 🥊 *fight*: 7,250  
  - 🛣️ *journey*: 7,274  
  - 🎢 *roller coaster*: 3,354  
  - 💣 *war*: 714  

- **Models used**:  
  - 🤖 **ChatGPT** – zero-shot sentiment classification  
  - 📉 **RoBERTa** – fine-tuned transformer for sentiment detection  

- **Human annotation**:  
  - 5 annotators (native + non-native English speakers)  
  - Sentiment labels: 😀 *positive*, 😐 *neutral*, 😞 *negative*  
  - Evaluation set: 90 sentences (15 per metaphor)  
  - Agreement measured with **Cohen’s Kappa**  

---

## 📊 Results
- **Human annotators**  
  - Substantial to strong agreement (0.47–0.87) for 🥊 fight, 👹 enemy, 🎢 roller coaster  
  - Moderate to fair agreement (0.39–0.70) for 🛣️ journey, 💣 war, ⚔️ battle  
  - No annotator pair consistently agreed → metaphors are subjective and context-driven.  

- **Machine performance**  
  - 🤖 **ChatGPT**: 😀😐😞 correlations 0.41–0.96 → robust metaphor understanding  
  - 📉 **RoBERTa**:  
    - ⚔️ battle: –0.24 to 0.00 (poor)  
    - 💣 war & 🎢 roller coaster: 0.30–0.69 (fair–moderate)  

**Key takeaway**: Generative models like ChatGPT capture metaphor-driven sentiment better than traditional transformers.

---

