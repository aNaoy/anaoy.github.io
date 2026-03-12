---
title: 'Veeam warns of critical flaws exposing backup servers to RCE attacks'
date: 2026-03-12
permalink: /posts/2026/03/12/veeam-warns-of-critical-flaws-exposing-backup-servers-to-rce-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans Veeam Backup & Replication

Veeam a publié des correctifs pour plusieurs failles de sécurité majeures affectant sa solution *Backup & Replication* (VBR), un outil fréquemment ciblé par les groupes de ransomware pour compromettre les infrastructures d'entreprise et empêcher la restauration des données.

**Points clés :**
*   **Risque élevé :** Les serveurs de sauvegarde sont des cibles privilégiées pour les cyberattaquants afin de faciliter les mouvements latéraux et le vol de données.
*   **Historique :** Des groupes comme FIN7, Cuba, ainsi que les opérateurs des ransomwares Frag, Akira et Fog ont par le passé activement exploité les vulnérabilités de Veeam.
*   **Urgence :** La publication des correctifs accroît le risque d'ingénierie inverse par les attaquants ; une mise à jour immédiate est nécessaire.

**Vulnérabilités identifiées :**
*   **CVE-2026-21666, CVE-2026-21667, CVE-2026-21669 :** Trois failles RCE permettant à des utilisateurs du domaine faiblement privilégiés d'exécuter du code à distance avec une faible complexité d'attaque.
*   **CVE-2026-21708 :** Faille RCE permettant à un "Backup Viewer" d'exécuter du code à distance avec les privilèges de l'utilisateur *postgres*.
*   **Autres vulnérabilités :** Des failles de haute sévérité permettant l'élévation de privilèges, l'extraction de clés SSH et la manipulation de fichiers sur les dépôts de sauvegarde (*Backup Repository*).

**Recommandations :**
*   Mettre à jour immédiatement les serveurs Veeam Backup & Replication vers les versions **12.3.2.4465** ou **13.0.1.2067**.
*   Appliquer systématiquement tous les correctifs de sécurité dès leur disponibilité pour prévenir toute tentative d'exploitation après analyse des patchs par les attaquants.

---
[Source](https://www.bleepingcomputer.com/news/security/veeam-warns-of-critical-flaws-exposing-backup-servers-to-rce-attacks/){:target="_blank"}
