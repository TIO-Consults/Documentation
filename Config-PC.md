 **la checklist complète**, claire et organisée, pour configurer ta nouvelle tour comme un **environnement pro Dev + Cloud/Lab**.
---

# ✅ **CHECKLIST OFFICIELLE – Configuration de ta nouvelle tour**

---

# 1️⃣ **Préparation du système (Ubuntu)**

### 🔧 Système & outils de base

* [ ] Mettre à jour Ubuntu
  `sudo apt update && sudo apt upgrade`
* [ ] Installer les outils essentiels
  `sudo apt install git curl wget htop tmux unzip zip build-essential`
* [ ] Configurer Git (nom + email)
* [ ] Générer une clé SSH
  `ssh-keygen -t ed25519`
* [ ] Ajouter la clé SSH à GitHub / GitLab

### 📂 Organisation des dossiers

* [ ] Créer un dossier général `~/workspace/`
* [ ] Créer les sous-dossiers :

  * [ ] `backend`
  * [ ] `mobile`
  * [ ] `front`
  * [ ] `infra`
  * [ ] `databases`
  * [ ] `sandbox` (tests et scripts)

---

# 2️⃣ **Environnement Java / Spring Boot (backend)**

### 🧰 Outils Java

* [ ] Installer **SDKMAN**
* [ ] Installer **Java 21** via SDKMAN
* [ ] Installer **Maven**
* [ ] Installer **Gradle** (optionnel)

### 🖥️ IDE

* [ ] Installer IntelliJ IDEA Community **ou** Eclipse
* [ ] Paramétrer les plugins : Lombok, Docker, YAML, etc.

### 🗄️ Bases de données

* [ ] Installer Docker
* [ ] Lancer PostgreSQL via Docker
* [ ] Créer un volume dédié Postgres
* [ ] Tester la connexion via `psql` ou DBeaver

### 🔍 Solr / moteurs de recherche

* [ ] Installer Solr (via Docker)
* [ ] Créer 2 instances : indexation + recherche
* [ ] Configurer la réplication comme dans ton projet
* [ ] Tester une requête curl pour valider l’instance

---

# 3️⃣ **Environnement Mobile / Front**

## 📱 React Native (Expo)

* [ ] Installer Node via `nvm`
* [ ] Installer Expo CLI
* [ ] Installer VSCode
* [ ] Installer Android Studio
* [ ] Créer un émulateur Android (Pixel 5 par ex.)
* [ ] Lier l’émulateur à Expo (test d’un projet simple)

## 🌐 React / Vue

* [ ] Installer Yarn ou PNPM (optionnel mais conseillé)
* [ ] Installer les extensions VSCode :

  * ESLint
  * Prettier
  * React Tools / Vue Tools
  * GitLens
* [ ] Tester un projet front (React ou Vue)

---

# 4️⃣ **Lab Cloud / DevOps Open Source**

## 🐳 Docker & Docker Compose

* [ ] Installer Docker Engine
* [ ] Ajouter ton utilisateur au groupe `docker`
* [ ] Installer Docker Compose
* [ ] Créer un fichier `docker-compose.yml` pour :

  * Postgres
  * Redis
  * RabbitMQ
  * Solr
  * Keycloak (optionnel)
* [ ] Tester le stack complet

## ⚙️ Ansible

* [ ] Installer Ansible
* [ ] Créer un projet Ansible dans `~/workspace/infra/ansible`
* [ ] Créer un inventaire local
* [ ] Faire un premier playbook (installer Docker, par ex.)
* [ ] Exécuter et valider

## ☁️ Kubernetes local (optionnel mais utile)

* [ ] Installer `k3d` ou `k3s`
* [ ] Créer un cluster local
* [ ] Installer kubectl
* [ ] Test : déployer un NGINX en kubernetes
* [ ] Installer Traefik / Ingress

## 📊 Monitoring

* [ ] Installer Netdata **ou** Prometheus + Grafana
* [ ] Accéder à l’interface pour vérifier les métriques

---

# 5️⃣ **Services & Serveurs pour tes projets**

## Pour Piri

* [ ] Mise en place du repository piri-api
* [ ] Mise en place du repository piri-ui
* [ ] Ajout des configs Solr dans Docker
* [ ] Test du build :
  `mvn clean install -Pprod`

## Pour Ya-Rayah

* [ ] Préparer backend Spring
* [ ] Préparer app mobile Expo
* [ ] Préparer front React
* [ ] Lancer les 3 en local

## Pour ColiShare (FastAPI)

* [ ] Installer Python (pyenv)
* [ ] Créer l’environnement virtuel
* [ ] Installer FastAPI + uvicorn
* [ ] Créer le premier endpoint
* [ ] Tester avec Swagger UI

---

# 6️⃣ **Finalisation & Optimisation**

* [ ] Configurer sauvegardes automatiques (rsync ou BorgBackup)
* [ ] Installer une solution de snapshot (Timeshift ou ZFS)
* [ ] Configurer les alias dans `~/.bashrc`
* [ ] Configurer tmux pour les sessions persistantes
* [ ] Mettre en place une **architecture de travail claire** :

  * un dossier par projet
  * un environnement isolé par technologie


