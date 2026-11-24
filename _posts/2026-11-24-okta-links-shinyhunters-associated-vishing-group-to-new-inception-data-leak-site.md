---
title: 'Okta Links ShinyHunters-Associated Vishing Group to New INCEPTION Data Leak Site'
date: 2026-11-24
permalink: /posts/2026/11/24/okta-links-shinyhunters-associated-vishing-group-to-new-inception-data-leak-site/
tags:
- veille-cyber
- hackernews
---
### Émergence du groupe INCEPTION : la menace du "vishing" persistante

Le groupe de cybercriminels **O-UNC-053**, anciennement lié au réseau ShinyHunters, a réapparu sous une nouvelle identité baptisée **INCEPTION**. Ce collectif se spécialise dans l'ingénierie sociale via le "vishing" (phishing vocal) pour compromettre des identifiants et contourner l'authentification multifacteur (MFA).

**Points clés :**
* **Mode opératoire :** Les attaquants contactent leurs cibles par téléphone, en se faisant passer pour des services d'assistance, afin d'obtenir la validation de notifications push ou le partage de codes temporaires (OTP).
* **Ciblage :** De nombreux secteurs sont visés (santé, finance, technologie, juridique, etc.) via des domaines frauduleux utilisant souvent des thématiques liées au département juridique (*legal*).
* **Infrastructure :** Les sites de phishing utilisent des kits sophistiqués qui filtrent les visiteurs : les victimes ciblées sont redirigées vers une fausse page de connexion, tandis que les autres sont renvoyées vers le portail officiel de l'organisation.
* **Extorsion :** Une fois l'accès aux applications SaaS obtenu, les données sensibles sont exfiltrées puis publiées sur le nouveau site de fuite de données d'INCEPTION pour faire pression sur les entreprises.

**Vulnérabilités :**
L'attaque ne repose pas sur une vulnérabilité logicielle spécifique (CVE), mais sur l'exploitation de la **faiblesse humaine** face aux méthodes d'authentification par notification push ou codes SMS, qui restent vulnérables aux attaques par interception et ingénierie sociale.

**Recommandations :**
* **Adopter l'authentification résistante au phishing :** Privilégier les méthodes basées sur les clés de sécurité matérielles (FIDO2/WebAuthn) ou les solutions comme Okta FastPass, qui sont immunisées contre le phishing classique et le vishing.
* **Sensibilisation :** Former les employés à ne jamais valider de notifications push ou communiquer de codes MFA par téléphone, même si l'appel semble provenir d'un service informatique ou juridique interne.
* **Veille sur les domaines :** Surveiller les enregistrements de nouveaux domaines utilisant le nom de l'entreprise avec des préfixes ou suffixes suspects (ex: *legal-<entreprise>.com*).
* **Politique de vérification :** Instaurer une procédure de rappel systématique pour valider l'identité de tout interlocuteur demandant une action sensible sur un compte utilisateur.

---
[Source](https://thehackernews.com/2026/11/okta-links-shinyhunters-associated.html){:target="_blank"}
