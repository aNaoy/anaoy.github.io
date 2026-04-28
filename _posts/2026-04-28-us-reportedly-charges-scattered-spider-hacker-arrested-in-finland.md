---
title: 'US reportedly charges Scattered Spider hacker arrested in Finland'
date: 2026-04-28
permalink: /posts/2026/04/28/us-reportedly-charges-scattered-spider-hacker-arrested-in-finland/
tags:
- veille-cyber
- bleepingcomp
---
### Arrestation d'un membre clé du groupe de cybercriminalité « Scattered Spider »

Un citoyen américain et estonien de 19 ans, connu sous le pseudonyme « Bouquet », a été arrêté en Finlande le 10 avril dernier. Il est accusé par la justice américaine d'être un membre actif du collectif de pirates informatiques **Scattered Spider** (également identifié sous les noms de *0ktapus, Octo Tempest* ou *UNC3944*). Il fait face à des poursuites pour fraude électronique, conspiration et intrusion informatique suite à son implication présumée dans plusieurs attaques visant de grandes entreprises mondiales.

**Points clés :**
*   **Mode opératoire :** Le groupe privilégie l'ingénierie sociale, le « MFA fatigue » (bombardement de notifications d'authentification multifacteur) et le phishing par SMS pour voler des identifiants.
*   **Tactique d'usurpation :** Les attaquants usurpent régulièrement l'identité d'employés auprès des services d'assistance informatique (helpdesk) pour réinitialiser les accès et compromettre des comptes administrateurs.
*   **Impact financier :** Les attaques ont engendré des millions de dollars de rançons, ainsi que des coûts de remédiation et de perturbation opérationnelle très élevés, même lorsque la rançon n'est pas payée.
*   **Contexte du groupe :** Composé principalement de jeunes adultes et d'adolescents, Scattered Spider est responsable de nombreuses cyberattaques de haut niveau (MGM Resorts, Caesars, Twilio, Reddit, etc.).

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, car les attaques reposent essentiellement sur des **vulnérabilités humaines et procédurales** (ingénierie sociale) plutôt que sur des failles logicielles exploitées directement par des exploits de type *zero-day*.

**Recommandations :**
*   **Renforcement du support technique :** Mettre en place des protocoles de vérification d'identité extrêmement stricts pour toute demande de réinitialisation de mot de passe ou de privilèges effectuée par téléphone ou messagerie.
*   **Éducation des utilisateurs :** Sensibiliser les employés aux risques de l'ingénierie sociale et à la dangerosité du « MFA fatigue » (ne jamais valider une demande d'authentification non sollicitée).
*   **Sécurisation du MFA :** Privilégier les méthodes d'authentification résistantes au phishing, comme les clés de sécurité matérielles (FIDO2/WebAuthn), plutôt que les codes SMS ou les notifications push classiques qui sont vulnérables aux techniques du groupe.

---
[Source](https://www.bleepingcomputer.com/news/security/us-reportedly-charges-scattered-spider-hacker-arrested-in-finland/){:target="_blank"}
