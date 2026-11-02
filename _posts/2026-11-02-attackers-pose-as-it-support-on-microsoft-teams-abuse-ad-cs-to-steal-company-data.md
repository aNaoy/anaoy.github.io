---
title: 'Attackers Pose as IT Support on Microsoft Teams, Abuse AD CS to Steal Company Data'
date: 2026-11-02
permalink: /posts/2026/11/02/attackers-pose-as-it-support-on-microsoft-teams-abuse-ad-cs-to-steal-company-data/
tags:
- veille-cyber
- hackernews
---
### Usurpation de support informatique et exploitation des services de certificats Active Directory (AD CS)

Des attaquants utilisent l'ingénierie sociale via Microsoft Teams pour se faire passer pour un support informatique, obtenir un accès à distance aux postes de travail via l'outil *Quick Assist*, puis compromettre l'infrastructure en exploitant des configurations vulnérables des services de certificats Active Directory (AD CS).

**Points clés :**
*   **Vecteur d'accès :** Usurpation d'identité sur Teams et prise de contrôle à distance par les employés eux-mêmes.
*   **Propagation :** Utilisation de scripts malveillants dissimulés pour déployer des outils et extraire des données ou élever des privilèges.
*   **Persistence :** L'obtention de certificats légitimes permet de maintenir l'accès même après une réinitialisation de mot de passe.
*   **Impact :** Vol de données d'entreprise et exécution de commandes sur les contrôleurs de domaine.

**Vulnérabilités exploitées (non liées à des failles logicielles, mais à des mauvaises configurations) :**
*   **ESC1 :** Permet à un utilisateur peu privilégié de demander un certificat en usurpant l'identité d'un compte hautement privilégié.
*   **ESC8 :** Exploitation du relais NTLM sur les pages d'inscription Web d'AD CS pour obtenir des certificats, souvent combinée avec l'attaque **PetitPotam**.

**Recommandations de sécurité :**
*   **Sensibilisation :** Vérifier systématiquement toute demande de support inattendue via un canal interne officiel et limiter l'accès aux outils de support à distance.
*   **Durcissement AD CS :**
    *   Auditer les modèles de certificats et restreindre les droits d'inscription.
    *   Activer l'authentification HTTPS et la protection étendue pour l'authentification (EPA) sur les points de terminaison Web d'inscription.
    *   Désactiver NTLM si possible sur les services AD CS.
*   **Surveillance et réponse :**
    *   Activer l'audit des certificats et révoquer les certificats suspects (tout en notant que cela n'invalide pas les tickets Kerberos actifs).
    *   S'assurer qu'aucune identité privilégiée n'est exclue des politiques de confinement automatique lors d'une alerte de sécurité.
    *   Utiliser les outils de posture de *Defender for Identity* pour détecter les modèles de certificats exposés à ESC1/ESC8.

---
[Source](https://thehackernews.com/2026/11/attackers-pose-as-it-support-on.html){:target="_blank"}
