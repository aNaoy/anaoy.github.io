---
title: 'ThreatsDay Bulletin: OpenSSL RCE, Foxit 0-Days, Copilot Leak, AI Password Flaws & 20+ Stories'
date: 2026-02-19
permalink: /posts/2026/02/19/threatsday-bulletin-openssl-rce-foxit-0-days-copilot-leak-ai-password-flaws-20-stories/
tags:
- veille-cyber
- hackernews
---
## Panorama des menaces cybernétiques actuelles

Les acteurs malveillants continuent de diversifier leurs tactiques, ciblant diverses plateformes et secteurs. La sophistication des attaques augmente, nécessitant une vigilance constante de la part des défenseurs.

**Points Clés:**

*   **Évolution des ransomwares :** Le ransomware LockBit 5.0, avec sa capacité à cibler les environnements virtualisés comme Proxmox et ses techniques d'évasion avancées, démontre la progression des groupes RaaS.
*   **Sophistication des attaques d'ingénierie sociale :** La campagne ClickFix, évoluant avec des couches d'obfuscation complexes ("Matryoshka") et des techniques d'évasion, cible spécifiquement les utilisateurs macOS via des sites web frauduleux et des commandes Terminal déguisées.
*   **Abus des outils légitimes :** L'utilisation abusive d'outils comme RMM (Remote Monitoring and Management) et les plateformes d'entreprise comme Jira Cloud, permet aux attaquants de se dissimuler et d'opérer à grande échelle.
*   **Menaces spécifiques aux plateformes :**
    *   **Android 17 :** Introduit des améliorations de confidentialité, notamment la dépréciation de l'attribut `usesCleartextTraffic`.
    *   **macOS :** Cible les identifiants via des campagnes ClickFix sophistiquées et des infostealers comme Cuckoo Stealer.
    *   **Microsoft 365 Copilot :** Une faille a permis de résumer des e-mails confidentiels sans autorisation, contournant les politiques DLP.
*   **Attaques ciblées sur l'industrie :** Une augmentation significative des attaques par ransomware contre les organisations industrielles est observée, avec une croissance de 49% du nombre de groupes ciblés.
*   **Risques liés à la géopolitique et à la chaîne d'approvisionnement :** Des restrictions sont imposées sur les véhicules d'origine chinoise dans les installations militaires pour des raisons de sécurité nationale. Des groupes liés à l'Iran ciblent des secteurs critiques et de défense.
*   **Exploitation des vulnérabilités :** Des failles critiques dans les logiciels comme Ivanti EPMM et OpenSSL continuent d'être exploitées pour obtenir un accès persistant et exécuter du code à distance.
*   **Défis liés à l'IA :** Les mots de passe générés par des modèles linguistiques (LLM) peuvent présenter des faiblesses de sécurité dues à leur nature prédictive.
*   **Ingénierie sociale via le courrier électronique :** Les attaques par rejeu DKIM et l'abus de notifications légitimes de fournisseurs comme PayPal et DocuSign permettent de tromper les filtres de sécurité et de lancer des escroqueries.
*   **Ciblage de portefeuille :** Des campagnes associées à la Corée du Nord exploitent une porte dérobée dans MetaMask pour voler des identifiants de portefeuille cryptographique.

**Vulnérabilités Identifiées :**

*   **CVE-2021-22175 :** Vulnérabilité SSRF dans GitLab, requérant un correctif pour les agences fédérales américaines.
*   **CVE-2026-1281 et CVE-2026-1340 :** Vulnérabilités critiques dans Ivanti EPMM permettant l'exécution de code à distance sans authentification.
*   **CVE-2025-15467 :** Débordement de tampon dans OpenSSL lié au traitement des données CMS, potentiellement exécutable à distance.
*   **CVE-2025-11187 :** Débordement de tampon basé sur la pile dans OpenSSL dû à une validation manquante.
*   **CVE-2025-70401, CVE-2025-70402, CVE-2025-66500 :** Vulnérabilités dans les plateformes PDF de Foxit et Apryse permettant la prise de contrôle de compte et l'exécution de code.

**Recommandations :**

*   **Mettre à jour les logiciels :** Appliquer rapidement les correctifs pour les vulnérabilités critiques, notamment pour GitLab (CVE-2021-22175), Ivanti EPMM (CVE-2026-1281, CVE-2026-1340) et OpenSSL (CVE-2025-15467, CVE-2025-11187).
*   **Sécuriser les environnements :** Mettre en œuvre des configurations de sécurité réseau robustes, comme les fichiers Network Security Configuration pour Android 17.
*   **Renforcer la détection et la réponse :** Utiliser des solutions de sécurité capables de détecter les techniques d'évasion et les abus d'outils légitimes.
*   **Sensibiliser les utilisateurs :** Informer les utilisateurs sur les tactiques d'ingénierie sociale, les campagnes de phishing et les risques liés au téléchargement de logiciels à partir de sources non fiables.
*   **Gérer les comptes machines :** Configurer l'option `AccountNotDelegated` pour les comptes machines sensibles afin de limiter les risques de délégation.
*   **Éviter les méthodes de génération de mots de passe non sécurisées :** Ne pas utiliser les LLM pour générer des mots de passe ; privilégier des méthodes cryptographiquement sécurisées ou des gestionnaires de mots de passe.
*   **Auditer les systèmes :** Examiner les systèmes pour les indicateurs de compromission, en particulier pour les environnements ayant pu être affectés par des exploits comme ceux d'Ivanti EPMM.
*   **Contrôler l'accès aux environnements d'entraînement cloud :** Assurer que les applications de formation vulnérables ne sont pas accessibles depuis Internet.

---
[Source](https://thehackernews.com/2026/02/threatsday-bulletin-openssl-rce-foxit-0.html){:target="_blank"}
