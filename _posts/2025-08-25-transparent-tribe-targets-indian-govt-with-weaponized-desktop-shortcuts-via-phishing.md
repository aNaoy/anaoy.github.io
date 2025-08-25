---
title: 'Transparent Tribe Targets Indian Govt With Weaponized Desktop Shortcuts via Phishing'
date: 2025-08-25
permalink: /posts/2025/08/25/transparent-tribe-targets-indian-govt-with-weaponized-desktop-shortcuts-via-phishing/
tags:
- veille-cyber
- hackernews
---
**Transparent Tribe cible les institutions gouvernementales indiennes avec des raccourcis malveillants**

Le groupeAPT (Advanced Persistent Threat) Transparent Tribe, également connu sous le nom d'APT36, a ciblé des entités gouvernementales indiennes en utilisant des fichiers de raccourcis de bureau malveillants. Ces attaques visent à la fois les systèmes Windows et BOSS Linux.

L'accès initial est obtenu par le biais d'e-mails de hameçonnage ciblés. Les fichiers ".desktop" malveillants, qui se font passer pour des documents PDF, déclenchent l'exécution d'un script shell lorsqu'ils sont ouverts. Ce script télécharge et exécute une charge utile malveillante (un binaire écrit en Go) à partir d'un serveur contrôlé par l'attaquant. Ce binaire établit ensuite une connexion avec un serveur de commande et de contrôle (C2) pour recevoir des instructions, télécharger d'autres charges utiles et exfiltrer des données. La persistance est assurée par un cron job.

Ce malware, identifié comme une variante du backdoor Poseidon de Transparent Tribe, est capable de reconnaissance système, d'évasion des techniques anti-débogage et anti-sandbox, de collecte de données, d'obtention d'un accès à long terme, de vol d'identifiants et potentiellement de mouvements latéraux au sein du réseau compromis.

Des campagnes antérieures de Transparent Tribe ont ciblé des organisations de défense indiennes et des entités gouvernementales connexes en utilisant des domaines usurpés pour voler des identifiants et des codes d'authentification à deux facteurs (2FA), y compris la solution Kavach utilisée par le gouvernement indien. L'utilisation de domaines typo-squattés et d'une infrastructure basée au Pakistan correspond aux tactiques et procédures établies du groupe.

**Points clés :**

*   **Acteur :** Transparent Tribe (APT36)
*   **Cibles :** Institutions gouvernementales indiennes (Windows et BOSS Linux)
*   **Méthode d'accès initial :** Hameçonnage ciblé avec des fichiers de raccourcis de bureau malveillants (.desktop)
*   **Charges utiles :** Backdoor Poseidon, scripts shell, binaires Go
*   **Capacités du malware :** Reconnaissance système, évasion, collecte de données, vol d'identifiants, persistance, mouvements latéraux potentiels.
*   **Tactiques supplémentaires :** Domaines usurpés, vol d'identifiants 2FA (Kavach).

**Vulnérabilités exploitées :**

L'article ne mentionne pas de CVE spécifiques. Les vulnérabilités exploitées sont principalement liées à :

*   La confiance des utilisateurs dans les pièces jointes d'e-mails.
*   La façon dont les systèmes d'exploitation gèrent les fichiers de raccourcis (par exemple, l'exécution de scripts associés aux fichiers .desktop).
*   La potentielle faiblesse des processus d'authentification si les pages de connexion sont compromises.

**Recommandations :**

Bien que l'article ne fournisse pas de recommandations directes, les actions suivantes peuvent être déduites pour atténuer ce type de menaces :

*   **Sensibilisation et formation :** Former les employés à reconnaître et signaler les e-mails de hameçonnage, les pièces jointes suspectes et les liens potentiellement malveillants.
*   **Vérification des sources :** Encourager une vérification rigoureuse des expéditeurs et de la légitimité des documents reçus par e-mail.
*   **Sécurité des points d'extrémité :** Maintenir des solutions antivirus et anti-malware à jour sur tous les systèmes.
*   **Gestion des privilèges :** Appliquer le principe du moindre privilège pour limiter les actions possibles en cas de compromission.
*   **Patch Management :** S'assurer que les systèmes d'exploitation et les logiciels sont régulièrement mis à jour pour corriger les vulnérabilités connues.
*   **Segmentation du réseau :** Limiter la propagation potentielle du malware en segmentant le réseau.
*   **Surveillance et analyse des journaux :** Mettre en place une surveillance active pour détecter les comportements anormaux et examiner régulièrement les journaux système.

---
[Source](https://thehackernews.com/2025/08/transparent-tribe-targets-indian-govt.html){:target="_blank"}
