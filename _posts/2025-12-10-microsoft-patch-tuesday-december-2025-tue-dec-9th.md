---
title: 'Microsoft Patch Tuesday December 2025, (Tue, Dec 9th)'
date: 2025-12-10
permalink: /posts/2025/12/10/microsoft-patch-tuesday-december-2025-tue-dec-9th/
tags:
- veille-cyber
- sans-isc
---
**Mises à jour de sécurité Microsoft : Décembre 2025**

La dernière série de correctifs de sécurité Microsoft résout 57 vulnérabilités, dont 3 critiques. Une vulnérabilité a déjà été exploitée, et deux étaient connues publiquement avant la publication des correctifs.

**Points clés :**

*   **Vulnérabilité exploitée activement :** CVE-2025-62221, une vulnérabilité d'élévation de privilèges dans le pilote Microsoft Cloud Files Mini Filters.
*   **Divulgations publiques :**
    *   CVE-2025-54100 : PowerShell utilisant `Invoke-WebRequest` peut exécuter des scripts inclus dans la réponse. Une mise en garde suggère l'utilisation du paramètre `-UseBasicParsing`.
    *   CVE-2025-64671 : Le plugin GitHub Copilot pour JetBrains peut entraîner une exécution de code à distance. Ce problème est lié à l'accès étendu des outils d'aide à la programmation basés sur l'IA dans les IDE.
*   **Vulnérabilités critiques :** Exécution de code à distance dans Microsoft Office et Outlook.

**Vulnérabilités notables et leurs CVE :**

*   **Élévation de privilèges :**
    *   CVE-2025-62221 (Pilote Microsoft Cloud Files Mini Filter, exploitée)
    *   CVE-2025-62455 (Microsoft Message Queuing - MSMQ)
    *   CVE-2025-62458 (Win32k)
    *   CVE-2025-62466 (Cache côté client Windows)
    *   CVE-2025-62469, CVE-2025-62569 (Système de fichiers de broking Microsoft)
    *   CVE-2025-62454, CVE-2025-62457 (Pilote Mini Filter de fichiers cloud Windows)
    *   CVE-2025-64679, CVE-2025-64680 (Bibliothèque de base DWM Windows)
    *   CVE-2025-64658 (Explorateur de fichiers Windows)
    *   CVE-2025-62571 (Installateur Windows)
    *   CVE-2025-62461, CVE-2025-62462, CVE-2025-62464, CVE-2025-55233, CVE-2025-62467 (Système de fichiers projeté Windows)
    *   CVE-2025-62472, CVE-2025-62474 (Gestionnaire de connexion d'accès à distance Windows)
    *   CVE-2025-64661 (Shell Windows)
    *   CVE-2025-64673 (Pilote VSP de stockage Windows)
    *   CVE-2025-59516, CVE-2025-59517 (Pilote VSP de stockage Windows)
*   **Exécution de code à distance :**
    *   CVE-2025-54100 (PowerShell, divulgation publique)
    *   CVE-2025-64671 (GitHub Copilot pour JetBrains, divulgation publique)
    *   CVE-2025-62552 (Microsoft Access)
    *   CVE-2025-62561, CVE-2025-62563, CVE-2025-62564, CVE-2025-62553, CVE-2025-62556, CVE-2025-62560 (Microsoft Excel)
    *   CVE-2025-62554, CVE-2025-62557 (Microsoft Office, critiques)
    *   CVE-2025-62562 (Microsoft Outlook, critique)
    *   CVE-2025-62555, CVE-2025-62558, CVE-2025-62559 (Microsoft Word)
    *   CVE-2025-62456 (Système de fichiers ReFS Windows)
    *   CVE-2025-62549, CVE-2025-64678 (Service RRAS Windows)
*   **Déni de service :**
    *   CVE-2025-62463, CVE-2025-62465 (Noyau graphique DirectX)
    *   CVE-2025-62567 (Hyper-V Windows)
*   **Divulgation d'informations :**
    *   CVE-2025-62570 (Serveur d'images de caméra Windows)
    *   CVE-2025-62468 (Service Pare-feu Windows Defender)
    *   CVE-2025-64670 (DirectX Windows)
    *   CVE-2025-62473 (Service RRAS Windows)
*   **Usurpation (Spoofing) :**
    *   CVE-2025-62223 (Microsoft Edge pour Mac)
    *   CVE-2025-64667 (Microsoft Exchange Server)
    *   CVE-2025-64672 (Microsoft SharePoint Server)

**Recommandations :**

Il est impératif d'appliquer les mises à jour de sécurité de Microsoft dès que possible pour corriger ces vulnérabilités. Une attention particulière doit être portée aux correctifs relatifs aux vulnérabilités critiques et à celles déjà exploitées ou publiquement divulguées.

---
[Source](https://isc.sans.edu/diary/rss/32550){:target="_blank"}
