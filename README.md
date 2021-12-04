# credit_scoring 

Dans ce projet nous avons pour but d'étudier différentes méthodes de classification supervisée sur des données présentant diverses structures : numériques, catégorielles.

Les étapes pour la réalisation du projets :
 * __Chargement des données et préparation__ : Dans un premier temps nous avons importer le jeu de données
et analyser ses caractéristiques.
 * __Apprentissage et évaluation de modèles__
 * __Normalisation des variables continues__
 * __Traitement de données manquantes__ : Nous avons imputer les valeurs manquantes dans notre jeu de données en utilisant les stratégies non supervisés suivantes du lodule Scikit-learn:
   * __mean__ pour les variables continues
   * __most_frequent__ pour les variables catégorielles
 * __Traitement de variables catégorielles__ : Pour pouvoir utiliser les variables catégorielles dans les algorithmes d'appretissage supervisé, nous avons transformer chaque variable catégorielle avec m modalités en m variables binaires dont une seule sera active.
 * __Construction de notre jeu de données__ : NOus avons constuit notre jeu de données en concaténant à la fois les données catégorielles transformées et les données continues normalisées.
 * __Création de nouvelles variables caractéristiques par combinaisons linéaires des variables initiales__
 * __Sélection de variables__: vous avons utiliser la méthode Random Forest de Scikit-learn pour déterminer quelles sont les meilleures variables pour prédire
si une personne va payer son crédit ou pas.
 * __Paramétrage des classifieurs__ : Dans cette partie, vous avons utiliser la fonction GridSearchCV de scikit-learn
afin de tuner les paramètres des trois algorithmes k-plus proches voisins, MLP et Arbre de décision.
 * __Création d’un pipeline__ : Dans cette partie vous avons automatiser l’enchainement des traitements effectués
précédemment (Normalisation, ACP et Construction du classifieur) dans un pipeline 
 * __Comparaison de plusieurs algorithmes d’apprentissage sur une même validation croisée__ : Nous avons ensuite utiliser sur notre jeu de données les algorihtmes d'apprentissage supervisé suivants :
   * NaiveBayesSimple
   * Un arbre CART
   * MultilayerPerceptron à deux couches de tailles respectives 20 et 10
   * k-plus-proches-voisins avec k=5
   * Bagging avec 50 classifieurs
   * AdaBoost avec 50 classifieurs
   * Random Forest avec 50 classifieurs

Data:

Ces données concerne les demandes de crédit. Tous les noms et valeurs d'attributs ont été remplacés par des symboles sans signification pour protéger la confidentialité des données.

Cet ensemble de données est intéressant car il existe un bon mélange d'attributs : continu, nominal avec un petit nombre de valeurs et nominal avec un plus grand nombre de valeurs. Il y a aussi quelques valeurs manquantes.


Contents:
Ce fichier comporte 16688 instances décrites par 15 variables caractéristiques (6 numériques, 9
catégorielles) et la variable à prédire "classe" (la dernière colonne du fichier) de nature nominale possédant un
nombre fini de valeurs (ici deux valeurs "+" et "–"). Il ne s’agit pas d’une tâche de régression, mais de
classification. Les exemples de ce jeu de données représentent des personnes (positifs et négatifs) pour lesquels
un crédit a été accordé ou non.


Contributors : HAMAT Abdoulaye, GLASS Philippe.
(Masters 2nd years students).

Data Source : https://archive.ics.uci.edu/ml/datasets/Credit+Approval

