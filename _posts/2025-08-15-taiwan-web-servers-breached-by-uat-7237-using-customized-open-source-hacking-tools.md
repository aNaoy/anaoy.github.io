---
title: 'Taiwan Web Servers Breached by UAT-7237 Using Customized Open-Source Hacking Tools'
date: 2025-08-15
permalink: /posts/2025/08/15/taiwan-web-servers-breached-by-uat-7237-using-customized-open-source-hacking-tools/
tags:
- veille-cyber
- hackernews
---
**Menace Persistante Avancée UAT-7237 Cible les Infrastructures Web Taïwanaises**

Un groupe d'acteurs de menace, identifié comme UAT-7237 et actif depuis au moins 2022, s'est attaqué à des entités d'infrastructure web à Taïwan. Ce groupe, potentiellement une sous-branche de UAT-5918, personnalise des outils open-source pour prolonger son accès aux environnements des victimes. Les attaques débutent par l'exploitation de vulnérabilités connues sur des serveurs non corrigés, suivies d'une phase de reconnaissance.

**Points Clés :**

*   **Cible :** Entités d'infrastructure web à Taïwan.
*   **Acteur :** UAT-7237, groupe d'origine chinoise.
*   **Méthodologie :** Utilisation d'outils open-source personnalisés pour l'évasion et l'accès persistant.
*   **Outils utilisés :**
    *   SoundBill : Chargeur de shellcode personnalisé pour décoder et lancer des charges utiles secondaires.
    *   Cobalt Strike : Utilisé comme porte dérobée principale.
    *   SoftEther VPN client : Pour maintenir l'accès.
    *   RDP (Remote Desktop Protocol) : Pour l'accès direct aux systèmes.
    *   JuicyPotato : Pour l'escalade de privilèges.
    *   Mimikatz : Pour l'extraction de mots de passe.
    *   FScan : Pour l'identification des ports ouverts.
*   **Déviations par rapport à UAT-5918 :** Moins de déploiement immédiat de web shells, préférence pour SoftEther VPN et RDP pour la persistance.
*   **Indicateur :** Configuration de langue chinoise simplifiée dans le client SoftEther VPN.

**Vulnérabilités exploitées :**

L'article mentionne l'exploitation de "known security flaws against unpatched servers exposed to the internet". Aucune vulnérabilité spécifique avec un identifiant CVE n'est nommée pour ces exploits initiaux dans le contexte de UAT-7237.

**Recommandations :**

L'article ne contient pas de recommandations explicites pour les organisations. Cependant, les observations suggèrent l'importance de :

*   Maintenir les serveurs web à jour et corrigés contre les vulnérabilités connues.
*   Surveiller l'utilisation d'outils tels que SoftEther VPN et les connexions RDP suspectes.
*   Mettre en œuvre des mécanismes de détection et de prévention d'intrusion robustes.
*   Restreindre les privilèges d'accès pour limiter l'escalade des privilèges.

---
[Source](https://thehackernews.com/2025/08/taiwan-web-servers-breached-by-uat-7237.html){:target="_blank"}
