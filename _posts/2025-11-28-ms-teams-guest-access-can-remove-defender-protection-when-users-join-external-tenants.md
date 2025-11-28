---
title: 'MS Teams Guest Access Can Remove Defender Protection When Users Join External Tenants'
date: 2025-11-28
permalink: /posts/2025/11/28/ms-teams-guest-access-can-remove-defender-protection-when-users-join-external-tenants/
tags:
- veille-cyber
- hackernews
---
### Contournement des protections Microsoft Defender via l'accès invité Teams

Une faille dans la fonctionnalité d'accès invité de Microsoft Teams permet de contourner les protections de Microsoft Defender pour Office 365. Lorsqu'un utilisateur rejoint un autre environnement (tenant) en tant qu'invité, les mesures de sécurité appliquées sont celles de l'environnement hôte, et non celles de son organisation d'origine.

Cette vulnérabilité est exacerbée par la nouvelle fonctionnalité de Teams permettant de discuter avec des utilisateurs externes via email, qui sera déployée globalement d'ici janvier 2026. L'invitation à rejoindre une conversation en tant qu'invité arrive par email et, provenant de l'infrastructure Microsoft, contourne les vérifications SPF, DKIM et DMARC, rendant le message difficile à identifier comme malveillant.

Une fois accepté, l'utilisateur devient un invité dans le tenant de l'attaquant, où il est soumis à des politiques de sécurité potentiellement inexistantes ou compromises. Un acteur malveillant peut créer un tenant avec des licences basiques (ne bénéficiant pas nativement de Defender pour Office 365) et désactiver toutes les protections. Il peut ensuite envoyer des liens de phishing ou des malwares via Teams, sans que l'organisation de la victime ne s'en aperçoive car l'attaque se déroule en dehors de ses propres contrôles de sécurité.

**Points Clés :**

*   L'accès invité dans Microsoft Teams applique les politiques de sécurité du tenant hôte.
*   La nouvelle fonctionnalité de discussion avec des utilisateurs externes par email peut être exploitée pour initier des attaques.
*   Les invitations par email contournent les contrôles d'authentification traditionnels (SPF, DKIM, DMARC).
*   Les environnements malveillants peuvent ne pas avoir les protections Defender pour Office 365 activées.

**Vulnérabilités :**

*   Le mécanisme d'accès invité de Teams ne transfère pas les protections de l'organisation d'origine.
*   La capacité d'un attaquant à créer des "zones sans protection" dans son propre tenant.
*   Le contournement potentiel des protections d'email grâce à l'origine de l'invitation (infrastructure Microsoft).

**Recommandations :**

*   Restreindre les invitations B2B aux domaines de confiance.
*   Implémenter des contrôles d'accès inter-tenants.
*   Limiter la communication externe sur Teams si elle n'est pas nécessaire.
*   Former les utilisateurs à identifier et signaler les invitations Teams non sollicitées provenant de sources externes.

---
[Source](https://thehackernews.com/2025/11/ms-teams-guest-access-can-remove.html){:target="_blank"}
