---
title: 'Rogue NuGet Package Poses as Tracer.Fody, Steals Cryptocurrency Wallet Data'
date: 2025-12-16
permalink: /posts/2025/12/16/rogue-nuget-package-poses-as-tracerfody-steals-cryptocurrency-wallet-data/
tags:
- veille-cyber
- hackernews
---
## Vol de cryptomonnaies via un paquet NuGet malveillant

Une bibliothèque .NET de traçage, nommée "Tracer.Fody.NLog", a été identifiée comme un logiciel malveillant déguisé en outil légitime. Publié en février 2020 et présent sur le dépôt NuGet pendant près de six ans, ce paquet a été téléchargé au moins 2 000 fois.

Son fonctionnement consiste à se faire passer pour la bibliothèque légitime "Tracer.Fody", maintenue par "csnemes", en utilisant un nom d'utilisateur similaire ("csnemess"). Une fois intégré dans un projet, le paquet malveillant scanne les fichiers de portefeuille Stratis (".wallet.json") et leurs mots de passe associés dans le répertoire par défaut de Windows. Ces informations sensibles sont ensuite envoyées vers une adresse IP basée en Russie.

L'attaque a utilisé plusieurs tactiques pour échapper à la détection, notamment l'utilisation de caractères ressemblant à des lettres cyrilliques dans le code source et l'intégration de la routine malveillante dans une fonction d'aide générique ("Guard.NotNull") utilisée lors de l'exécution normale du programme. Les exceptions lors de l'exfiltration des données sont silencieusement ignorées, permettant au programme hôte de continuer à fonctionner sans erreur apparente tout en divulguant les informations du portefeuille.

Cette technique d'usurpation, appelée "typosquatting", où un paquet malveillant imite un paquet légitime en variant légèrement son nom, est une menace récurrente dans l'écosystème open-source. L'adresse IP utilisée pour l'exfiltration a déjà été associée à une attaque similaire en décembre 2023 visant la bibliothèque "AsyncEx".

**Points Clés :**

*   **Type de menace :** Paquet NuGet malveillant déguisé en bibliothèque de traçage .NET.
*   **Objectif :** Vol de données de portefeuilles de cryptomonnaies Stratis.
*   **Méthode :** Typosquatting du nom de la bibliothèque et de l'auteur, exfiltration silencieuse des données vers une infrastructure contrôlée par l'attaquant.
*   **Durée de la menace :** Présent sur le dépôt NuGet pendant environ six ans.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article, mais la technique utilisée repose sur l'ingénierie sociale et la confiance accordée aux dépôts de paquets.

**Recommandations :**

*   **Vigilance accrue lors de l'ajout de dépendances :** Vérifier attentivement le nom exact des paquets et le nom des auteurs, particulièrement pour les bibliothèques populaires.
*   **Analyse des paquets :** Examiner le code source des dépendances, si possible, pour identifier des comportements suspects.
*   **Utilisation d'outils de sécurité :** Employer des solutions de sécurité capables de détecter et de bloquer les paquets malveillants.
*   **Surveillance des infrastructures :** Les experts prévoient que des tactiques similaires pourraient être utilisées contre d'autres types de bibliothèques .NET courantes (journaux, validation d'arguments, utilitaires).

---
[Source](https://thehackernews.com/2025/12/rogue-nuget-package-poses-as-tracerfody.html){:target="_blank"}
