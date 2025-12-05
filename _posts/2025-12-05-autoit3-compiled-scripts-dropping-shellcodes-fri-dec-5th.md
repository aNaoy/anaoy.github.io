---
title: 'AutoIT3 Compiled Scripts Dropping Shellcodes, (Fri, Dec 5th)'
date: 2025-12-05
permalink: /posts/2025/12/05/autoit3-compiled-scripts-dropping-shellcodes-fri-dec-5th/
tags:
- veille-cyber
- sans-isc
---
### AutoIT3 : Une technique d'exécution de shellcode déguisée

Des scripts compilés en AutoIT3 sont utilisés pour dissimuler et exécuter des shellcodes, exploitant notamment la fonction `FileInstall()`. Cette fonction permet d'intégrer des fichiers dans un script compilé, qui seront ensuite extraits dans le répertoire temporaire lors de l'exécution.

Le shellcode est lui-même obfuscé par une simple transformation de caractères (décalage ASCII d'une unité) et est lu à partir d'un fichier intégré. Il est ensuite alloué dans une mémoire exécutable grâce à `VirtualAlloc` de `kernel32.dll`, copié dans cette mémoire, puis exécuté via un appel à `CallWindowProc` de `user32.dll`.

Cette méthode permet aux attaquants de rendre leurs malwares plus discrets en combinant l'obfuscation du langage de script avec des techniques d'exécution de code bas niveau.

**Points Clés:**

*   **Langage de script utilisé:** AutoIT3, connu pour sa facilité d'utilisation et sa capacité à compiler en exécutables autonomes.
*   **Fonction exploitée:** `FileInstall()`, permettant d'embarquer des fichiers dans des scripts compilés.
*   **Mécanisme d'exécution:** Extraction d'un fichier intégré dans le répertoire temporaire, lecture et désobfuscation d'un shellcode, allocation de mémoire exécutable (`VirtualAlloc`), copie du shellcode, et enfin exécution via `CallWindowProc`.
*   **Obfuscation:** Simple décalage ASCII appliqué aux caractères du shellcode.
*   **Malwares associés:** Des échantillons ont été observés livrant le RAT Quasar et le voleur d'informations Phantom.

**Vulnérabilités:**

Aucune vulnérabilité spécifique de type CVE n'est directement mentionnée dans cet article. La technique repose sur l'utilisation légitime de fonctions du langage AutoIT3 et des API Windows, détournées à des fins malveillantes.

**Recommandations:**

*   **Surveillance des scripts AutoIT3:** Portez une attention particulière aux scripts AutoIT3, surtout s'ils sont compilés et contiennent des fichiers intégrés via `FileInstall()`.
*   **Analyse de code :** Les analystes doivent être préparés à identifier et désobfusquer le code AutoIT3, ainsi qu'à analyser les shellcodes extraits.
*   **Solutions de sécurité :** Assurez-vous que vos solutions de sécurité (antivirus, EDR) sont capables de détecter les shellcodes injectés et les comportements d'exécution suspects, notamment les appels à `VirtualAlloc` et `CallWindowProc` avec des données potentiellement malveillantes.

---
[Source](https://isc.sans.edu/diary/rss/32542){:target="_blank"}
