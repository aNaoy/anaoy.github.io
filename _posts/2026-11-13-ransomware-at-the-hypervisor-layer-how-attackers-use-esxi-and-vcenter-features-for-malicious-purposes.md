---
title: 'Ransomware at the hypervisor layer: how attackers use ESXi and vCenter features for malicious purposes'
date: 2026-11-13
permalink: /posts/2026/11/13/ransomware-at-the-hypervisor-layer-how-attackers-use-esxi-and-vcenter-features-for-malicious-purposes/
tags:
- veille-cyber
- securelist
---
### Ransomware : L'exploitation détournée des couches de virtualisation

L'analyse d'une récente attaque contre une infrastructure virtualisée démontre que les attaquants n'ont pas besoin d'exploiter des vulnérabilités complexes du hyperviseur (ESXi) pour causer des dégâts majeurs. En compromettant le plan de gestion (vCenter) par des identifiants volés, les attaquants ont utilisé des fonctionnalités légitimes pour détruire l'environnement et les sauvegardes.

**Points clés**
*   **Absence d'exploit "Zero-Day" :** L'attaque s'est appuyée sur l'usage détourné de commandes et d'outils d'administration officiels (living-off-the-land).
*   **Stratégie de destruction :** Les attaquants ont prioritairement neutralisé les infrastructures de sauvegarde avant de procéder au chiffrement des machines virtuelles.
*   **Asymétrie de visibilité :** La protection des machines virtuelles (EDR) est inopérante face à des manipulations effectuées directement au niveau du datastore ou du gestionnaire ESXi.
*   **Persistance :** Utilisation de services légitimes détournés (ex: *MeshAgent*, *Ligolo-ng*) et de services *systemd* malveillants pour maintenir l'accès.

**Vulnérabilités mentionnées**
Bien que l'attaque étudiée n'ait pas utilisé d'exploit direct, les vulnérabilités suivantes sont fréquemment exploitées dans ce type de campagne :
*   **CVE-2024-37085 :** Abus de l'intégration Active Directory (groupe ESX Admins) pour obtenir des droits d'administration complets sur ESXi.
*   **CVE-2021-22005 & CVE-2021-21972 :** Exécution de code à distance (RCE) sur vCenter.
*   **CVE-2024-40711 :** Vulnérabilité critique affectant les solutions de sauvegarde (Veeam), facilitant la compromission des plateformes de restauration.

**Recommandations de sécurité**
*   **Considérer vCenter comme un actif de "Tier 0" :** Isoler le plan de gestion des autres segments administratifs, limiter strictement les accès réseau et exiger une authentification multifacteur (MFA) résistante au phishing.
*   **Ségregation des identités :** Ne pas utiliser les comptes d'administration du domaine (AD) pour gérer l'infrastructure de virtualisation. Utiliser des comptes distincts avec le principe du moindre privilège.
*   **Durcir l'accès direct :** Restreindre l'accès SSH et le mode "Shell" d'ESXi. Surveiller toute modification des *Host Profiles* et des paramètres de sécurité (notamment l'option `execInstalledOnly`).
*   **Indépendance des sauvegardes :** Concevoir les sauvegardes comme une zone de sécurité autonome avec des identifiants d'administration distincts, afin d'éviter qu'une compromission de la production n'entraîne la destruction des capacités de restauration.
*   **Centralisation des logs :** Exporter systématiquement les journaux (auth.log, shell.log, vpxa.log) vers un système de gestion centralisé (SIEM) externe pour éviter leur suppression lors d'un incident.

---
[Source](https://securelist.com/esxi-ransomware/121959/){:target="_blank"}
