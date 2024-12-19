# Examen BentoML

## Fonctionnement du projet

Ce projet utilise BentoML pour déployer un modèle de machine learning. Ce modèle a pour but de prédire la chance d'admission d'un étudiant dans une université.

## Architecture du projet

1. **Entraînement du modèle**: Les modèles de machine learning sont entraînés en utilisant la librarie scikit-learn.
2. **Enregistrement du modèle**: Les modèles entraînés sont enregistrés dans un format compatible avec BentoML.
3. **Création du service BentoML**: Un service BentoML est créé en définissant une classe qui hérite de `bentoml.Service`. Cette classe spécifie les artefacts du modèle et les API de prédiction.
4. **Déploiement**: Le service BentoML est conteneurisé et déployé sur une infrastructure cloud ou sur des serveurs locaux.
5. **Prédiction**: Les utilisateurs peuvent envoyer des requêtes HTTP au service déployé pour obtenir des prédictions en temps réel.

## Fichiers principaux

- `prepare_date.py`: Script pour charger les données, de les nettoyer et de les diviser en un jeu d'entraînement et un jeu de test.
- `service.py`: Définition du service BentoML et des API de prédiction.
- `Dockerfile`: Fichier pour créer l'image Docker du service.
- `README.md`: Documentation du projet.

