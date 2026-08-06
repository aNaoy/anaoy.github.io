---
title: 'Swiss government SharePoint breach compromised 200 accounts'
date: 2026-08-06
permalink: /posts/2026/08/06/swiss-government-sharepoint-breach-compromised-200-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque contre le gouvernement suisse : 200 comptes SharePoint compromis

Le BIT (Office fédéral de l'informatique et de la télécommunication) a détecté une intrusion sur ses serveurs SharePoint fin juillet 2026, entraînant la compromission des identifiants d'environ 200 comptes. Bien qu'aucune exfiltration de données sensibles n'ait été confirmée à ce stade, les autorités ont pris des mesures conservatoires strictes.

**Points clés :**
*   **Détection :** Activité inhabituelle repérée sur les serveurs SharePoint le 28 juillet 2026.
*   **Impact :** Environ 200 comptes compromis. Aucune donnée confidentielle ou hautement sensible n'était stockée sur cette plateforme.
*   **Investigation :** Le BIT collabore avec l'Office fédéral de la cybersécurité et Microsoft. Aucune revendication par un groupe de rançongiciel n'a été enregistrée.

**Vulnérabilités potentielles :**
L'attaque aurait exploité des failles corrigées lors du « Patch Tuesday » de juillet 2026, ciblant potentiellement :
*   **CVE-2026-56164 :** Vulnérabilité d'élévation de privilèges dans SharePoint (activement exploitée).
*   **CVE-2026-50522 :** Faille critique d'exécution de code à distance (RCE) permettant le vol de clés de chiffrement serveur.

**Recommandations et mesures prises :**
*   **Réponse immédiate :** Blocage de l'accès internet externe aux serveurs SharePoint et réinitialisation des mots de passe des comptes affectés.
*   **Assainissement :** Réinstallation préventive des serveurs compromis par les équipes techniques.
*   **Continuité :** Utilisation de méthodes alternatives sécurisées pour le partage de documents en attendant la restauration des services.
*   **Hygiène sécuritaire :** Application rigoureuse des correctifs de sécurité (Patch Management) dès leur publication par les éditeurs pour prévenir l'exploitation de failles connues.

---
[Source](https://www.bleepingcomputer.com/news/security/swiss-government-sharepoint-breach-compromised-200-accounts/){:target="_blank"}
