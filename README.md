# Guide d'installation de l'infrastructure sécurisée

Ce guide vous aidera à installer une infrastructure sous Minikube. Suivez les étapes ci-dessous pour mettre en place un environnement vulnérable et sécurisé.

## Prérequis

Avant de commencer, assurez-vous d'avoir les éléments suivants :

- Système d'exploitation : Ubuntu 22/04 ou tout autre environnement Linux
- Minikube : Installation de Minikube pour la gestion des clusters Kubernetes. Référez-vous à la documentation officielle pour les instructions d'installation.
- Lens : Installation de Lens, une interface graphique pour la gestion de clusters Kubernetes. Référez-vous à la documentation officielle pour les instructions d'installation.
- OWASP ZAP : Installation d'OWASP ZAP, un outil de sécurité pour les tests d'intrusion. Référez-vous à la documentation officielle pour les instructions d'installation.
- Postman : Installation de Postman, une plateforme de développement d'API. Référez-vous à la documentation officielle pour les instructions d'installation.
- Visual Studio Code : Installation de Visual Studio Code, un éditeur de code source. Référez-vous à la documentation officielle pour les instructions d'installation.
- Langage de programmation : YAML (pour les manifestes Kubernetes, Helm et Helmfile).

## Étapes d'installation

1. Clonage du dépôt :

```shell
git clone https://github.com/AsTheLow/projet-tut.git
```


2. Démarrage de Minikube :

```shell
minikube start 
```
3. Application des fichiers Helmfile pour le déploiement des ressources vulnérables :
```shell
cd /chemin/projet-tut/helmfile/vulnerable/
helmfile apply 
```
4. Retour à la racine du projet :
```shell
cd .. 
```
5. Déploiement du module de sécurité (ModSecurity) :
```shell
cd modsec/
helmfile apply
```
6. Votre infrastructure est maintenant déployée ! Accédez à Lens pour visualiser les différents conteneurs démarrés.

## Utilisation

Pour utiliser l'infrastructure déployée, suivez les étapes suivantes :

1. Ouvrez Lens, l'interface graphique de gestion de clusters Kubernetes.

2. Connectez-vous à votre cluster Minikube.

3. Visualisez les différents conteneurs démarrés et assurez-vous que tout fonctionne correctement.

4. Utilisez OWASP ZAP pour effectuer des tests d'intrusion sur votre infrastructure et identifier les vulnérabilités.

5. Utilisez Postman pour développer et tester vos API dans l'environnement sécurisé.

6. Utilisez Visual Studio Code pour travailler sur les fichiers YAML des manifestes Kubernetes, Helm et Helmfile.

## Contribution

Si vous souhaitez contribuer à l'amélioration de cette infrastructure sécurisée, suivez les étapes ci-dessous :

1. Fork ce dépôt sur GitHub.

2. Effectuez vos modifications et améliorations.

3. Soumettez une demande d'extraction (pull request) avec une description détaillée des changements apportés.

4. Vos contributions seront examinées et fusionnées si elles répondent aux critères de qualité.

## Problèmes

Si vous rencontrez des problèmes lors de l'installation ou de l'utilisation de l'infrastructure sécurisée, veuillez créer une issue sur le dépôt GitHub. Décrivez le problème en détail et fournissez toutes les informations nécessaires pour le reproduire.

## Licence

Ce projet est sous licence MIT. Consultez le fichier `LICENSE` pour plus d'informations.

