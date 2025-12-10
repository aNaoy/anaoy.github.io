---
title: 'Windows PowerShell now warns when running Invoke-WebRequest scripts'
date: 2025-12-10
permalink: /posts/2025/12/10/windows-powershell-now-warns-when-running-invoke-webrequest-scripts/
tags:
- veille-cyber
- bleepingcomp
---
### **Sécurité accrue pour Invoke-WebRequest dans PowerShell**

Windows PowerShell 5.1 intègre désormais une notification de sécurité lors de l'utilisation de la cmdlet `Invoke-WebRequest` pour télécharger du contenu web. Cette mesure vise à prévenir l'exécution de code potentiellement malveillant et pallie une vulnérabilité critique (CVE-2025-54100) qui affectait principalement les environnements d'entreprise automatisés par des scripts PowerShell.

La mise à jour, appliquée via les correctifs KB5074204 (pour Windows 11) et KB5074353 (pour Windows Server 2022), ajoute une invite de confirmation. L'utilisateur est alerté que des scripts contenus dans la page téléchargée pourraient s'exécuter. Par défaut, ignorer cette invite (en appuyant sur 'Entrée' ou en sélectionnant 'Non') annule l'opération et suggère l'utilisation du paramètre `-UseBasicParsing` pour un traitement plus sûr. Choisir 'Oui' confirme l'acceptation du risque d'exécution de scripts embarqués, tandis que 'Non' interrompt l'action par mesure de protection.

Cette nouvelle fonctionnalité est similaire à celle déjà présente dans PowerShell 7. Il est important de noter que la commande `curl` étant aliasée à `Invoke-WebRequest`, les mêmes avertissements s'appliqueront lors de son utilisation dans des scripts.

**Points Clés :**

*   PowerShell 5.1 alerte désormais sur les risques d'exécution de scripts lors de l'utilisation de `Invoke-WebRequest`.
*   Cette mesure est une réponse à la vulnérabilité CVE-2025-54100.
*   Une invite de confirmation permet à l'utilisateur de continuer ou d'annuler l'opération.
*   Le paramètre `-UseBasicParsing` est recommandé pour éviter l'exécution de scripts.
*   L'alias `curl` vers `Invoke-WebRequest` est également concerné.

**Vulnérabilités :**

*   **CVE-2025-54100 :** Vulnérabilité de haute gravité liée à l'exécution de code à distance dans PowerShell, spécifiquement lors du traitement de contenu web téléchargé par `Invoke-WebRequest` sans précautions.

**Recommandations :**

*   **Pour les administrateurs :** Mettre à jour les scripts d'automatisation pour inclure explicitement le paramètre `-UseBasicParsing` afin d'éviter les blocages dus aux confirmations manuelles.
*   **Pour les utilisateurs :** Être vigilant face aux invites de sécurité et privilégier le paramètre `-UseBasicParsing` ou annuler les opérations suspectes pour assurer la sécurité du système.
*   Installer les mises à jour de sécurité pertinentes (KB5074204, KB5074353, etc.).

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-windows-powershell-now-warns-when-running-invoke-webrequest-scripts/){:target="_blank"}
