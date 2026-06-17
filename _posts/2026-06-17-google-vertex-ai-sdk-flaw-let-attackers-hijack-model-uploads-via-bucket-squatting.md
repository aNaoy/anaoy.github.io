---
title: 'Google Vertex AI SDK Flaw Let Attackers Hijack Model Uploads via Bucket Squatting'
date: 2026-06-17
permalink: /posts/2026/06/17/google-vertex-ai-sdk-flaw-let-attackers-hijack-model-uploads-via-bucket-squatting/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans le SDK Google Vertex AI : L'attaque "Pickle in the Middle"

Une faille de sécurité dans le SDK Google Cloud Vertex AI pour Python permettait à des attaquants de détourner le processus d'upload de modèles de Machine Learning. En utilisant une technique de « bucket squatting » (squattage de compartiment de stockage), un attaquant pouvait intercepter les fichiers de la victime, les remplacer par des versions malveillantes et exécuter du code arbitraire au sein de l'infrastructure de Google.

**Points clés :**
* **Mécanisme de l'attaque :** Le SDK générait des noms de compartiments (buckets) Cloud Storage prévisibles basés sur l'ID du projet et la région. L'attaquant, anticipant ce nom, créait le bucket avant la victime pour intercepter l'upload.
* **Impact :** Une fois le modèle corrompu (souvent via les formats *pickle* ou *joblib*), l'attaquant pouvait injecter du code, voler des jetons OAuth, et accéder à des données sensibles (poids de modèles TensorFlow, métadonnées BigQuery, journaux, etc.).
* **Accessibilité :** Aucune authentification ni accès préalable au projet de la victime n'étaient requis ; seule la connaissance de l'ID du projet (souvent public) suffisait.
* **Complexité :** L'attaque reposait sur une exécution rapide (moins de 2,5 secondes) pour remplacer le modèle avant qu'il ne soit chargé par Vertex AI.

**Vulnérabilités :**
* Aucune référence CVE n'a été attribuée à cette faille spécifique, bien qu'elle s'inscrive dans une série de problèmes liés au nommage prévisible des buckets dans Vertex AI (notamment **CVE-2026-2473**, corrigée en février 2026).

**Recommandations :**
* **Mise à jour :** Mettre à jour immédiatement le SDK `google-cloud-aiplatform` vers la version **1.148.0 ou ultérieure**.
* **Configuration explicite :** Ne pas se fier aux valeurs par défaut du SDK. Définir manuellement le paramètre `staging_bucket` lors de l'utilisation de `Model.upload()` en spécifiant un bucket dont vous avez la maîtrise totale.
* **Périmètre d'application :** Appliquer ces mises à jour sur tous les environnements utilisant le SDK, y compris les notebooks de développement, les pipelines CI/CD et les environnements d'entraînement.

---
[Source](https://thehackernews.com/2026/06/google-vertex-ai-sdk-flaw-let-attackers.html){:target="_blank"}
