# [Labs] Initiation à Docker

    Auteur: Sébastien DAVOULT
    Courriel: d@vou.lt
    Licence: CC-BY-4.0
    Version: 1.0

<!--- Forked from  --->

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />Ce support de formation est distribué sous la license <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## Environnement

Chaque participant a accès à son environnement, il est composant d'un cluster Kubernetes, voici les paramètres:

| Clé        | Valeur                 |
| ---------- | ---------------------- |
| Adresse IP |                        |
| Kubeconfig | (livré au participant) |

## 1 - Mon premier conteneur Kubernetes

Dans cet exercice, vous allez déployer un *conteneur* dans un *POD* unique propulsé par un simple *déploiement*.

- [ ] Création d'un *deploiement* nommé whoami
  - [ ] Utilisant l'image **containous/whoami**
  - [ ] Utilisant le port interne **80/TCP**
- [ ] Création d'un service nommé **whoami**
  - [ ] Ecoutant sur le port **80**
  - [ ] Lié au deploiement **whoami**
  - [ ] Type de service: **NodePort**
  - [ ] Récupérer le port utilisé sur la machine hôte
- [ ] Accéder au service whoami depuis votre poste client

## 2 - Stockage persistant

Dans cet exercice, vous allez déployer un *Deployment* propulsant une base de données sur un *Stockage Persistant*.

- [ ] Création d'un *déploiement* nommé mariadb
  - [ ] Utilisant l'image **mariadb:latest**
  - [ ] Utilisant le port interne **3306/TCP**
  - [ ] Créer un compte utilisateur nommé **wordpress**
  - [ ] Créer un mot de passe pour l'utilisateur **wordpress**
  - [ ] Le mot de passe *root* de MariaDB devra etre généré automatiquement
  - [ ] Créer une base de données nommée **wordpress**
- [ ] Création d'un service nommé **mariadb**
  - [ ] Ecoutant sur le port **56100** 
  - [ ] Lié au déploiement **mariadb**
  - [ ] Type de Service: **ClusterIP**
- [ ] Création d'un *Pod* ephémaire de debug
  - [ ] Utilisant l'image **ubuntu:latest**
  - [ ] Installer le paquet **mariadb-client**
  - [ ] Installer un client **mariadb**
  - [ ] Réaliser une connexion pour valider le bon fonctionnement