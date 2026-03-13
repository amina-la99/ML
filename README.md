# ML
**Prédiction de la sévérité des effets indésirables 
médicamenteux par Deep Learning**

---

## 📋 Description

Modèle LSTM pour prédire la sévérité des effets 
indésirables médicamenteux sur 10 jours de suivi patient.
4 niveaux de sévérité : None · Mild · Moderate · Severe

---

## 🏗️ Architecture du modèle

- LSTM 128 → Dropout 0.4 → LSTM 64 → TimeDistributed Dense
- Focal Loss custom pour classes déséquilibrées
- Oversampling des cas sévères (factor=4)

---

## ⚙️ Pipeline complet

1. Génération et équilibrage du dataset synthétique
2. One-hot encoding des médicaments
3. Regroupement en séquences temporelles (10 jours)
4. Entraînement LSTM avec Early Stopping
5. Évaluation par jour + Matrice de confusion
6. Interface NLP : texte patient → prédiction
7. Interface Gradio patient + médecin

---

## 🛠️ Stack

Python · TensorFlow/Keras · scikit-learn
Pandas · NumPy · Gradio · Seaborn

---

## 🎯 Interfaces

**Interface Patient** — saisie des symptômes en texte libre
**Interface Médecin** — historique sur 10 jours par patient

