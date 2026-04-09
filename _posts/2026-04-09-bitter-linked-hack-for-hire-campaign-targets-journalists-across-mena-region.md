---
title: 'Bitter-Linked Hack-for-Hire Campaign Targets Journalists Across MENA Region'
date: 2026-04-09
permalink: /posts/2026/04/09/bitter-linked-hack-for-hire-campaign-targets-journalists-across-mena-region/
tags:
- veille-cyber
- hackernews
---
### Campagne d'espionnage « Hack-for-Hire » contre la société civile dans la région MENA

Des chercheurs ont identifié une campagne de cyber-espionnage persistante ciblant des journalistes, des militants et des officiels au Moyen-Orient et en Afrique du Nord (MENA). Attribuée au groupe de menace **Bitter** (soupçonné d'agir pour le compte du gouvernement indien), cette opération mêle ingénierie sociale sophistiquée, hameçonnage ciblé et déploiement de logiciels espions Android.

**Points clés :**
*   **Cibles :** Journalistes égyptiens et libanais, militants et figures politiques.
*   **Techniques :** Utilisation de faux profils sur les réseaux sociaux (LinkedIn), messages frauduleux via iMessage, WhatsApp et e-mail.
*   **Vecteurs d'attaque :**
    *   **Hameçonnage classique :** Pages usurpant le support Apple ou Google pour dérober des identifiants et des codes 2FA.
    *   **Attaques OAuth :** Utilisation de l'authentification Google OAuth pour obtenir un accès persistant via des applications tierces malveillantes.
    *   **Logiciels espions (Spyware) :** Distribution de malwares comme *ProSpy* et *Dracarys*, déguisés en plug-ins de chiffrement pour messageries (Signal, Telegram).
*   **Extension de domaine :** Les infrastructures utilisées présentent des liens techniques avec les campagnes passées de Bitter (ex: malware Dracarys), marquant une évolution probable de leurs tactiques vers le ciblage de la société civile.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est citée, car l'attaque repose principalement sur l'abus de fonctionnalités légitimes (OAuth 2.0, ingénierie sociale) et l'exécution de charges utiles malveillantes (APK) installées manuellement par la victime.

**Recommandations :**
*   **Méfiance vis-à-vis des demandes d'authentification :** Ne jamais accepter de permissions OAuth provenant de sources inconnues ou suspectes.
*   **Vérification des applications tierces :** Auditer régulièrement les comptes Google/Apple pour révoquer l'accès aux applications inconnues ou inutilisées.
*   **Sécurisation des messageries :** Éviter de cliquer sur des liens de « vérification » ou de « support » reçus par messagerie (iMessage, WhatsApp).
*   **Installation d'applications :** Télécharger uniquement des applications via les boutiques officielles (Google Play Store) et se méfier des prétendus « plug-ins de sécurité » ou « plug-ins de chiffrement » suggérés par des tiers.
*   **Authentification forte :** Utiliser des clés de sécurité physiques plutôt que des codes SMS pour la double authentification lorsque cela est possible.

---
[Source](https://thehackernews.com/2026/04/bitter-linked-hack-for-hire-campaign.html){:target="_blank"}
