---
title: 'Zeabur shutting down after second security breach in two months'
date: 2026-10-21
permalink: /posts/2026/10/21/zeabur-shutting-down-after-second-security-breach-in-two-months/
tags:
- veille-cyber
- bleepingcomp
---
### Fin de service pour Zeabur suite à des failles de sécurité critiques

La plateforme d'hébergement Zeabur annonce sa fermeture définitive pour fin 2026 après avoir subi deux violations de données majeures en deux mois. Le dernier incident, survenu en octobre 2026, a permis à des attaquants d'accéder aux infrastructures partagées, aux serveurs dédiés et à la base de données de production en utilisant des identifiants internes stockés en clair.

**Points clés :**
* **Volume du vol de données :** 3,2 millions d'enregistrements de variables d'environnement et informations de 321 810 comptes exposés.
* **Impact technique :** Compromission de clusters dans neuf régions, accès root sur 101 serveurs GCP, ajout de clés SSH malveillantes et copie de 16 disques clients.
* **Cause racine :** Utilisation d'identifiants administrateur non chiffrés, non expirés et non renouvelés après le premier incident d'août 2026.
* **Issue :** La complexité croissante de la plateforme et l'incapacité à garantir une sécurité adéquate ont conduit l'entreprise à cesser ses activités (arrêt des services entre le 1er et le 31 décembre 2026).

**Vulnérabilités exploitées :**
* **Gestion des secrets :** Stockage d'identifiants et jetons d'accès en texte clair.
* **Absence de rotation des secrets :** Identifiants administrateur inchangés depuis janvier 2024.
* **Configuration réseau :** Portails d'administration exposés directement sur l'Internet public.
* **Défaut d'isolation :** Segmentation interne insuffisante entre les applications clientes et les systèmes critiques.
* *Note : Aucune CVE spécifique n'a été attribuée à ces erreurs de configuration.*

**Recommandations pour les utilisateurs :**
* **Rotation immédiate :** Changer impérativement tous les mots de passe, clés API et secrets stockés sur la plateforme.
* **Gestion des sessions :** Révoquer toutes les sessions actives liées à Zeabur.
* **Infrastructure :** Reconstruire intégralement les serveurs GCP potentiellement compromis.
* **Migration :** Sauvegarder les données et migrer les services vers des alternatives sécurisées avant l'arrêt définitif de la plateforme fin décembre.

---
[Source](https://www.bleepingcomputer.com/news/security/zeabur-shutting-down-after-second-security-breach-in-two-months/){:target="_blank"}
