---
title: 'How infostealers turn stolen credentials into real identities'
date: 2026-02-19
permalink: /posts/2026/02/19/how-infostealers-turn-stolen-credentials-into-real-identities/
tags:
- veille-cyber
- bleepingcomp
---
## Les Voleurs d'Informations : De la Créneau Volée à l'Identité Réelle

Les logiciels malveillants de type "infostealer" modernes vont bien au-delà du simple vol de noms d'utilisateur et de mots de passe. Ils collectent désormais des données étendues telles que les cookies de navigateur, l'historique de navigation et des informations système. Ces ensembles de données sont ensuite agrégés et vendus, permettant aux attaquants de lier des informations techniques à des individus réels, leurs comportements et leurs affiliations professionnelles.

Une analyse de plus de 90 000 fuites provenant d'infostealers a révélé que ces informations, une fois combinées, permettent aux cybercriminels de passer d'une simple credential compromise à l'identification d'une personne, de son employeur et potentiellement de son rôle au sein d'une organisation. Cette convergence brouille la distinction entre identité personnelle et professionnelle, transformant une compromission sur un appareil personnel en un risque pour l'entreprise.

Les infostealers exploitent des données provenant d'une large gamme de services :

*   **Services professionnels et d'entreprise :** LinkedIn, GitHub, Microsoft Teams, Outlook et des domaines d'entreprise sont fréquemment ciblés. Cela facilite le phishing ciblé, l'ingénierie sociale et la priorisation des accès aux environnements d'entreprise, surtout en cas de réutilisation de mots de passe.
*   **Plateformes personnelles et sociales :** YouTube, Facebook et d'autres réseaux sociaux contiennent des informations qui facilitent la validation d'identité et le lien entre différents comptes.
*   **Services sensibles :** Des domaines gouvernementaux (comme l'IRS, la Canada Revenue Agency) et des plateformes pour adultes ont été trouvés. Les données issues de ces derniers peuvent être utilisées pour des campagnes d'extorsion.

L'efficacité persistante des infostealers s'explique par des comportements courants : installation d'applications illicites, réutilisation de mots de passe entre comptes personnels et professionnels, et stockage de credentials dans les navigateurs.

Pour atténuer l'impact de ces attaques, il est crucial de considérer que des identifiants sont déjà exposés. La réutilisation des mots de passe est un vecteur majeur d'exploitation.

### Points Clés

*   Les infostealers collectent désormais des données étendues au-delà des identifiants de connexion.
*   Ces données agrégées permettent d'établir un lien entre les identifiants volés et l'identité réelle d'un individu, son emploi et ses comportements.
*   La réutilisation des mots de passe est un facteur clé de succès pour les attaquants exploitant les données d'infostealers.
*   Une compromission sur un appareil personnel peut rapidement engendrer un risque pour l'entreprise en raison de la réutilisation des identifiants.

### Vulnérabilités

Bien que l'article ne mentionne pas de CVE spécifiques, il met en évidence les vulnérabilités intrinsèques liées à :

*   La **réutilisation des mots de passe** sur différents services, personnels et professionnels.
*   Le **stockage non sécurisé des identifiants** (dans les navigateurs, ou via des pratiques peu sûres).
*   L'absence d'une **surveillance continue des identifiants compromis** dans les environnements d'entreprise.

### Recommandations

*   **Mettre en place des politiques de mots de passe robustes** qui encouragent l'utilisation de phrases de passe longues.
*   **Scanner activement Active Directory** contre une base de données d'identifiants compromis connus pour bloquer la réutilisation.
*   **Éduquer les utilisateurs** sur les risques liés à la réutilisation des mots de passe et aux sources non fiables pour les téléchargements.
*   **Adopter une approche de sécurité continue** qui traite la sécurité des mots de passe comme une mesure de confinement active plutôt qu'une configuration statique.

---
[Source](https://www.bleepingcomputer.com/news/security/how-infostealers-turn-stolen-credentials-into-real-identities/){:target="_blank"}
