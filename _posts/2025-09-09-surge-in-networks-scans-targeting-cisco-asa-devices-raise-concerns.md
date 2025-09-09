---
title: 'Surge in networks scans targeting Cisco ASA devices raise concerns'
date: 2025-09-09
permalink: /posts/2025/09/09/surge-in-networks-scans-targeting-cisco-asa-devices-raise-concerns/
tags:
- veille-cyber
- bleepingcomp
---
**Vague de balayages suspects ciblant les appareils Cisco ASA**

Une augmentation notable des balayages réseau ciblant les appareils Cisco ASA a été observée, suscitant des inquiétudes parmi les chercheurs en cybersécurité. Ces activités, détectées par GreyNoise à la fin du mois d'août, ont vu des milliers d'adresses IP uniques sonder les portails de connexion des ASA ainsi que les services Telnet/SSH de Cisco IOS. La deuxième vague de ces balayages était majoritairement imputable à un botnet brésilien. Les analyses des journaux révèlent l'utilisation d'agents utilisateurs similaires aux navigateurs Chrome, suggérant une origine commune. Les États-Unis, le Royaume-Uni et l'Allemagne ont été les régions les plus touchées.

Des observations antérieures ont montré qu'une telle activité de reconnaissance précède dans 80% des cas la divulgation de nouvelles vulnérabilités. Bien que la corrélation soit statistiquement plus faible pour Cisco, ces alertes peuvent aider les défenseurs à renforcer leur surveillance. Ces balayages peuvent être des tentatives d'exploitation d'anciennes failles corrigées, ou des efforts de cartographie en préparation de l'exploitation de nouvelles vulnérabilités.

Un rapport indépendant a également documenté une activité similaire, débutant fin juillet et culminant fin août, avec des centaines de milliers de requêtes enregistrées sur les appliances Cisco ASA.

**Points Clés :**

*   Augmentation significative des balayages réseau ciblant les appareils Cisco ASA.
*   Implication probable d'un botnet brésilien dans une partie de l'activité.
*   Utilisation d'agents utilisateurs similaires suggérant une origine commune.
*   La plupart des balayages ont ciblé les États-Unis.
*   L'activité de reconnaissance précède souvent la découverte de nouvelles vulnérabilités.
*   Les balayages peuvent concerner des failles déjà patchées ou préparer l'exploitation de nouvelles failles.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée directement dans l'article comme étant exploitée lors de ces balayages. L'article suggère que les balayages peuvent cibler des vulnérabilités connues et corrigées, ou préparer l'exploitation de futures failles.

**Recommandations :**

*   Appliquer les dernières mises à jour de sécurité sur les appareils Cisco ASA.
*   Mettre en œuvre l'authentification multi-facteurs (MFA) pour toutes les connexions à distance aux ASA.
*   Éviter d'exposer directement les interfaces `/+CSCOE+/logon.html`, WebVPN, Telnet ou SSH.
*   Si un accès externe est nécessaire, utiliser un concentrateur VPN, un proxy inverse ou une passerelle d'accès pour renforcer les contrôles d'accès.
*   Utiliser les indicateurs d'activité de balayage partagés pour bloquer préventivement ces tentatives.
*   Mettre en place des blocages géographiques et des limitations de débit pour les régions éloignées de l'organisation.

---
[Source](https://www.bleepingcomputer.com/news/security/surge-in-networks-scans-targeting-cisco-asa-devices-raise-concerns/){:target="_blank"}
