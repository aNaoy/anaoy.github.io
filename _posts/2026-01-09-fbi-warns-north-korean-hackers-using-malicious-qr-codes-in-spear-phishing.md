---
title: 'FBI Warns North Korean Hackers Using Malicious QR Codes in Spear-Phishing'
date: 2026-01-09
permalink: /posts/2026/01/09/fbi-warns-north-korean-hackers-using-malicious-qr-codes-in-spear-phishing/
tags:
- veille-cyber
- hackernews
---
**Nouvelle Tendance de Cybercriminalité : L'Usage des QR Codes Malveillants par des Hackers Nord-Coréens**

Des acteurs de cybercriminalité soutenus par l'État nord-coréen, notamment le groupe Kimsuky (également connu sous les noms d'APT43, Black Banshee, Emerald Sleet, Springtail, TA427, et Velvet Chollima), utilisent activement des codes QR malveillants dans des campagnes de spear-phishing. Ces attaques visent des organisations gouvernementales, des think tanks et des institutions académiques aux États-Unis et à l'étranger. Cette méthode, appelée "quishing", exploite le fait que les codes QR redirigent les utilisateurs vers des appareils mobiles, potentiellement moins sécurisés que les postes de travail d'entreprise, contournant ainsi les défenses traditionnelles.

Le groupe Kimsuky a déjà été identifié pour sa capacité à exploiter des configurations DMARC défectueuses afin de falsifier des adresses électroniques légitimes. Les attaques récentes utilisant des QR codes malveillants ont pris plusieurs formes :

*   Emails de spoofing se faisant passer pour des conseillers étrangers ou des employés d'ambassades, invitant les destinataires à scanner un QR code pour accéder à des questionnaires ou à des documents via de faux liens de connexion, dans le but de voler des informations ou des identifiants Google.
*   Emails usurpant l'identité d'employés de think tanks, incitant au scan d'un QR code pour accéder à une infrastructure sous le contrôle des attaquants pour des actions ultérieures.
*   Invitations à des conférences inexistantes, le QR code renvoyant vers une page d'inscription frauduleuse visant à collecter des identifiants de compte Google.

Le FBI a également noté que ces opérations de quishing aboutissent souvent au vol de tokens de session, permettant aux attaquants de contourner l'authentification multifacteur (MFA) et de compromettre des identités cloud sans déclencher d'alertes de MFA échouée. Ces attaques sont considérées comme une méthode d'intrusion "résiliente à la MFA" dans les environnements d'entreprise, car elles débutent sur des appareils mobiles non gérés, échappant ainsi aux dispositifs de sécurité traditionnels comme l'EDR. En décembre 2025, Kimsuky avait également utilisé des QR codes dans des emails pour distribuer un nouveau variant de malware Android appelé DocSwap.

**Points Clés :**

*   Le groupe Kimsuky, affilié à la Corée du Nord, est à l'origine de ces campagnes.
*   L'utilisation de codes QR malveillants ("quishing") est une nouvelle tactique pour contourner les défenses de sécurité.
*   Les QR codes redirigent les utilisateurs vers des appareils mobiles, souvent moins protégés.
*   Les attaques visent à voler des identifiants, des tokens de session et à obtenir un accès persistant aux réseaux.
*   Ces attaques sont considérées comme une menace sérieuse, résiliente à la MFA.

**Vulnérabilités exploitées :**

*   Conceptions de sécurité des appareils mobiles moins robustes que celles des postes de travail d'entreprise.
*   La tendance des utilisateurs à faire confiance aux codes QR.
*   La capacité des attaquants à contourner l'authentification multifacteur par le biais du vol de tokens de session.
*   Potentiellement, des vulnérabilités dans la configuration DMARC, bien que cela concerne davantage les emails de spoofing précédant le QR code.

**Recommandations :**

*   Faire preuve d'une extrême prudence face aux QR codes présents dans des emails non sollicités ou suspects.
*   Vérifier la légitimité de l'expéditeur avant de scanner un QR code.
*   Éviter de scanner des QR codes provenant de sources inconnues ou douteuses.
*   Sensibiliser les employés à cette nouvelle méthode d'attaque.
*   Renforcer les politiques de sécurité pour les appareils mobiles accédant aux ressources de l'entreprise.
*   Mettre en place des solutions de détection et de réponse avancées, capables de surveiller les activités suspectes, même sur les appareils mobiles.

---
[Source](https://thehackernews.com/2026/01/fbi-warns-north-korean-hackers-using.html){:target="_blank"}
