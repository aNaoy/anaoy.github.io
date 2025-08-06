---
title: 'ReVault! When your SoC turns against you…'
date: 2025-08-06
permalink: /posts/2025/08/06/revault-when-your-soc-turns-against-you/
tags:
- veille-cyber
- zerodaysfans
---
### ReVault : Quand le matériel se retourne contre l'utilisateur

Des vulnérabilités critiques ont été découvertes dans le firmware ControlVault3 et ses API Windows associées, baptisées "ReVault". Ces failles affectent plus de 100 modèles d'ordinateurs portables Dell et peuvent compromettre gravement la sécurité des appareils.

**Points clés :**

*   **Persistance après compromission :** ReVault permet aux attaquants de maintenir une présence sur le système, même après une réinstallation de Windows.
*   **Contournement de la sécurité :** Une attaque physique permet de contourner l'authentification Windows et d'obtenir des privilèges administrateur ou système.
*   **Impact sur la biométrie :** Il est possible de modifier le firmware pour qu'il accepte n'importe quelle empreinte digitale, neutralisant ainsi la sécurité biométrique.

**Vulnérabilités identifiées :**

*   **CVE-2025-24311 :** Vulnérabilité de dépassement de tampon (Out-of-bounds vulnerability).
*   **CVE-2025-25050 :** Vulnérabilité de dépassement de tampon (Out-of-bounds vulnerability).
*   **CVE-2025-25215 :** Vulnérabilité de libération arbitraire de mémoire (Arbitrary free).
*   **CVE-2025-24922 :** Vulnérabilité de dépassement de pile (Stack overflow).
*   **CVE-2025-24919 :** Vulnérabilité de désérialisation non sécurisée (Unsafe deserialization) affectant les API Windows.

**Recommandations :**

*   **Mise à jour du système :** Maintenez vos systèmes à jour pour installer le dernier firmware ControlVault.
*   **Désactivation des services :** Si les périphériques de sécurité (lecteur d'empreintes digitales, lecteur de carte à puce, lecteur NFC) ne sont pas utilisés, désactivez les services ControlVault.
*   **Désactivation de la connexion par empreinte digitale :** Envisagez de désactiver l'authentification par empreinte digitale dans des environnements à risque accru.
*   **Sécurité de connexion renforcée :** Activez la fonctionnalité "Enhanced Sign-in Security" (ESS) de Windows pour atténuer certaines attaques physiques et détecter des firmwares ControlVault potentiellement compromis.
*   **Détection d'intrusion :** Activez la détection d'intrusion physique dans le BIOS de l'ordinateur.
*   **Surveillance des journaux :** Soyez attentif aux plantages inattendus des services biométriques ou des services de gestion des informations d'identification dans les journaux Windows.

---
[Source](https://blog.talosintelligence.com/revault-when-your-soc-turns-against-you/){:target="_blank"}
