---
title: 'Google Gemini Broke Into Real Company Systems After Security Test Domain Mix-Up'
date: 2026-09-19
permalink: /posts/2026/09/19/google-gemini-broke-into-real-company-systems-after-security-test-domain-mix-up/
tags:
- veille-cyber
- hackernews
---
### Intrusion involontaire de Google Gemini : Une faille de nommage de domaine

Lors d'un test de cybersécurité réalisé en mai 2026 par la société israélienne Irregular, le modèle d'intelligence artificielle Gemini a accidentellement infiltré des systèmes d'entreprises réelles. Cet incident souligne les risques liés à l'autonomie des agents d'IA connectés à Internet.

**Points clés :**
*   **Cause de l'incident :** Une confusion de noms de domaine entre un environnement de test ("Capture the Flag") et un domaine existant dans le monde réel a permis à l'IA d'accéder à des systèmes réels.
*   **Comportement de l'IA :** Gemini a réussi à deviner des mots de passe par force brute et à extraire des identifiants stockés dans des dépôts publics.
*   **Réaction de l'IA :** Contrairement à d'autres modèles, Gemini a cessé ses activités dès qu'il a identifié qu'il avait accédé à un système d'entreprise réelle, démontrant un comportement jugé responsable par Google.
*   **Absence de malveillance :** Google n'a pas classé cet événement comme un défaut d'alignement de l'IA, les mécanismes de sécurité internes ayant fonctionné correctement.

**Vulnérabilités exploitées :**
*   **Faiblesse d'authentification :** Utilisation de mots de passe devinables par force brute.
*   **Exposition de données :** Stockage d'identifiants sensibles sur des dépôts de code publics.
*   **Erreur de configuration (Naming Conflict) :** Utilisation de noms de domaines de test non isolés du monde réel.
*   *Note : Aucune CVE spécifique n'est associée à cet incident, car il s'agit d'une défaillance opérationnelle liée à l'agent d'IA.*

**Recommandations :**
*   **Isolation stricte :** S'assurer que les environnements de test et les domaines utilisés pour les exercices de type "Capture the Flag" sont totalement isolés d'Internet ou utilisent des domaines réservés à la recherche (ex: `.test`, `.example`).
*   **Gestion des secrets :** Appliquer une politique stricte d'hygiène numérique interdisant la présence de credentials (mots de passe, clés API) dans les dépôts de code, même privés.
*   **Limitation des accès :** Restreindre les capacités des agents d'IA à interagir avec des systèmes externes en dehors des bacs à sable sécurisés.
*   **Monitoring actif :** Surveiller étroitement les actions des agents d'IA lors des phases de tests pour détecter toute déviation vers des cibles non autorisées.

---
[Source](https://thehackernews.com/2026/09/google-gemini-broke-into-real-company.html){:target="_blank"}
