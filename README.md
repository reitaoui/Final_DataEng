# Projet de Clustering Textuel

## Objectif

Simuler un projet d'entreprise réel où plusieurs développeurs travaillent sur le même projet, chacun développant une fonctionnalité dans une branche différente, puis fusionnant sa version finale avec la branche principale (`main`). L'objectif final est de créer un conteneur Docker basé sur la branche principale du dépôt GitHub, se mettant à jour automatiquement en production.

## Consignes

Utilisez le [repository GitHub](https://github.com/MLDS-AF/Examen) comme point de départ, contenant des templates. Suivez les étapes ci-dessous :

1. Développez un modèle de clustering basé sur la réduction de la dimensionalité via l'ACP, l'AFC et UMAP (espace réduit de dimension 20). Utilisez des données textuelles (par exemple, les données NG20, en limitant à 2000 documents). La méthode est séquentielle, combinant une méthode de réduction de dimension avec l'algorithme de clustering K-Means.

2. Créez un repository GitHub contenant un README et un `.gitignore`. Ajoutez un fichier `main.py` évaluant chaque approche (ACP+kmeans, TSNE+kmeans, UMAP+kmeans) avec des métriques telles que NMI, ARI et Accuracy. 

3. Travaillez de manière indépendante et asynchrone, en développant chaque approche dans une nouvelle branche. Utilisez le notebook `template_branche.ipynb` pour développer et tester le modèle. Fusionnez ensuite chaque méthode avec la branche `main` à l'aide d'une pull request, en ajoutant votre notebook dans un dossier "experiments" et votre approche dans `main.py`.

4. Faites un clone de la branche `main` sur une machine, créez une image Docker et exécutez le fichier `main.py`. Récupérez les résultats du clustering pour chaque méthode.

5. Poussez l'image Docker résultante sur Docker Hub pour la rendre accessible à d'autres utilisateurs.

