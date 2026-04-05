---
title: 'Site-DOM-XSS using Cookie Injection: The AI Hackers are Coming Faster than You Think'
date: 2026-04-05
permalink: /posts/2026/04/05/site-dom-xss-using-cookie-injection-the-ai-hackers-are-coming-faster-than-you-think/
tags:
- veille-cyber
- zerodaysfans
---
### Vulnérabilité DOM-XSS par injection de cookie

Cet article expose une faille de type **DOM-based Cross-Site Scripting (DOM-XSS)** exploitant la manière dont une application gère les cookies, démontrant comment un attaquant peut manipuler le comportement d'une page Web via une injection.

**Points clés :**
*   **Mécanisme :** La vulnérabilité survient lorsqu'une application lit des données stockées dans un cookie sans les assainir correctement, puis les injecte directement dans le DOM (Document Object Model) de la page.
*   **Vecteur d'attaque :** Si un attaquant parvient à contrôler le contenu d'un cookie (via des techniques comme le *Cookie Tossing* ou une faille XSS sur un sous-domaine), il peut injecter des scripts malveillants qui s'exécuteront dans le contexte de la page victime.
*   **Risques :** Exécution de code JavaScript arbitraire, vol de sessions (cookies de session), détournement de clics ou exfiltration de données sensibles.

**Vulnérabilités associées :**
*   Bien qu'il s'agisse d'une faille de logique applicative spécifique (DOM-XSS), elle est classée sous les failles de type **CWE-79** (Improper Neutralization of Input During Web Page Generation).

**Recommandations :**
*   **Assainissement des entrées :** Ne jamais faire confiance aux données provenant du client, y compris les cookies. Toujours valider et assainir les données avant de les insérer dans le DOM.
*   **Utilisation des API sécurisées :** Privilégier l'utilisation de propriétés sécurisées comme `.textContent` ou `.innerText` au lieu de `.innerHTML` pour éviter l'interprétation de balises HTML/scripts injectés.
*   **Politique de cookies :** Appliquer les attributs `HttpOnly` (empêche l'accès au cookie via JavaScript) et `SameSite=Strict/Lax` pour limiter les risques d'injection et de vol de cookies.
*   **Content Security Policy (CSP) :** Mettre en place une CSP rigoureuse pour restreindre les sources d'exécution de scripts et empêcher l'exécution de scripts en ligne (inline).

---
[Source](https://medium.com/@renwa/site-dom-xss-using-cookie-injection-the-ai-hackers-are-coming-faster-than-you-think-3ef82f2a991d?source=rss-3f8ae70e3957------2){:target="_blank"}
