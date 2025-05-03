---
title: 'DOCUMENTATION : APPLICATIVE (Grafana, Stalwart, Elastic Security, Tvheadend, eBrigade)'
tags: [DOC-AP4]

---

[toc]

# eBrigade

## Création de CT

![Créer un CT sur proxmox](https://hackmd.io/_uploads/BJc2A8W3Je.png)

### Page 1 : Informations générales

![Page 1 de la création du CT (Général)](https://hackmd.io/_uploads/SkrSyDb3yl.png)

### Page 2 : Choix du modèle

![Page 2 de la création du CT (Modèle)](https://hackmd.io/_uploads/rJjiyDZ2yx.png)

### Page 3 : Disques

![Page 3 de la création du CT (Disques)](https://hackmd.io/_uploads/BJEExwZhJx.png)

### Page 4 : Processeur

![Page 4 de la création du CT (Processeur)](https://hackmd.io/_uploads/r1sKlvb2Jl.png)

### Page 5 : Mémoire

![Page 5 de la création du CT (Mémoire)](https://hackmd.io/_uploads/HJX0gvWhkx.png)

### Page 6 : Réseau

![Page 6 de la création du CT (Réseau)](https://hackmd.io/_uploads/S1uQzPZ3Jg.png)

### Page 7 : DNS

![Page 7 de la création du CT (DNS)](https://hackmd.io/_uploads/SJGuzvW31x.png)

### Page 8 : Confirmation

![Page 8 de la création du CT (Confirmation)](https://hackmd.io/_uploads/ryVnMvZ3yx.png)

## Installation des dépendances

### Connexion au CT

![Se connecter au CT](https://hackmd.io/_uploads/Bk-dQDb3ke.png)

### Configuration initiale d'Alpine

![setup-alpine (1/3)](https://hackmd.io/_uploads/SySwvwZ21l.png)

![setup-alpine (2/3)](https://hackmd.io/_uploads/SkxhDwZhJe.png)

![setup-alpine (3/3)](https://hackmd.io/_uploads/SyCYdwb2yg.png)

### Ajouter sudo

![Ajouter sudo](https://hackmd.io/_uploads/SyB2FDb3yx.png)

![Modifier visudo pour autoriser tous les utilisateurs à utiliser sudo](https://hackmd.io/_uploads/SkGWcPZ3yx.png)

### Copier les sources eBrigade

![Depuis l'utilisateur eBrigade, créer le dépôt source et ajouter sshfs pour transférer les fichiers](https://hackmd.io/_uploads/rJF89PZ3yl.png)

![Installer sshfs sur Windows et configurer la connexion](https://hackmd.io/_uploads/SyHIGubhke.png)

![Copier les sources depuis le serveur Windows](https://hackmd.io/_uploads/rJ7Wz_Wnkg.png)

![Copier les sources dans /var/www/localhost/htdocs](https://hackmd.io/_uploads/SJUbEd-n1l.png)

### Installer apache2 et PHP7

![Ajouter apache2](https://hackmd.io/_uploads/SJcCSsZ3yg.png)

![Ajouter les dépôts Alpine 3.14](https://hackmd.io/_uploads/S1LPNob3Jl.png)

![Mettre à jour et installer PHP7](https://hackmd.io/_uploads/SkiyLU7hyg.png)

![Donner les droits à apache sur le répertoire de configuration](https://hackmd.io/_uploads/ByX10c-3yx.png)

![Démarrer et activer apache2](https://hackmd.io/_uploads/B1X5wdb2kg.png)

### Installer MySQL

![Ajouter mariadb](https://hackmd.io/_uploads/S1fKcFb3Je.png)

![Configurer mariadb](https://hackmd.io/_uploads/rk5HqtWnke.png)

![Démarrer mariadb](https://hackmd.io/_uploads/S1ADiYWnJx.png)

![Sécuriser l'installation de MySQL](https://hackmd.io/_uploads/SJDejtZ21l.png)

![Ajouter mariadb au démarrage](https://hackmd.io/_uploads/S1w3KjW21l.png)

### Créer une base de données avec un utilisateur admin

![Créer la base de données avec l'utilisateur admin](https://hackmd.io/_uploads/rk193t-n1l.png)

## Configuration initiale

### Accéder via le navigateur

![Accéder au navigateur à l'adresse 172.16.15.20](https://hackmd.io/_uploads/rJz1u_Z2yg.png)

### Entrer les informations de la base de données

![Entrer les informations d'identification de la base de données](https://hackmd.io/_uploads/HyV_d_Wn1x.png)

### Choisir un mot de passe pour l'utilisateur admin

![Choisir un mot de passe pour l'utilisateur admin](https://hackmd.io/_uploads/H1k70qZ21e.png)

### Validation du changement de mot de passe

![Succès du changement de mot de passe](https://hackmd.io/_uploads/ryU5ts-3yl.png)

### Définir les paramètres de base (nom, etc.)

![Configurer les paramètres de base](https://hackmd.io/_uploads/H1CncsW3kl.png)

### Initialisation réussie

![Initialisation réussie](https://hackmd.io/_uploads/Skm1osZ2yx.png)

# Stalwart

## Création d'un container Debian

### Installer Stalwart

![Mettre à jour et installer les dépendances](https://hackmd.io/_uploads/ryUeFn-2ke.png)

![Installer Stalwart](https://hackmd.io/_uploads/Sy3x93b2ye.png)

![Télécharger et installer Stalwart](https://hackmd.io/_uploads/rkpnc3W3Jl.png)

![Installation de Stalwart dans /opt](https://hackmd.io/_uploads/HkFk22Wnkg.png)

## Configuration initiale de Stalwart

![Accéder à l'interface Stalwart](http://VMM68COL01.haut-rhin.gouv:8080/login)

![Créer les répertoires LDAP](https://hackmd.io/_uploads/Sy0vThW21e.png)

### Lier Active Directory (AD)

![Lier l'AD (1/3)](https://hackmd.io/_uploads/SJu8MTZ2ye.png)

![Lier l'AD (2/3)](https://hackmd.io/_uploads/B1RuMTZ3Jl.png)

![Lier l'AD (3/3)](https://hackmd.io/_uploads/BkVCz6-hkl.png)

### Modifier le répertoire d'authentification

![Changer le répertoire d'authentification](https://hackmd.io/_uploads/rktEX6W2yg.png)

### Créer un domaine

![Créer un domaine](https://hackmd.io/_uploads/rJBnVTZ3Je.png)

![Ajouter haut-rhin.gouv](https://hackmd.io/_uploads/rk_er6Zn1x.png)

### Voir les enregistrements DNS

![Voir les enregistrements DNS](https://hackmd.io/_uploads/HyK7Hab31e.png)

### Copier la zone DNS sur le DNS

![Copier la zone DNS vers le serveur DNS](https://hackmd.io/_uploads/Hyfj8T-2yl.png)

# Grafana

## Création d'un container Alpine

### Installer Grafana

![Installer Grafana sur Alpine](https://hackmd.io/_uploads/ByGiA0b2Jl.png)

![Activer Grafana au démarrage](https://hackmd.io/_uploads/Hk7LykfhJe.png)

![Démarrer Grafana](https://hackmd.io/_uploads/H1TtkJznJg.png)

## Configuration de Grafana

![Accéder à Grafana à l'adresse 172.16.10.50:3000 et se connecter avec les identifiants par défaut](https://hackmd.io/_uploads/BkhS5yM2kx.png)

![Mettre à jour le mot de passe admin](https://hackmd.io/_uploads/SyQ551Ghkl.png)

# Tvheadend

## Création d'un container Alpine

### Installer Tvheadend

![Installer Tvheadend sur Alpine](https://hackmd.io/_uploads/BkIxNbfnyx.png)

![Activer Tvheadend au démarrage](https://hackmd.io/_uploads/HkdN4WGnJl.png)

![Démarrer Tvheadend](https://hackmd.io/_uploads/ByDGrbGn1g.png)

## Configuration de Tvheadend

![Accéder à l'interface de Tvheadend à l'adresse 172.16.10.60:9981](https://hackmd.io/_uploads/HkiUBZG2Jl.png)

![Choisir la langue](https://hackmd.io/_uploads/SyY48ZMnkg.png)

![Définir un mot de passe pour l'interface](https://hackmd.io/_uploads/rki5LbGnJe.png)

![Sélectionner IPTV comme source de flux](https://hackmd.io/_uploads/Sk8MDWM21g.png)

![Passer l'URL IPTV](https://hackmd.io/_uploads/HJEIu-zh1e.png)

![Passer l'analyse de canaux](https://hackmd.io/_uploads/ByN5ObG31l.png)

![Autoriser la cartographie automatique](https://hackmd.io/_uploads/HJ9Ad-Ghyg.png)

![Finaliser la configuration](https://hackmd.io/_uploads/rkBWYZG2ye.png)

# Elastic Security

## Création d'un container Debian

### Installer Elastic Security

#### Installer Elastic Search

![Mettre à jour les dépôts et installer les prérequis](https://hackmd.io/_uploads/SkMxSUmhke.png)

![Télécharger la clé GPG pour ElasticSearch](https://hackmd.io/_uploads/rJBNB8mhJl.png)

![Ajouter le dépôt ElasticSearch](https://hackmd.io/_uploads/SJsKr8731g.png)

![Installer ElasticSearch](https://hackmd.io/_uploads/SkiyLU7hyg.png)

![Copier le mot de passe du super utilisateur](https://hackmd.io/_uploads/HJlDEP8X31e.png)

#### Installer Kibana

![Installer Kibana](https://hackmd.io/_uploads/BJeCPIX2yg.png)

### Configuration d'Elastic Security

#### Configuration d'Elastic Search

![Modifier /etc/elasticsearch/elasticsearch.yml](https://hackmd.io/_uploads/Sy-rjUm3kg.png)

![Autoriser l'accès depuis toutes les adresses IP](https://hackmd.io/_uploads/rymCjLQnJe.png)

![Démarrer le service ElasticSearch](https://hackmd.io/_uploads/BkVyC8Q21x.png)

#### Configuration de Kibana

![Modifier /etc/kibana/kibana.yml](https://hackmd.io/_uploads/BkhXRU7nyg.png)

![Modifier l'adresse d'écoute de Kibana](https://hackmd.io/_uploads/rJ-xZvXhyl.png)

![Démarrer Kibana](https://hackmd.io/_uploads/BkKNZvmh1e.png)

#### Connexion à Kibana

![Obtenir le token de connexion à Kibana](https://hackmd.io/_uploads/BkL0bwX3ke.png)

![Se connecter avec le token dans l'interface de Kibana](https://hackmd.io/_uploads/HycGfvmhkl.png)

![Vérifier la connexion via le code de vérification](https://hackmd.io/_uploads/S1sPzPX3ye.png)

![Attendre la configuration](https://hackmd.io/_uploads/SJoazwXnkx.png)

#### Générer les clés de chiffrement pour Kibana

![Générer les clés de chiffrement dans Kibana](https://hackmd.io/_uploads/rkQkIv73Je.png)

#### Ajouter les lignes à /etc/kibana/kibana.yml

![Ajouter les lignes nécessaires dans kibana.yml](https://hackmd.io/_uploads/HJ2dIPm31g.png)

### Configuration de l'agent Elastic

![Télécharger et installer Elastic Agent](https://hackmd.io/_uploads/Hyh22v73Jl.png)

![Décompresser l'archive d'Elastic Agent](https://hackmd.io/_uploads/HymspDQ2yg.png)

![Installer l'agent Elastic](https://hackmd.io/_uploads/ByE-dF73Jg.png)

![Démarrer l'agent Elastic](https://hackmd.io/_uploads/ryhYVm73Jl.png)

![Attendre la connexion de l'agent](https://hackmd.io/_uploads/Sk3Wzx73Je.png)
