# Plateforme de Partage de Fichiers Sécurisée 



Ce projet vise à créer une plateforme de partage de fichiers sécurisée, axée sur le chiffrement et la gestion de l'intégrité des données.

------



## Objectifs & Livrables

### Objectifs

- Implémenter un **algorithme de chiffrement/déchiffrement** robuste.



### Livrables

- Un **script Python** qui chiffre un fichier en entrée.
- Une **démonstration** de chiffrement et de déchiffrement local.
- Un **schéma d’architecture** détaillé.

------



## Schéma d’architecture simplifié

L'architecture du projet s'articule autour de l'API et de la sécurisation des données.

- **Utilisateur :** Envoie ou récupère un fichier via l'API.
- **API (Flask/FastAPI) :** Gère les requêtes d'upload et de download.
- **Module de chiffrement :** Chiffre les fichiers avant leur stockage et les déchiffre au moment du téléchargement.
- **Stockage sécurisé :** Conserve les fichiers chiffrés et leurs métadonnées.

------



## Arborescence des livrables

Voici la structure du projet, organisée de manière logique pour le développement et la maintenance.

Bash

```
secure-file-sharing/
│── app.py                   		# Point d'entrée principal (Flask/FastAPI)
│── config.py                 		# Configuration (clé secrète, variables env)
│── requirements.txt    		# Dépendances Python
│── Dockerfile              		 # Dockerisation de l’app
│── .gitlab-ci.yml / .github/ 	 # Pipeline CI/CD (selon GitLab/GitHub)
│── README.md                  	 # Documentation du projet
│
├── src/                      	 # Code source principal
│   ├── crypto_utils.py   		     # Fonctions de chiffrement/déchiffrement
│   ├── hash_utils.py       	   # Fonctions de hachage (SHA-256)
│   ├── storage_manager.py   	  # Gestion des fichiers et métadonnées
│   ├── auth.py                		# Authentification (mot de passe maître / JWT)
│   └── __init__.py
│
├── data/                    	  # Données stockées (ignorer dans Git)
│   ├── encrypted/         		    # Fichiers chiffrés
│   └── metadata.json       	   # Métadonnées (UUID → nom + hash)
│
├── tests/                   	  # Tests unitaires
│   ├── test_crypto.py
│   ├── test_api.py
│   └── __init__.py
│
└── ci-cd/                   	  # Configurations DevOps
    ├── docker-compose.yml   	  # (optionnel) Pour tests locaux
    └── pipeline.yml          	 # Exemple de workflow CI/CD
```



### Explication rapide



- **`app.py` :** Lance l'API avec les routes `/upload` et `/download`.
- **`src/` :** Contient tout le code métier (chiffrement, authentification, gestion du stockage).
- **`data/` :** Répertoire pour le stockage local des fichiers chiffrés et de leurs métadonnées.
- **`tests/` :** Assure que le chiffrement, l'API et l'authentification fonctionnent correctement via des tests unitaires.
- **`ci-cd/` :** Fichiers de configuration pour le pipeline CI/CD et Docker.

------



## Planning de déroulement du projet 🗓️

Ce plan de travail de 5 jours est conçu pour le projet "Secure File Sharing Platform".



### **Jour 1 : Développement de l’application de base**

- **Objectifs :**
  - Créer une API minimale (Flask ou FastAPI) avec les routes `POST /upload` et `GET /download/{id}`.
  - Utiliser un **UUID** pour les identifiants de fichiers.
  - Stocker la correspondance entre l'ID et le nom original dans une base de données (ex: SQLite) ou un fichier JSON.
- **Livrables :**
  - Une API fonctionnelle pour l'upload et le download.
  - Un test de l'API avec un outil comme Postman ou cURL.



### **Jour 2 : Sécurité & bonnes pratiques**

- **Objectifs :**
  - Ajouter une **authentification** basique (mot de passe maître ou JWT).
  - Vérifier l'**intégrité des fichiers** à l'aide d'un hash **SHA-256**.
  - Rédiger des **tests unitaires** avec `pytest` pour les fonctions de chiffrement et d'API.
- **Livrables :**
  - L'authentification est activée.
  - Un test automatisé qui confirme que le fichier téléchargé est identique au fichier original.



### **Jour 3 : DevOps & CI/CD**

- **Objectifs :**
  - Créer un **Dockerfile** pour containeriser l'application.
  - Mettre en place un **pipeline CI/CD** (GitHub Actions ou GitLab CI) pour :
    - Lancer les tests unitaires à chaque `push`.
    - Construire l'image Docker.
    - Déployer l'image sur DockerHub ou un serveur local.
- **Livrables :**
  - L'application est dockerisée.
  - Un pipeline CI/CD est fonctionnel.



### **Jour 4 : Finalisation & Soutenance**

- **Objectifs :**
  - Démontrer le flux complet : `commit` → `pipeline` → `build Docker` → `déploiement`.
  - Démontrer l'upload, le stockage chiffré, le download et la vérification d'intégrité.
  - Rédiger un **README** clair avec les instructions d'installation, d'utilisation et le schéma d'architecture.
- **Livrables :**
  - Une démonstration complète et réussie du workflow.



### **Jour 5 : Soutenance devant la classe**

- **Livrables :**
  - Une **démonstration live** de l'upload/download sécurisé via l'API.
  - Un **README** documenté, incluant la description du projet, les instructions d'installation, des exemples d'utilisation de l'API et les mesures de sécurité mises en place.
