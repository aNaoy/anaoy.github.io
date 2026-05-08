---
title: 'One Missed Threat Per Week: What 25M Alerts Reveal About Low-Severity Risk'
date: 2026-05-08
permalink: /posts/2026/05/08/one-missed-threat-per-week-what-25m-alerts-reveal-about-low-severity-risk/
tags:
- veille-cyber
- hackernews
---
### L'angle mort du SOC : Les risques cachés des alertes à faible priorité

L'analyse de 25 millions d'alertes de sécurité révèle une faille structurelle majeure dans les opérations de défense : la hiérarchisation basée sur la sévérité conduit les équipes SOC et MDR à ignorer systématiquement des menaces réelles. Cette pratique crée un angle mort où près de 1 % des alertes "faibles" ou "informationnelles" correspondent à des compromissions effectives, soit environ une brèche par semaine pour une organisation moyenne.

**Points clés**
*   **Échec du triage :** La gestion manuelle ou traditionnelle des alertes est saturée ; environ 60 % des alertes ne sont jamais examinées, faute de ressources humaines.
*   **Le mythe de l'EDR :** 51 % des points de terminaison confirmés comme compromis avaient été marqués comme « atténués » par les solutions EDR. L'analyse forensique de la mémoire révèle que des menaces actives persistent malgré ces outils.
*   **Évolution du phishing :** Les attaquants contournent les passerelles email en utilisant des plateformes légitimes (Vercel, PayPal, OneDrive) et des techniques de dissimulation avancées (fichiers SVG, métadonnées PDF, QR codes dans des fichiers DOCX).
*   **Stratégie cloud :** Les attaquants privilégient la persistance et l'évasion de défense (token manipulation) plutôt que l'impact immédiat, exploitant souvent des erreurs de configuration AWS/S3 banales.

**Vulnérabilités et menaces observées**
L'étude identifie l'utilisation active d'outils standards par des acteurs malveillants :
*   **Malwares en mémoire :** Mimikatz, Cobalt Strike, Meterpreter, StrelaStealer.
*   **Techniques d'évasion :** Utilisation de services légitimes pour héberger des infrastructures malveillantes, détournement de CAPTCHA pour bloquer les scanners de sécurité automatisés, et obfuscation via des fichiers encodés ou des annotations invisibles.

**Recommandations**
*   **Automatisation de l'investigation :** S'affranchir de la limitation humaine par l'usage de l'IA (type AI SOC) pour analyser la totalité du volume d'alertes, et non plus seulement une sélection par niveau de sévérité.
*   **Forensique systématique :** Ne pas se fier aveuglément au statut « atténué » des solutions EDR ; procéder à des analyses de mémoire sur les endpoints suspects.
*   **Boucle de rétroaction :** Utiliser les résultats de chaque investigation pour affiner et améliorer en continu les règles de détection à la source, brisant ainsi le cycle de l'ignorance institutionnalisée.
*   **Durcissement du cloud :** Prioriser la remédiation des erreurs de configuration dans les environnements cloud (notamment AWS S3), souvent classées « faible sévérité » mais essentielles pour stopper la persistance des attaquants.

---
[Source](https://thehackernews.com/2026/05/one-missed-threat-per-week-what-25m.html){:target="_blank"}
