---
title: 'New Interrupt Injection Attack Can Bypass Spectre v2 Defenses on Intel and AMD CPUs'
date: 2026-08-06
permalink: /posts/2026/08/06/new-interrupt-injection-attack-can-bypass-spectre-v2-defenses-on-intel-and-amd-cpus/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité par injection d'interruption : contournement des défenses Spectre v2

Des chercheurs du MIT CSAIL ont découvert une nouvelle méthode d'attaque, nommée « Interrupt Injection » (ou TONTOU), capable de contourner les protections contre les vulnérabilités Spectre v2 sur les processeurs Intel et AMD.

**Points clés :**
* **Mécanisme :** L'attaque exploite une faille temporelle (Time-of-Neutralization to Time-of-Use) : un utilisateur non privilégié déclenche une interruption matérielle précise juste après que le processeur a assaini son prédicteur de branchement, mais avant que le noyau ne l'utilise. Cela permet de « ré-empoisonner » le prédicteur.
* **Impact :** Sur un système AMD Zen 2, cette technique a permis de lire des données sensibles du noyau (comme le fichier `/etc/shadow`) avec un taux de réussite élevé.
* **Portée :** La vulnérabilité concerne principalement les systèmes partagés. AMD a confirmé que les processeurs Zen 1 à Zen 4 sont potentiellement vulnérables. Intel, de son côté, estime qu'aucune mitigation supplémentaire n'est nécessaire.
* **Complexité :** L'attaque nécessite l'exécution de code local, mais ne requiert aucun privilège spécifique. Elle utilise des gadgets de divulgation existants dans le noyau pour réussir l'exploitation.

**Vulnérabilités associées :**
* **CVE-2023-20569 (Inception) :** L'injection d'interruption utilise cette faille pour remplir le tampon de pile de retour avec une cible malveillante.
* **Aucun CVE spécifique** n'a été attribué à la technique d'injection d'interruption elle-même à ce jour.

**Recommandations :**
* **Mise à jour du noyau Linux :** Un correctif a été intégré dans le noyau Linux (commit `f5fdd6665ac4d8528ed1c9242cb1cf7a7f5bdb0e`). Il est crucial de s'assurer que le système utilise une version du noyau incluant cette correction, qui modifie la séquence « Safe-RET » pour ignorer l'exécution d'instructions sensibles après le retour d'une interruption.
* **Vérification :** Les administrateurs peuvent vérifier si leur système est corrigé en consultant la documentation relative à la protection contre le débordement de pile (SRSO) dans le noyau, bien que la transparence sur ce correctif spécifique reste limitée dans les bulletins officiels d'AMD.

---
[Source](https://thehackernews.com/2026/08/new-interrupt-injection-attack-can.html){:target="_blank"}
