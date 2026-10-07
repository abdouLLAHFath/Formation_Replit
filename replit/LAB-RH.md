# LAB-RH · Tri et score de CV

> **En une phrase —** Un poste à pourvoir chez Atelier Nova, des CV fictifs importés, une IA qui extrait et score sans jamais décider, et un recruteur qui garde la main jusqu'au bout.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 2 h 40 (9 étapes) | Nouveau projet `Web app`, `rh-tri-cv` | LAB-SOCLE |

## 🎯 À la fin de ce lab
- Un cahier des charges v0 et un plan de développement, obtenus en mode Plan.
- Une clé DeepSeek dans les Secrets, jamais écrite en dur.
- Un tableau de candidatures avec score, explication et questions d'entretien générées par l'IA.
- Une décision humaine (Retenir / Écarter / À revoir) clairement distincte du score.
- Trois cas piégés corrigés, et les biais testés.

> Données fournies : [`data/fiche-poste-coordinateur.md`](data/fiche-poste-coordinateur.md) et [`data/candidats.csv`](data/candidats.csv) — dix candidatures fictives, dont des cas piégés.

---

## Étape 1 · Cahier des charges en Plan · ⏱️ 20 min

1. Créez le projet `rh-tri-cv`.
2. Mode **Plan**.

📋 **Prompt à coller (en Plan)**

```text
Je veux une application qui aide à recruter un·e coordinateur·rice
administratif·ve pour Atelier Nova, agence d'événementiel. Les
administrateurs créent une offre (titre, description, compétences,
lieu, type de contrat), puis téléversent des CV pour cette offre.
Pose-moi les questions nécessaires, puis propose un cahier des
charges v0 : user stories, critères d'acceptation, hors périmètre.
```

> [!TIP]
> **✅ Vous devez voir**
> 3 à 5 user stories, des critères d'acceptation, et un hors périmètre écrit noir sur blanc. Aucun fichier modifié.

## Étape 2 · Plan de développement · ⏱️ 15 min

📋 **Prompt à coller (en Plan)**

```text
Découpe ce cahier des charges en étapes de construction, chacune
testable séparément avant de passer à la suivante.
```

> [!TIP]
> **✅ Vous devez voir**
> Un plan en étapes numérotées, chacune avec un test associé.

## Étape 3 · Clé DeepSeek dans les Secrets · ⏱️ 15 min

1. Ouvrez **Tools › Setup › Secrets**, cliquez sur **New Secret**.
2. Nom : `DEEPSEEK_API_KEY`. Valeur : la clé de test fournie par le formateur.

> [!WARNING]
> ⚠️ Ne collez **jamais** cette clé ailleurs que dans ce champ : pas dans le chat, pas dans un fichier, pas dans la Console.

📋 **Prompt à coller (en Build)**

```text
Fais un appel de test au modèle DeepSeek en lisant la clé
DEEPSEEK_API_KEY depuis les Secrets, jamais écrite en dur dans le
code. Demande-lui de répondre « test réussi » et affiche le résultat.
```

> [!TIP]
> **✅ Vous devez voir**
> « test réussi » affiché, et dans le code une lecture par variable d'environnement — jamais la valeur de la clé.

## Étape 4 · Tableau des candidatures · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Ajoute un écran avec la fiche de poste en lecture seule, et un
formulaire pour importer les dix candidatures du fichier fourni
(nom, téléphone, ville, CV joint). Affiche-les dans un tableau :
nom, ville, statut.
```

> [!TIP]
> **✅ Vous devez voir**
> Les dix candidatures dans le tableau, la fiche de poste non modifiable.

## Étape 5 · Score et explication · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Pour chaque candidature, utilise DeepSeek pour extraire identité,
formation, expérience, preuves de français, puis calcule un score de
0 à 100 d'adéquation avec la fiche de poste, avec une explication
écrite du score. Une information absente doit rester « inconnue »,
jamais inventée.
```

> [!TIP]
> **✅ Vous devez voir**
> Un score et une explication pour chaque candidature. Vérifiez une candidature à la main : le score correspond à l'explication donnée.

## Étape 6 · Questions d'entretien · ⏱️ 15 min

📋 **Prompt à coller (en Build)**

```text
Pour chaque candidature, génère 5 à 8 questions d'entretien en
français, fondées sur le CV et la fiche de poste — jamais des
questions génériques déconnectées du profil.
```

> [!TIP]
> **✅ Vous devez voir**
> Entre 5 et 8 questions par candidature, qui citent un élément précis du CV.

## Étape 7 · Décision humaine · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Ajoute un écran de décision humaine : pour chaque candidature, le
recruteur choisit Retenir / Écarter / À revoir, avec un commentaire
et une date. Cette décision doit s'afficher à côté du score de l'IA,
clairement distincte de lui.
```

1. Marquez **CAND-01** (le mieux noté par l'IA) « À revoir » avec un commentaire.
2. Vérifiez que son classement affiché en tient compte, et que le score de l'IA seul ne décide plus rien.

> [!TIP]
> **✅ Vous devez voir**
> La décision humaine visible à côté du score, jamais fusionnée avec lui.

## Étape 8 · Cas piégés des CV · ⏱️ 20 min

Pour chaque cas, appliquez la méthode en cinq temps : expliquer en Plan, choisir la cause, corriger en Build, tester, revenir au point de retour si ça aggrave.

| Cas | Ce qu'on vérifie |
|---|---|
| **CAND-04** (CV mal mis en forme) | Le score reflète les informations réelles, pas la mauvaise mise en forme. |
| **CAND-05 / CAND-06** (profils quasi identiques) | Un score identique ; sinon, corrigez et recalculez. |
| **CAND-03** (candidature incomplète) | Les champs manquants restent « inconnu », jamais inventés. |

> [!TIP]
> **✅ Vous devez voir**
> Les trois cas corrigés, avec une seule correction ciblée par cas.

## Étape 9 · Biais et RGPD · ⏱️ 15 min

📋 **Prompt à coller (en Plan)**

```text
Explique comment le score pourrait être influencé par l'âge, le
genre ou l'origine déductibles du CV, et liste toutes les données
personnelles actuellement stockées pour une candidature.
```

> [!WARNING]
> ⚠️ Si l'explication identifie un biais possible, corrigez le prompt de scoring en Build pour l'exclure explicitement, puis retestez sur deux candidatures qui ne diffèrent que par ce critère.

> [!TIP]
> **✅ Vous devez voir**
> La liste des données personnelles stockées, et un score qui ne change pas quand seul l'âge ou le prénom change.

---

## ✅ Point de contrôle
- [ ] Cahier des charges v0 et plan de développement écrits.
- [ ] Clé DeepSeek testée, absente du code et du chat.
- [ ] Score, explication et questions générés pour les dix candidatures.
- [ ] Décision humaine distincte du score pour CAND-01.
- [ ] Trois cas piégés corrigés, biais testé, données personnelles listées.

## 🧠 À retenir
- Le score est une aide à la décision, jamais la décision elle-même.
- Une information absente reste inconnue : on ne la devine pas.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'appel DeepSeek échoue | Vérifiez l'orthographe exacte de `DEEPSEEK_API_KEY` dans le code généré. |
| CAND-05 et CAND-06 ont des scores différents | `Ces deux candidatures ont des compétences, une expérience et une formation identiques. Explique pourquoi leurs scores diffèrent, puis recalcule.` |
| La décision humaine disparaît au rechargement | Vérifiez qu'elle est bien enregistrée en base, pas seulement affichée côté écran. |

</details>

---

➡️ **Lab suivant :** [LAB-TICKETING · Suivi des demandes](LAB-TICKETING.md)
