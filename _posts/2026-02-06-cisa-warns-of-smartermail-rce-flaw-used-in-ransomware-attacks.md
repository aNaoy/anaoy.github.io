---
title: 'CISA warns of SmarterMail RCE flaw used in ransomware attacks'
date: 2026-02-06
permalink: /posts/2026/02/06/cisa-warns-of-smartermail-rce-flaw-used-in-ransomware-attacks/
tags:
- veille-cyber
- bleepingcomp
---
**Exploitation d'une faille critique dans SmarterMail pour des attaques par ransomware**

Des acteurs malveillants exploitent activement une vulnérabilité critique dans le logiciel de serveur de messagerie et de collaboration SmarterMail, permettant l'exécution de code à distance (RCE) sans authentification. L'agence américaine CISA a ajouté cette faille à son catalogue des vulnérabilités connues et exploitées (KEV).

**Points Clés :**

*   **Logiciel affecté :** SmarterMail, une plateforme de messagerie auto-hébergée et de collaboration.
*   **Nature de la menace :** Exploitation de la vulnérabilité pour mener des campagnes de ransomware.
*   **CISA :** L'Agence de cybersécurité et de sécurité des infrastructures des États-Unis a émis une alerte.
*   **Utilisateurs :** Le logiciel est couramment utilisé par les prestataires de services gérés (MSP), les PME et les sociétés d'hébergement, touchant environ 15 millions d'utilisateurs dans 120 pays.

**Vulnérabilités :**

*   **CVE-2026-24423 :** Faille critique dans le composant ConnectToHub API de SmarterMail, permettant l'exécution de code à distance sans authentification. Les versions antérieures au build 9511 sont affectées.
*   **WT-2026-0001 (nom interne) :** Une autre faille d'omission d'authentification découverte, permettant la réinitialisation du mot de passe administrateur sans vérification. Cette faille, bien que non référencée par un CVE, a également été exploitée.

**Recommandations :**

*   **Mise à jour immédiate :** Installer le dernier build disponible pour SmarterMail, actuellement le build 9526 (publié le 30 janvier), qui corrige ces failles.
*   **Application des correctifs :** Appliquer les mises à jour de sécurité et les mesures d'atténuation recommandées par le fournisseur.
*   **Arrêt de l'utilisation :** Pour les entités fédérales américaines et celles soumises à la directive BOD 22-01, il était impératif d'appliquer les correctifs ou de cesser d'utiliser le produit avant le 26 février 2026. Il est fortement conseillé à toutes les organisations d'en faire de même.

---
[Source](https://www.bleepingcomputer.com/news/security/cisa-warns-of-smartermail-rce-flaw-used-in-ransomware-attacks/){:target="_blank"}
