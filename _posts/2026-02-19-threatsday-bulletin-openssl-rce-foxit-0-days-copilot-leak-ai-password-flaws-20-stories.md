---
title: 'ThreatsDay Bulletin: OpenSSL RCE, Foxit 0-Days, Copilot Leak, AI Password Flaws & 20+ Stories'
date: 2026-02-19
permalink: /posts/2026/02/19/threatsday-bulletin-openssl-rce-foxit-0-days-copilot-leak-ai-password-flaws-20-stories/
tags:
- veille-cyber
- hackernews
---
**Tendances Actuelles dans le Paysage de la Cybersécurité**

Les développements récents mettent en évidence une évolution constante des menaces et des tactiques des acteurs malveillants, touchant diverses plateformes et secteurs.

**Points Clés :**

*   **Évolution des Ransomwares :** Le ransomware LockBit 5.0 présente des techniques d'évasion avancées et une capacité à cibler les environnements de virtualisation comme Proxmox. La popularité des attaques par ransomware visant le secteur industriel est en hausse.
*   **Campagnes de Social Engineering :** La tactique "ClickFix" continue d'évoluer, utilisant une obfuscation imbriquée pour tromper les utilisateurs de macOS. Des campagnes ciblent spécifiquement le vol d'identifiants via de faux sites de téléchargement de logiciels et de gestionnaires de paquets. L'utilisation de bots Telegram pour le phishing cible les grandes entreprises, tandis que des kits de phishing dédiés à Booking.com ciblent le secteur de l'hôtellerie et les clients.
*   **Exploitation de Logiciels :** Des vulnérabilités critiques dans Ivanti Endpoint Manager Mobile (EPMM) permettent l'exécution de code à distance et l'accès persistant. Des failles dans les moteurs PDF de Foxit et Apryse peuvent mener à des prises de contrôle de comptes. Le logiciel de surveillance et de gestion à distance (RMM) est de plus en plus abusé par les attaquants.
*   **Nouvelles Techniques d'Attaque :** L'abus des essais de Jira Cloud est utilisé pour des campagnes de spam. Les attaques par rejeu DKIM exploitent les factures légitimes pour contourner la sécurité. Le RAT Remcos évolue vers une surveillance en temps réel via webcam.
*   **Risques liés à l'IA et aux Protocoles :** Les mots de passe générés par les grands modèles linguistiques (LLM) manquent de caractère aléatoire sécurisé. Les vulnérabilités dans OpenSSL permettent l'exécution de code à distance. La délégation Kerberos s'applique également aux comptes machine, élargissant le risque.
*   **Ciblage Géopolitique :** Les véhicules fabriqués en Chine sont interdits d'accès aux installations militaires polonaises par mesure de sécurité. Des poursuites judiciaires au Texas visent des entreprises technologiques chinoises pour des accusations d'accès à des données et de risques de cybersécurité.
*   **Campagnes Coordonnées :** Une campagne liée à la Corée du Nord cible les professionnels de la cryptomonnaie et de l'IA, incluant une attaque sur l'extension MetaMask.

**Vulnérabilités Identifiées :**

*   **CVE-2025-15467** : Vulnérabilité de débordement de tampon dans OpenSSL permettant l'exécution de code à distance.
*   **CVE-2025-11187** : Vulnérabilité de débordement de tampon dans OpenSSL due à un manque de validation.
*   **CVE-2021-22175** : Vulnérabilité de "Server-Side Request Forgery" (SSRF) dans GitLab.
*   **CVE-2026-1281 et CVE-2026-1340** : Vulnérabilités critiques dans Ivanti Endpoint Manager Mobile (EPMM) permettant l'exécution de code à distance.
*   **CVE-2025-70401, CVE-2025-70402, CVE-2025-66500** : Vulnérabilités dans les plateformes PDF de Foxit et Apryse.

**Recommandations :**

*   **Mise à Jour des Systèmes :** Appliquer les correctifs de sécurité rapidement, notamment pour GitLab (CVE-2021-22175) et Ivanti EPMM (CVE-2026-1281, CVE-2026-1340).
*   **Configuration de Sécurité :** Migrer vers des fichiers de configuration de sécurité réseau pour un contrôle granulaire du trafic clairtext sur Android.
*   **Vigilance face au Phishing et au Social Engineering :** Être particulièrement prudent face aux e-mails, messages et demandes provenant de sources inattendues ou non vérifiées, surtout s'ils incitent à cliquer sur des liens ou à télécharger des fichiers.
*   **Sécurisation des Comptes :** Les administrateurs doivent s'assurer que les comptes machine sensibles ne sont pas configurés pour la délégation (ex: `Set-ADAccountControl -Identity “HOST01$” -AccountNotDelegated $true`).
*   **Utilisation Prudente de l'IA :** Ne pas utiliser les LLM pour générer des mots de passe. Les développeurs utilisant des assistants IA doivent vérifier la présence d'identifiants codés en dur et s'assurer que les agents utilisent des méthodes de génération de mots de passe sécurisées.
*   **Audit des Systèmes :** Examiner les systèmes pour des indicateurs de compromission, en particulier pour les vulnérabilités exploitées (comme celles dans Ivanti EPMM depuis l'été 2025).
*   **Renforcement des Défenses DLP :** S'assurer que les politiques de prévention de perte de données (DLP) sont correctement configurées et fonctionnent comme prévu, en particulier avec l'intégration d'outils d'IA.

---
[Source](https://thehackernews.com/2026/02/threatsday-bulletin-openssl-rce-foxit-0.html){:target="_blank"}
