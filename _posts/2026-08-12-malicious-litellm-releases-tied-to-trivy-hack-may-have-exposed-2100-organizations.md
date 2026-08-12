---
title: 'Malicious LiteLLM Releases Tied to Trivy Hack May Have Exposed 2,100+ Organizations'
date: 2026-08-12
permalink: /posts/2026/08/12/malicious-litellm-releases-tied-to-trivy-hack-may-have-exposed-2100-organizations/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement : L'affaire LiteLLM et TeamPCP

En mars 2026, deux versions malveillantes de la bibliothèque open-source **LiteLLM** (1.82.7 et 1.82.8) ont été publiées sur PyPI. Ces versions contenaient un code malveillant capable d'exfiltrer des secrets sensibles (clés cloud, jetons Kubernetes, mots de passe de bases de données, clés SSH et API) vers un domaine contrôlé par des attaquants. Cette attaque s'inscrit dans la campagne plus large « TeamPCP » (suivie sous le nom **UNC6780**), qui a également compromis le scanner de sécurité **Trivy** d'Aqua Security.

**Points clés :**
* **Portée :** Plus de 2 500 organisations potentiellement exposées via 434 000 fichiers exfiltrés.
* **Mécanisme :** Le fichier `litellm_init.pth` permettait l'exécution automatique du code malveillant dès le démarrage d'un processus Python, indépendamment de l'importation directe de LiteLLM.
* **Origine :** La compromission initiale semble provenir d'une rotation incomplète des secrets suite à l'attaque sur les outils Trivy, permettant aux attaquants de voler des jetons de publication PyPI.
* **Impact :** Des entités majeures (Cisco, NVIDIA, Commission européenne, etc.) ont été identifiées comme victimes potentielles.

**Vulnérabilités :**
* **CVE-2026-33634 :** Identifiant la compromission globale de la chaîne d'approvisionnement incluant LiteLLM (versions 1.82.7-1.82.8) et les composants Trivy.

**Recommandations :**
1. **Audit de dépendances :** Vérifier toute installation de LiteLLM effectuée le 24 mars 2026 entre 10:39 et 16:00 UTC. Attention aux dépendances transitives non épinglées.
2. **Rotation des secrets :** Considérer comme compromis tous les secrets (clés cloud, jetons, mots de passe) accessibles par les systèmes ayant installé les versions corrompues. Privilégier désormais l'utilisation de jetons temporaires plutôt que de secrets à longue durée de vie.
3. **Recherche d'indicateurs (IoC) :** Rechercher sur GitHub des dépôts contenant les préfixes `tpcp-docs-` ou des assets de release tagués `data-<timestamp>`, utilisés par les attaquants pour stocker les données volées.

---
[Source](https://thehackernews.com/2026/08/malicious-litellm-releases-tied-to.html){:target="_blank"}
