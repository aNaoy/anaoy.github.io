---
title: 'Zendesk spam wave returns, floods users with Activate account emails'
date: 2026-02-05
permalink: /posts/2026/02/05/zendesk-spam-wave-returns-floods-users-with-activate-account-emails/
tags:
- veille-cyber
- bleepingcomp
---
**Vague de Spam par Zendesk : Utilisation Abusive des Formulaires de Support**

Une nouvelle vague de courriels indésirables submerge les boîtes de réception des utilisateurs, exploitant les systèmes de support Zendesk des entreprises. Ces courriels, souvent intitulés "Activez votre compte" ou des notifications similaires, semblent émaner de différentes sociétés et sont envoyés en grand nombre, submergeant les destinataires qui n'ont jamais sollicité ces communications.

Cette activité rappelle un incident similaire survenu en janvier, où des attaquants avaient exploité la capacité de Zendesk à permettre la soumission de tickets par des utilisateurs non vérifiés. Chaque ticket générait alors un courriel de confirmation, transformant les portails de support exposés en relais de spam à grande échelle. Bien que Zendesk ait depuis mis en place des mesures de sécurité, cette recrudescence suggère que l'exploitation des portails de tickets vulnérables reste possible.

**Points Clés :**

*   Utilisation abusive des formulaires de soumission de tickets Zendesk par des acteurs malveillants.
*   Génération massive de courriels de confirmation ("Activate account", notifications de support) ressemblant à des communications légitimes.
*   Les courriels contournent les filtres anti-spam en étant envoyés depuis des instances Zendesk réelles.
*   L'objectif précis de cette campagne n'est pas encore clairement établi, mais il s'agit probablement de submerger les utilisateurs ou d'autres motivations liées au spam.

**Vulnérabilités :**

*   L'article ne mentionne pas de CVE spécifiques. La vulnérabilité réside dans la conception de certaines configurations de Zendesk permettant à des utilisateurs non authentifiés de soumettre des tickets, déclenchant ainsi l'envoi d'emails.

**Recommandations :**

*   **Pour les entreprises utilisant Zendesk :**
    *   Restreindre la création de tickets aux utilisateurs vérifiés uniquement.
    *   Supprimer les champs génériques (placeholders) qui permettent l'utilisation de n'importe quelle adresse e-mail ou sujet de ticket.
    *   Mettre en œuvre des mesures de sécurité renforcées pour la détection d'activités inhabituelles sur les plateformes de support.
*   **Pour les utilisateurs :**
    *   Ignorer ces courriels indésirables et ne pas cliquer sur les liens qu'ils contiennent.
    *   Signaler les courriels comme spam si la fonction est disponible.

---
[Source](https://www.bleepingcomputer.com/news/security/zendesk-spam-wave-returns-floods-users-with-activate-account-emails/){:target="_blank"}
