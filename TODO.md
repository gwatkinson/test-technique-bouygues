# TODO LIST

* [ ] Faire une image Docker pour partager le contenu de ce projet. Il faut :
  * [ ] Créer un Dockerfile avec la bonne version de `Python` (3.9.9) (et `poetry` ?)
  * [ ] Y copier ou monter les fichiers du projet (de github et les données, pas le venv, ...)
  * [ ] Installer les dépendances avec `poetry`
  * [ ] Executer le notebook avec `nbconvert --exec` (À vérifier)
  * [ ] Exposer le port du notebook (8888) pour voir le notebook
* [ ] Réaliser les 3 parties du projets :
  * [ ] Statistiques descriptives
    * [ ] Utiliser pandas profiling (labeliser les variables binaires avant ?)
    * [ ] Faire des commentaires pertinents sur les bases de données
      * [ ] Par exemple, sur l'ancienneté, sur les valeurs manquantes
    * [ ] Faire des graphiques (histogrammes, boxplots, matrice de corrélation, ...)
    * [ ] Utiliser missingno pour visualiser les données manquantes
  * [ ] Préparation de données
    * [ ] Joindre les bases avec l'id_client
    * [ ] Ajouter la quantité de go pour chaque forfait
    * [ ] Remplir les valeurs manquantes
      * [ ] forfait -> imputer le nb de go ?
      * [ ] genre, parent
      * [ ] Utiliser différent imputers
      * [ ] Essayer en enlevant certaines valeurs manquantes
    * [ ] Utiliser sklearn-pandas ?
  * [ ] Modélisation avec métrique de votre choix
    * [ ] Choisir la target (résiliation ou non)
    * [ ] Faire un dummy model pour avoir une base de comparaison
    * [ ] Tester different modeles de classification :
      * [ ] Regression logistique
      * [ ] Random Forest
      * [ ] Decision Tree
      * [ ] SVM
      * [ ] KNN
      * [ ] Naive Bayes
      * [ ] XGBoost
      * [ ] LightGBM
      * [ ] CatBoost
      * [ ] Autres ?
    * [ ] Reflechir à normalisation ou non
    * [ ] Comment utiliser les variables catégorielles ?
      * [ ] `methode_paiement`
      * [ ] `contrat`
      * [ ] `genre`
      * [ ] les options (`multiple_ligne`, `service_internet`, ...)
    * [ ] Quelle métrique utiliser ?
      * [ ] Verifier si les classes sont équilibrées
      * [ ] Choisir une métrique en fonction de l'objectif (prédire les résiliants est plus important que prédire les non résiliants).
    * [ ] Utiliser GridSearchCV pour trouver les meilleurs hyperparamètres
    * [ ] Visualiser les résultats
      * [ ] Du GridSearchCV
      * [ ] Et du model final (regarder distribution des erreurs, matrice de confusion, ...)
