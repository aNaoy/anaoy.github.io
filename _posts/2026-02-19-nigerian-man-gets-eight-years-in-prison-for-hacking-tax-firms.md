---
title: 'Nigerian man gets eight years in prison for hacking tax firms'
date: 2026-02-19
permalink: /posts/2026/02/19/nigerian-man-gets-eight-years-in-prison-for-hacking-tax-firms/
tags:
- veille-cyber
- bleepingcomp
---
**Condamnation pour Fraude Fiscale Numérique**

Un homme nigérian a été condamné à huit ans de prison aux États-Unis pour son implication dans une vaste escroquerie visant des sociétés de préparation fiscale. L'individu, Matthew Abiodun Akande, a réussi à s'introduire dans les systèmes de plusieurs entreprises pour voler des informations personnelles de clients. Ces données ont ensuite été utilisées pour déposer plus de 1000 déclarations de revenus frauduleuses, demandant indûment plus de 8,1 millions de dollars en remboursements. Au total, plus de 1,3 million de dollars ont été détournés avant que l'opération ne soit démantelée.

**Points Clés :**

*   **Méthode d'Attaque :** Utilisation du logiciel malveillant de type RAT (Remote Access Trojan) nommé Warzone, acheté avec des licences et dissimulé à l'aide d'un crypteur pour échapper aux antivirus.
*   **Ingénierie Sociale :** Envoi d'e-mails d'hameçonnage (phishing) se faisant passer pour un PDG d'une entreprise, contenant des documents fiscaux authentiques pour crédibiliser le message et dirigeant les victimes vers un lien Dropbox.
*   **Exploitation :** Le lien Dropbox contenait un fichier exécutable déguisé qui installait silencieusement le RAT sur les réseaux des sociétés de conseil fiscal.
*   **Vol de Données :** Le RAT a permis de voler les numéros de sécurité sociale et les informations fiscales antérieures des clients.
*   **Fraude :** Utilisation des informations volées pour soumettre des déclarations de revenus frauduleuses.
*   **Blanchiment :** Les remboursements frauduleux étaient dirigés vers des comptes bancaires contrôlés par des complices aux États-Unis, qui retiraient l'argent liquide et transféraient une partie vers le Mexique.

**Vulnérabilités :**

Bien que l'article ne détaille pas de CVE spécifiques pour les logiciels utilisés, il met en évidence la vulnérabilité des entreprises à :

*   L'utilisation de logiciels malveillants de type RAT (comme Warzone) capables de voler des données sensibles.
*   Les attaques par hameçonnage (phishing) sophistiquées, notamment celles utilisant l'usurpation d'identité et des pièces jointes ou liens trompeurs.
*   L'absence de mesures de sécurité adéquates pour détecter et bloquer les logiciels malveillants inconnus ou dissimulés.

**Recommandations :**

*   **Sécurité des Points d'Accès :** Renforcer la sécurité des terminaux avec des solutions antivirus et anti-malware à jour et performantes.
*   **Formation à la Cybersécurité :** Sensibiliser régulièrement les employés aux menaces d'hameçonnage et aux techniques d'ingénierie sociale.
*   **Vérification des Liens et Pièces Jointes :** Encourager une prudence accrue avant de cliquer sur des liens ou d'ouvrir des pièces jointes provenant d'expéditeurs inconnus ou suspects, même si le contenu semble légitime.
*   **Authentification Forte :** Implémenter des mécanismes d'authentification multi-facteurs pour protéger l'accès aux systèmes et aux données sensibles.
*   **Surveillance des Réseaux :** Mettre en place des systèmes de détection et de réponse aux incidents pour identifier rapidement toute activité suspecte sur le réseau.
*   **Segmentation du Réseau :** Limiter la propagation potentielle des malwares en segmentant les réseaux et en contrôlant les accès.

---
[Source](https://www.bleepingcomputer.com/news/security/nigerian-man-gets-eight-years-in-prison-for-hacking-tax-firms/){:target="_blank"}
