# Test technique pour le stage data science chez Bouygues Telecom

<div style="text-align: right;"><span style="font-style: italic; margin-right: 1.5em;">Gabriel Watkinson</span></div>
<hr class="solid">

Ce repo contient le test technique pour le stage de data science chez Bouygues Telecom basée sur des données factices sur la résiliation des clients ayant un abonnement télécom. Le contenu du test se situe dans le notebook `test-technique-gwatkinson.ipynb`.

Pour relancer le notebook, il suffit d'installer les dépendances avec `poetry install` (idéalement dans un environnement virtuel avec python 3.9.9) et d'ajouter les données dans un dossier `data` dans la racine du projet.

## Description du test

L'objectif est de comprendre et de prédire la résilation des clients. Pour ce faire 4 datasets sont fournis :

* resiliation_option : contient les données sur les options des forfaits fixe et mobile des clients
* resiliation_client : contient des données clients
* resiliation_contrat : contient les caractéristiques des contrats des clients
* resiliation_forfait : contient les caractéristiques du forfait mobile du client

## Organisation du notebook

Le notebook est composé de 3 parties et d'une conclusion :

1. Analyses des données et statistiques descriptives
2. Préparation de données
3. Modélisation du problème
