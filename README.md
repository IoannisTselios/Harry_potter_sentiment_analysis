# Harry Potter Sentiment Analysis & Social Networks 🎭📊

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=YELLOW)] [![NetworkX](https://img.shields.io/badge/NetworkX-00A1D6?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTIiIGhlaWdodD0iMTIiPjwvc3ZnPg==)] [![NLTK](https://img.shields.io/badge/NLTK-FF6F00?style=for-the-badge&logo=nltk&logoColor=white)] [![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)]

## 🎯 Project Overview
**Can we predict if Harry Potter characters are friends or enemies using NLP?** 

This **DTU research project** combines **Network Analysis** + **Sentiment Analysis** to map character relationships across all 7 Harry Potter books. We built character interaction networks (edges = co-appearing in sentences) weighted by sentence sentiment scores.

**My contributions (Ioannis Tselios):**
- ✅ **Character dataset creation** (557 characters with attributes)
- ✅ **Network construction** for all 7 books using NLTK NER
- ✅ **Community detection** (Louvain algorithm)
- ✅ **Web scraping** (Harry Potter Fandom + spells dataset)

**Key findings:** Sentiment scores cluster tightly (~5.3) making friend/foe prediction inconclusive, but networks reveal realistic social structures!

---

## 🚀 Features
- 📚 **Full Harry Potter analysis** (6.67MB text, all 7 books)
- 🌐 **Character networks** (77-342 nodes per book) 
- 😊 **Sentence-level sentiment** weighting edges
- 👥 **Community detection** (Quidditch teams, Death Eaters)
- ☁️ **Word clouds** (TF-IDF per book)
- 🪄 **Spell frequency analysis**
- 🔍 **NER + name mapping** for 557 characters

## 📈 Results Highlights
🔬 First 3 books: Hogwarts-focused (small networks)
🏆 Book 4+: Triwizard → Death Eaters → Ministry communities
⚡ Voldemort communities appear Books 4-7 only
📊 Top connected: Harry, Ron, Hermione, Dumbledore, Snape, Hagrid
❌ Sentiment: No friend/foe distinction (all ~5.3)


![Network Example](https://github.com/IoannisTselios/Harry_potter_sentiment_analysis/raw/main/images/network_chamber_secrets.png)
*Harry Potter & Chamber of Secrets network (77 nodes, 342 edges)* [file:96]

---

## 🛠️ Tech Stack
```python
# Core pipeline
NLTK (NER) → NetworkX (graphs) → Louvain (communities) 
→ Scikit-learn (TF-IDF) → Sentiment dataset (10K words)
BeautifulSoup (scraping)

📁 Repository Structure
Harry_potter_sentiment_analysis/
├── data/
│   ├── books/           # 7 Harry Potter txt files
│   ├── characters.csv   # 557 characters + attributes
│   └── spells.csv
├── notebooks/
│   ├── 01_data_prep.ipynb
│   ├── 02_networks.ipynb
│   ├── 03_sentiment.ipynb
│   └── 04_wordclouds.ipynb
├── src/
│   ├── ner_mapping.py
│   ├── network_builder.py
│   └── sentiment.py
└── images/
    └── networks/        # Book network visualizations
    └── wordclouds/


🚀 Quick Start
# 1. Clone repo
git clone https://github.com/IoannisTselios/Harry_potter_sentiment_analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run analysis notebooks sequentially
jupyter notebook notebooks/01_data_prep.ipynb
