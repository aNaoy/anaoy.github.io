---
title: 'Researchers Show a Single Malicious Webpage Visit Can Compromise Tor Browser'
date: 2026-07-29
permalink: /posts/2026/07/29/researchers-show-a-single-malicious-webpage-visit-can-compromise-tor-browser/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans Firefox et Tor Browser

Une faille de sécurité majeure dans le compilateur JIT (Just-In-Time) de Firefox permet à un attaquant d'exécuter du code arbitraire sur le système de la victime par la simple consultation d'une page web malveillante. Cette vulnérabilité affecte également le navigateur Tor, qui intègre les versions vulnérables de Firefox.

**Points clés :**
*   **Mécanisme :** La faille provient d'une erreur dans la gestion des optimisations du compilateur JIT. Une opération de modification de mémoire était incorrectement étiquetée comme une simple lecture, permettant à l'optimiseur de réutiliser un pointeur obsolète (stale pointer) après que la mémoire associée a été libérée.
*   **Chaînage d'attaques :** La vulnérabilité est utilisée dans une chaîne d'exploitation nommée "IonStack", capable d'aboutir à une élévation de privilèges (root) sur Android 17 en combinaison avec une faille du noyau Linux baptisée "GhostLock".
*   **Portée :** Les versions de Firefox de 147 à 151.0.2 sont concernées.

**Vulnérabilités identifiées :**
*   **CVE-2026-10702 :** Faille d'exécution de code arbitraire dans le processus de rendu de Firefox (critique).
*   **CVE-2026-43499 (GhostLock) :** Vulnérabilité au niveau du noyau Linux (futex) permettant une compromission totale du système.

**Recommandations :**
*   **Mise à jour immédiate :** Appliquer sans délai la mise à jour vers **Firefox 151.0.3** ou une version ultérieure pour bloquer le point d'entrée initial de l'attaque.
*   **Utilisateurs de Tor :** Veiller à installer les mises à jour du navigateur Tor dès leur disponibilité, car elles intègrent le correctif de sécurité de Mozilla.
*   **Correction système :** Bien que la mise à jour du navigateur stoppe l'exploitation initiale, elle ne corrige pas la faille GhostLock (CVE-2026-43499) au niveau du noyau ; une mise à jour complète du système d'exploitation est nécessaire pour protéger le noyau contre d'autres vecteurs d'attaque.

---
[Source](https://thehackernews.com/2026/07/researchers-show-single-malicious.html){:target="_blank"}
