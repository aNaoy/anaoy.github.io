---
title: 'CISA gives govt agencies 7 days to patch new Fortinet flaw'
date: 2025-11-19
permalink: /posts/2025/11/19/cisa-gives-govt-agencies-7-days-to-patch-new-fortinet-flaw/
tags:
- veille-cyber
- bleepingcomp
---
**Alerte de Sécurité : Fortinet FortiWeb sous le Feu des Attaques**

Les agences gouvernementales américaines ont reçu une directive de la CISA leur imposant de sécuriser leurs systèmes sous sept jours face à une nouvelle faille critique découverte dans le pare-feu d'applications web FortiWeb de Fortinet. Cette vulnérabilité, référencée **CVE-2025-58034**, permet à des acteurs malveillants authentifiés d'exécuter du code non autorisé sur le système sous-jacent grâce à des requêtes HTTP ou des commandes CLI spécialement conçues. L'exploitation de cette faille est relativement simple et ne nécessite pas d'interaction de la part de l'utilisateur.

La CISA a ajouté cette vulnérabilité à son catalogue des vulnérabilités connues et exploitées, soulignant son potentiel élevé de vector d'attaque pour les cybercriminels. Cette action fait suite à une autre vulnérabilité similaire (CVE-2025-64446) dans le même produit, qui a également été exploitée en "zero-day" et qui a fait l'objet d'une directive de correction avec une date limite plus ancienne.

Ces incidents s'ajoutent à une série de vulnérabilités Fortinet qui ont été exploitées dans le passé pour des cyberespionnages, des attaques par ransomware, et des compromissions d'infrastructures critiques.

**Points Clés :**

*   **Produit affecté :** Fortinet FortiWeb (pare-feu d'applications web)
*   **Nature de la faille :** Injection de commandes OS (OS Command Injection)
*   **Impact :** Permet l'exécution de code non autorisé sur le système sous-jacent
*   **Conditions d'exploitation :** Nécessite une authentification et des requêtes/commandes spécialement conçues
*   **Exploitation :** Déjà exploitée en "zero-day"

**Vulnérabilités :**

*   **CVE-2025-58034 :** Injection de commandes OS (OS Command Injection)
*   **CVE-2025-64446 :** Autre faille de FortiWeb, également exploitée en "zero-day" et ayant fait l'objet d'une directive de correction distincte.

**Recommandations :**

*   **Mise à jour immédiate :** Les agences gouvernementales fédérales américaines sont sommées de patcher leurs systèmes affectés sous sept jours (date limite le 25 novembre 2025).
*   **Surveillance :** Il est conseillé aux organisations utilisant FortiWeb de vérifier l'état de leurs systèmes et d'appliquer les correctifs de sécurité dès qu'ils sont disponibles.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-gives-govt-agencies-7-days-to-patch-new-fortinet-flaw/){:target="_blank"}
