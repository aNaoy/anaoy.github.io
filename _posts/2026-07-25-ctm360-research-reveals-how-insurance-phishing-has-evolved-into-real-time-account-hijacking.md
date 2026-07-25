---
title: 'CTM360 Research Reveals How Insurance Phishing Has Evolved Into Real-Time Account Hijacking'
date: 2026-07-25
permalink: /posts/2026/07/25/ctm360-research-reveals-how-insurance-phishing-has-evolved-into-real-time-account-hijacking/
tags:
- veille-cyber
- hackernews
---
### L'évolution du phishing : vers le détournement de compte en temps réel

Les campagnes de phishing visant le secteur des assurances ont radicalement évolué, passant de la simple collecte différée d'identifiants à une technique de **détournement de session en temps réel**. Les attaquants agissent désormais comme des intermédiaires actifs entre la victime et le portail légitime de l'assureur.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation massive de publicités Google sponsorisées (Google Ads) pour attirer les victimes via des recherches liées à des devis ou des renouvellements d'assurance.
*   **Infrastructure éphémère :** Les attaquants exploitent des plateformes légitimes (GitHub Pages, Netlify, Wix, etc.) pour héberger leurs pages de phishing, rendant la détection par les méthodes traditionnelles de blocage de domaines moins efficace.
*   **Technique « InsureOTP Kit » :** Ce kit de phishing permet aux attaquants de gérer les sessions des victimes en direct, incluant l'interception et la retransmission immédiate des codes OTP (One-Time Password) vers le site officiel.
*   **Cibles étendues :** Bien que l'Arabie saoudite soit particulièrement visée, des activités ont été observées en Europe, aux États-Unis et en Inde.
*   **Changement de paradigme :** L'attaque complète se déroule en une seule session. Lorsque la victime termine le processus de connexion, l'attaquant a déjà pris le contrôle du compte.

**Vulnérabilités exploitées :**
*   Il n'y a pas de CVE spécifique mentionnée, car l'attaque repose sur l'ingénierie sociale et le détournement de processus d'authentification légitimes (interception de flux de connexion), plutôt que sur une faille logicielle directe.

**Recommandations :**
*   **Surveillance proactive :** Ne pas se limiter à la détection de domaines malveillants. Surveiller activement les publicités payantes usurpant la marque sur les moteurs de recherche.
*   **Analyse comportementale :** Détecter les anomalies dans les modèles d'authentification (ex: délais de saisie OTP suspects, sessions provenant d'infrastructures cloud inhabituelles).
*   **Renseignement sur les menaces (CTI) :** Passer d'une protection basée uniquement sur la marque (Digital Risk Protection) à une intelligence des menaces centrée sur les modes opératoires et l'infrastructure des attaquants.
*   **Sensibilisation :** Éduquer les utilisateurs à la prudence face aux liens sponsorisés sur les moteurs de recherche, même s'ils semblent mener vers des portails officiels.

---
[Source](https://thehackernews.com/2026/07/ctm360-research-reveals-how-insurance.html){:target="_blank"}
