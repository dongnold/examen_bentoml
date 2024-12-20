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

## Instructions pour lancer le projet

1. Mettez-vous dans le dossier du projet
cd examen_bentoml

2. Executer la commande suivante pour créer l'environnement virtuel:
virtualenv bentomlenv

3. source bentomlenv/bin/activate

4. pip3 install -r requirements.txt

5. bentoml build

6. bentoml containerize lr_service:latest

7. docker run --rm -p 3000:3000 lr_service:<tag>

8. python src/test.py



