---
title: 'Xen Hypervisor Flaws Let One Malicious VM Read and Write Any Other VMs Memory'
date: 2026-11-04
permalink: /posts/2026/11/04/xen-hypervisor-flaws-let-one-malicious-vm-read-and-write-any-other-vms-memory/
tags:
- veille-cyber
- hackernews
---
### Faille critique dans l'hyperviseur Xen : Risque d'évasion de VM

Deux vulnérabilités critiques affectant l'hyperviseur Xen permettent à une machine virtuelle (VM) malveillante de contourner son isolation, pour lire ou écrire directement dans la mémoire d'autres VM, y compris dans le domaine de contrôle (dom0). Ces failles, identifiées lors d'opérations de "grant copy", surviennent en raison d'une mauvaise gestion de la validation des permissions lors de copies groupées au sein d'une même page mémoire.

**Points clés :**
*   **Impact :** Une VM compromise peut prendre le contrôle total de l'hôte et de toutes les autres instances isolées.
*   **Versions affectées :** Toutes les versions de Xen depuis la 4.6 (les versions antérieures, comme la 4.5, ne sont pas concernées).
*   **Découverte :** Identifiées initialement par l'IA d'Anthropic, puis validées par des chercheurs en sécurité.

**Vulnérabilités :**
*   **CVE-2026-102703** et **CVE-2026-102704** (regroupées sous l'avis de sécurité **XSA-523**).

**Recommandations :**
*   **Appliquer les correctifs :** Mettre à jour immédiatement l'hyperviseur Xen vers les versions corrigées disponibles pour votre distribution ou plateforme (ex: XCP-ng 8.3, Qubes OS 4.3).
*   **Redémarrage obligatoire :** Un redémarrage complet de l'hôte est nécessaire après l'application des correctifs.
*   **Versions obsolètes :** Pour les utilisateurs de versions de Xen antérieures à la 4.17 (dont le support de sécurité a expiré), la mise à jour vers une version supportée est impérative, car aucun correctif ne sera fourni pour les anciennes branches.
*   **Cas spécifiques :** Pour les utilisateurs de Qubes OS, il est nécessaire de reseeller les phrases secrètes (Anti Evil Maid) suite à la modification des binaires Xen qui impacte les registres PCR18 et PCR19.

---
[Source](https://thehackernews.com/2026/11/xen-hypervisor-flaws-let-one-malicious.html){:target="_blank"}
