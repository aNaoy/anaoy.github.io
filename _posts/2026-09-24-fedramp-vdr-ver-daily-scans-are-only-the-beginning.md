---
title: 'FedRAMP VDR & VER: Daily Scans Are Only the Beginning'
date: 2026-09-24
permalink: /posts/2026/09/24/fedramp-vdr-ver-daily-scans-are-only-the-beginning/
tags:
- veille-cyber
- bleepingcomp
---
### FedRAMP 2026 : Le virage vers la validation continue

À compter du 7 décembre 2026, FedRAMP impose ses nouvelles règles de détection et de réponse aux vulnérabilités (VDR) et de vérification (VER). Cette transition marque la fin des modèles de conformité manuels et ponctuels au profit d'une approche d'ingénierie continue basée sur des preuves automatisées.

**Points clés :**
*   **Transition vers FedRAMP 20x :** Le modèle Rev5 devient obsolète. Le nouveau cadre impose une automatisation rigoureuse où les preuves de sécurité ne sont plus des documents artisanaux, mais des données machines en temps réel.
*   **Fréquence accrue :** La fréquence des scans de vulnérabilités dépend désormais de la classe de certification (de 14 jours pour la Classe A à quotidiennement pour la Classe D).
*   **Délais de remédiation stricts :** Les délais de correction sont drastiquement réduits, allant de 192 jours à seulement 12 heures pour les vulnérabilités critiques hautement exploitables.
*   **Preuve par défaut :** Le principe "Assume It's Automatable" (VER-EVA-AIA) oblige les fournisseurs à prouver qu'une vulnérabilité n'est pas automatisable, faute de quoi elle est considérée comme telle.
*   **Processus sous surveillance :** Toute défaillance dans les outils de détection est désormais elle-même classée comme une vulnérabilité.

**Vulnérabilités :**
L'article ne mentionne pas de CVE spécifiques, mais souligne que la "défaillance des processus de détection" est désormais traitée comme une vulnérabilité critique. La conformité n'est plus statique : une chaîne de pipeline de détection défaillante constitue une faille de sécurité opérationnelle immédiate.

**Recommandations :**
*   **Prioriser l'automatisation :** Abandonner la préparation de documents manuels au profit de systèmes récupérant les preuves directement depuis les outils techniques (SIEM, CI/CD, outils de configuration).
*   **Operationaliser la réponse :** Anticiper les astreintes et les processus de réponse aux incidents pour respecter les délais de remédiation très courts (jusqu'à 12 heures).
*   **Adopter une vision holistique :** Ne pas percevoir cette échéance comme un simple projet de mise en conformité temporaire, mais comme une restructuration durable des capacités de sécurité, réutilisable pour d'autres cadres (SOC 2, résilience européenne).
*   **Gérer la continuité :** Désigner des responsables pour la surveillance constante des outils de validation, afin d'éviter les interruptions invisibles qui pourraient compromettre la certification.

---
[Source](https://www.bleepingcomputer.com/news/security/fedramp-vdr-and-ver-daily-scans-are-only-the-beginning/){:target="_blank"}
