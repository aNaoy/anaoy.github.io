---
title: 'New CSS Attacks Can Break Webmail Defenses to Steal Passwords and Tokens'
date: 2026-08-08
permalink: /posts/2026/08/08/new-css-attacks-can-break-webmail-defenses-to-steal-passwords-and-tokens/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités CSS : Le danger caché dans vos e-mails

Des recherches récentes révèlent comment des attaques exploitant le CSS et le HTML permettent de briser les barrières de sécurité des services de messagerie web. Ces techniques permettent d'extraire des mots de passe, de dérober des jetons d'authentification, de détourner des actions d'interface utilisateur et de manipuler des outils d'IA intégrés.

**Points clés :**
*   **Technique :** Les attaques exploitent soit des éléments autorisés par les services de messagerie, soit des divergences entre les filtres de désinfection (sanitizers) et le rendu final par le navigateur.
*   **Vecteurs d'attaque :**
    *   **Détournement d'interface :** Utilisation de CSS pour superposer des éléments malveillants sur des interfaces légitimes (ex: faux champs de saisie Outlook).
    *   **Exfiltration de jetons :** Utilisation de techniques de clickjacking ou d'injection de style pour transmettre des données sensibles (jetons de connexion) à des serveurs tiers.
    *   **Manipulation d'IA :** Tromper les modèles d'IA lisant les e-mails avec du contenu caché (texte invisible via CSS) pour provoquer des actions non autorisées.
*   **Cibles identifiées :** Outlook, Gmail, Fastmail, Proton Mail, Yahoo Mail, et AOL Mail.

**Vulnérabilités :**
*   Le rapport ne mentionne pas de CVE spécifiques, mais documente des failles de logique et de parsing CSS sur les plateformes citées.
*   **Exemples :** "Label-jacking" sur Outlook, contournement de `image-set()` sur Gmail, et failles de mutation CSS sur Fastmail.

**Recommandations :**
*   **Isolation stricte :** Isoler systématiquement le contenu des e-mails HTML dans des `iframes` isolées (sandboxed).
*   **Filtrage rigoureux :** Restreindre strictement le CSS autorisé (utilisation de listes blanches), interdire les menus `select` et les sélecteurs CSS dangereux.
*   **Validation des attributs :** Vérifier les attributs personnalisés pour détecter les "gadgets" CSS avant toute exécution DOM.
*   **Contrôle des ressources :** Bloquer les requêtes d'images non autorisées et limiter les domaines sources pour prévenir les fuites de données.

---
[Source](https://thehackernews.com/2026/08/new-css-attacks-can-break-webmail.html){:target="_blank"}
