# Projet de Reconnaissance Vocale (ASR)

Un système de reconnaissance vocale simple pour identifier les mots "oui", "non", "un" et "deux" en français.

## Structure du projet

- **asr/** - Reconnaissance vocale audio
  - **data/** - Données d'entraînement et de test
  - **models/** - Modèles entraînés
  - **notebooks/** - Jupyter notebooks pour l'exploration et l'entraînement
  - **src/** - Code source Python

## Notebooks

1. **01_Audio_Recording_Test.ipynb** - Test d'enregistrement audio et visualisation
2. **02_Data_Collection.ipynb** - Collection d'exemples de mots prononcés
3. **03_Model_Training.ipynb** - Extraction des caractéristiques et entraînement du modèle

## Fonctionnalités

- Enregistrement audio avec visualisation de la forme d'onde et du spectrogramme
- Extraction de caractéristiques MFCC
- Modèle de classification basé sur un réseau de neurones (MLP)
- Visualisation du pipeline complet (audio → MFCC → classification)

## Prérequis
numpy
scipy
matplotlib
librosa
scikit-learn
sounddevice
soundfile
jupyter
seaborn
tqdm


## Utilisation

1. Créer l'environnement virtuel : `python -m venv env_asr`
2. Activer l'environnement : `env_asr\Scripts\activate`
3. Installer les dépendances : `pip install -r requirements.txt`
4. Exécuter les notebooks dans l'ordre

## Performances (testé avec ma voix)

Le modèle atteint une précision de 75% sur l'ensemble de test avec seulement 32 exemples d'entraînement.

=== Résultats ===
Précision : 3/4 (75%)
[{'actual': 'un', 'predicted': 'un', 'correct': True},
 {'actual': 'deux ', 'predicted': 'deux', 'correct': False},
 {'actual': 'oui', 'predicted': 'oui', 'correct': True},
 {'actual': 'non', 'predicted': 'non', 'correct': True}]
