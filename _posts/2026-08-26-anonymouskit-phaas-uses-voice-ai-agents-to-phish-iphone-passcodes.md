---
title: 'AnonyMousKIT PhaaS uses voice AI agents to phish iPhone passcodes'
date: 2026-08-26
permalink: /posts/2026/08/26/anonymouskit-phaas-uses-voice-ai-agents-to-phish-iphone-passcodes/
tags:
- veille-cyber
- bleepingcomp
---
### Menace AnonyMousKIT : Le Phishing par IA vocale cible les iPhone volés

La plateforme de "Phishing-as-a-Service" (PhaaS) baptisée AnonyMousKIT industrialise le vol de codes de déverrouillage et d'identifiants Apple pour les appareils perdus ou volés. Opérationnel depuis 2024, ce service s'appuie sur un vaste écosystème de revendeurs et sur l'intelligence artificielle pour tromper les victimes.

**Points clés :**
* **Automatisation :** Utilisation d'agents vocaux par IA (disposant de plusieurs "personnalités") pour appeler les victimes et les manipuler.
* **Ingénierie sociale :** Les attaquants se font passer pour le support Apple, utilisant des données réelles (modèle, IMEI) obtenues via le mode "Perdu" pour gagner la confiance des utilisateurs.
* **Vaste réseau :** La plateforme connecte 506 domaines et alimente 168 enseignes de revente.
* **Objectifs :** Récupérer les codes de déverrouillage, les identifiants Apple et les codes 2FA pour désactiver le verrouillage d'activation (Activation Lock), accéder aux sauvegardes iCloud, aux mots de passe (Keychain) et revendre les appareils débloqués.

**Vulnérabilités exploitées :**
* Il n'existe pas de CVE spécifique, car l'attaque repose sur l'exploitation de la confiance humaine (ingénierie sociale) plutôt que sur une faille logicielle. Le mécanisme de sécurité "Activation Lock" d'Apple est contourné par le vol direct des identifiants et des codes d'accès fournis par la victime elle-même.

**Recommandations :**
* **Méfiance envers les appels non sollicités :** Apple ne demandera jamais par téléphone ou par message de dicter un code de déverrouillage ou un mot de passe.
* **Vérification des sources :** Ne jamais saisir ses identifiants Apple sur un site autre que les domaines officiels d'Apple (appleid.apple.com ou icloud.com).
* **Sécurisation des accès :** Activer l'authentification à deux facteurs et ne jamais partager les codes reçus par SMS ou sur vos appareils de confiance.
* **Signalement :** En cas de perte d'un appareil, rester vigilant face aux communications prétendant provenir du support Apple et utiliser uniquement les outils officiels de localisation.

---
[Source](https://www.bleepingcomputer.com/news/security/anonymouskit-phaas-uses-voice-ai-agents-to-phish-iphone-passcodes/){:target="_blank"}
