# Projet de Clustering Textuel - Rapport de Fusion

-- réalisé par Reina EL ITAOUI et Lydia GUISSI

## Objectif

L'objectif de ce projet est de simuler un environnement de développement collaboratif pour créer un modèle de clustering textuel basé sur la réduction de dimensionnalité (ACP, TSNE, UMAP) et l'algorithme de clustering K-Means. Chaque membre de l'équipe travaillera sur une approche spécifique dans une branche distincte avant de fusionner ses modifications dans la branche principale (`main`). Enfin, une image Docker sera créée, exécutée et partagée sur Docker Hub pour permettre un déploiement facile.

## Consignes

1. **Développement du Modèle de Clustering :**
   - Utilisation des données textuelles, les données NG20 limitées à 2000 documents.
   - Développement d'une approche séquentielle combinant la réduction de dimensionnalité (ACP, TSNE, UMAP) avec l'algorithme de clustering K-Means.

2. **Repository GitHub :**
   - Création d'un repository GitHub avec un README et un `.gitignore`.
   - Ajout d'un fichier `main.py` évaluant chaque approche (ACP+kmeans, TSNE+kmeans, UMAP+kmeans) avec des métriques telles que NMI, ARI et Accuracy.

3. **Travail en Collaboration :**
   - Travail de manière indépendante et asynchrone.
   - Utilisation du notebook `template_branche.ipynb` pour le développement et les tests.
   - Création d'une nouvelle branche pour chaque approche (ACP, TSNE, UMAP).
   - Fusion de chaque branche avec `main` via une pull request.
   - Ajout du notebook dans un dossier "experiments" et de l'approche dans `main.py`.

4. **Création de l'Image Docker :**
   - Clone de la branche `main` sur la machine.
   - Création d'un Dockerfile spécifiant l'environnement et les dépendances nécessaires.
   - Exécution du fichier `main.py` dans le conteneur Docker.
   - Récupération des résultats du clustering pour chaque méthode.

5. **Publication sur Docker Hub :**
   - Création d'une image Docker avec les modifications apportées. [ optimisée - voir la suite -  https://hub.docker.com/repository/docker/reitaoui/image_bonus/general ]
   - Push de l'image sur Docker Hub pour la rendre accessible à d'autres membres de l'équipe.
     
## BONUS 
### Modification du Code dans la branche bonus (Optimisation majeure)

Le code initial a été significativement amélioré dans la branche bonus pour éviter la dépendance à `sentence_transformers` en raison de sa taille importante (réduisant les imports de 8GB à 760MB). De plus, des méthodes de clustering supplémentaires, telles que l'Agglomerative Clustering et DBSCAN, ont été intégrées pour offrir une variété d'options aux utilisateurs. De plus, des visualisations après chaque méthode de réduction de dimension ont été ajoutées pour faciliter l'analyse des résultats.

À la place de `sentence_transformers`, une approche de base d'extraction de caractéristiques à l'aide de 'pickle' et `CountVectorizer` a été intégrée. Ces modifications ont été apportées pour améliorer l'efficacité, faciliter le partage et garantir la reproductibilité du code au sein de l'équipe.

La nouvelle image docker - [ https://hub.docker.com/repository/docker/reitaoui/image_bonus/general ]
L'ancienne image qui nécessitait 8 GB d'imports - [https://hub.docker.com/r/lydiagu00/leprojet]

En suivant ces étapes, la branche bonus offre une version optimisée du workflow collaboratif de développement, de tests et de déploiement d'un modèle de clustering textuel. L'utilisation de Docker facilite la distribution du modèle, assurant ainsi une reproductibilité de l'environnement.
