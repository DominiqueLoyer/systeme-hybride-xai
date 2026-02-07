# 🔬 Système Hybride XAI

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)](https://flask.palletsprojects.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![SysCRED](https://img.shields.io/badge/Integrated_in-SysCRED-blue)](https://github.com/DominiqueLoyer/systemFactChecking)
**Backend Flask pour système hybride de vérification de crédibilité avec Explainable AI (XAI)**

PhD Research - Dominique S. Loyer | UQAM

---

## 📋 Overview

Système hybride combinant approches symboliques et neuronales pour la vérification de crédibilité informationnelle avec capacités d'explicabilité (XAI):

- **Backend Flask**: API REST pour l'évaluation de crédibilité
- **Interface Web**: Frontend HTML/CSS/JS interactif
- **Documentation XAI**: Stratégie d'explicabilité des décisions
- **Neuro-symbolique**: Fusion règles OWL + modèles Transformers

---

## 🚀 Quick Start

### Installation

```bash
git clone https://github.com/DominiqueLoyer/systeme-hybride-xai.git
cd systeme-hybride-xai

# Installer les dépendances
pip install flask

# Lancer le serveur
python backend_flask.py
```

### Accès

Le serveur démarre sur `http://localhost:5000`

---

## 📁 Project Structure

```
systeme-hybride-xai/
├── README.md                           # Ce fichier
├── backend_flask.py                    # ⭐ Serveur Flask principal
├── Copie de Backend Flask_app.py       # Version alternative
├── backend_7juin25.html                # Interface web
├── interface806.html                   # Interface alternative
└── Analyse et Stratégie XAI...         # Documentation XAI
```

---

## 📡 API Endpoints

| Endpoint | Méthode | Description |
|----------|---------|-------------|
| `/api/verify` | POST | Vérification de crédibilité |
| `/api/health` | GET | État du serveur |
| `/api/explain` | POST | Explicabilité XAI |

### Exemple Request

```bash
curl -X POST http://localhost:5000/api/verify \
  -H "Content-Type: application/json" \
  -d '{"input_data": "https://www.exemple.com/article"}'
```

### Exemple Response

```json
{
  "scoreCredibilite": 0.75,
  "niveauCredibilite": "HIGH",
  "explanation": {
    "factors": ["source_reputation", "content_analysis"],
    "weights": [0.4, 0.6]
  }
}
```

---

## 🔧 Architecture XAI

Le système utilise une approche hybride pour l'explicabilité:

1. **Règles symboliques**: Ontologie OWL pour les règles de base
2. **Attention Weights**: Visualisation des poids d'attention Transformer
3. **LIME/SHAP**: Explicabilité locale des prédictions

---

## 🏷️ Citation

```bibtex
@software{loyer2025hybride,
  author = {Loyer, Dominique S.},
  title = {Système Hybride XAI: Neuro-Symbolic Credibility Verification},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/DominiqueLoyer/systeme-hybride-xai}
}
```

---

## 📜 License

MIT License
