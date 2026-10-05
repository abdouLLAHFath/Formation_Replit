# LAB-03 · Cahier des charges et plan de développement (mode Plan)

> **En une phrase —** Vous décrivez un besoin métier à l'Agent en mode Plan, il questionne et critique sans rien construire, et vous ressortez avec un cahier des charges v0 et un plan d'étapes testables.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 30 min | Nouveau projet `Web app` par fil rouge | LAB-02 |

## 🎯 À la fin de ce lab
- Vous avez utilisé le mode **Plan** : l'Agent a répondu sans modifier un seul fichier.
- Vous avez un **cahier des charges v0** (3 à 5 user stories, critères d'acceptation, hors périmètre) — repris au projet final.
- Vous avez un **plan de développement** découpé en étapes, chacune testable séparément.

> 🧵 **Choisissez votre fil rouge pour la journée : RH ou Finance.** Les deux parcours sont donnés ci-dessous ; suivez celui que vous avez choisi dans tous les labs suivants (ou faites les deux si le temps le permet).

---

## Étape 1 · Activer le mode Plan · ⏱️ 2 min

1. Créez un nouveau projet `Web app`, nommé `rh-tri-cv` (fil RH) ou `finance-cloture` (fil Finance).
2. Dans le sélecteur de mode de l'Agent, choisissez **Plan**.

> [!IMPORTANT]
> **🎛️ Ce que fait le mode Plan**
> Lecture seule : l'Agent explore, pose des questions, découpe en tâches — mais **ne modifie aucun fichier**. Aucun point de retour n'est créé, puisque rien ne change.

## Étape 2 · Décrire le besoin et laisser l'Agent critiquer · ⏱️ 10 min

### 🧵 Fil RH

📋 **Prompt à coller**

```text
Je veux une application qui aide un recruteur à trier des CV pour le
poste de coordinateur·rice administratif·ve d'Atelier Nova (fiche de
poste ci-jointe). Critique ce besoin avant que je ne construise quoi
que ce soit : étapes manquantes dans le flux CV → score → décision,
risques de biais, questions de RGPD à anticiper. Ne modifie rien.
```

Joignez `data/fiche-poste-coordinateur.md` à votre message (glisser-déposer ou bouton de pièce jointe).

> [!TIP]
> **✅ Vous devez voir**
> - L'Agent relève au moins : la nécessité d'une grille de critères explicite, la question de la validation humaine finale, un risque de biais (âge, genre, trous de carrière), et le fait que les CV sont des données personnelles.

### 🧵 Fil Finance

📋 **Prompt à coller**

```text
Je veux une application qui aide un comptable à clôturer le mois pour
Atelier Nova : import de transactions, nettoyage, classification par
compte, détection d'anomalies, tableau de bord, rapport. Critique ce
besoin avant que je ne construise quoi que ce soit : où l'IA doit
intervenir et où un calcul doit rester déterministe (jamais confié au
modèle), risques si un total est faux. Ne modifie rien.
```

> [!TIP]
> **✅ Vous devez voir**
> - L'Agent distingue ce qui doit rester un calcul de code (totaux, moyennes, rapprochements) de ce qui relève de l'IA (classification, rédaction du résumé), et signale qu'un total faux non détecté est le risque principal.

## Étape 3 · Rédiger 3 à 5 user stories · ⏱️ 8 min

📋 **Prompt à coller**

```text
À partir de cette discussion, rédige 3 à 5 user stories au format
« En tant que [rôle], je veux [action] afin de [bénéfice] », avec pour
chacune un critère d'acceptation vérifiable, et une section « hors
périmètre » de ce lab. Toujours en Plan : ne crée aucun fichier.
```

> [!TIP]
> **✅ Vous devez voir**
> - Des user stories au format demandé, un critère d'acceptation par story (pas une phrase vague), et une liste explicite de ce qui est hors périmètre (ex. fil RH : pas de signature électronique ; fil Finance : pas de connexion bancaire réelle).

## Étape 4 · Découper en plan de développement · ⏱️ 8 min

📋 **Prompt à coller**

```text
Découpe la construction en étapes de prompts courts, chacune pouvant
être exécutée puis testée séparément en mode Build. Relis ton propre
plan : des étapes trop grosses ? des dépendances entre étapes mal
ordonnées ? Corrige avant de me le donner.
```

> [!TIP]
> **✅ Vous devez voir**
> - Une liste d'étapes numérotées, chacune assez petite pour être construite et testée en une fois (pas « construire toute l'application » en une étape).

---

## ✅ Point de contrôle
- [ ] Aucun fichier créé pendant tout le lab (le mode est resté sur Plan).
- [ ] Cahier des charges v0 : 3 à 5 user stories, critères d'acceptation, hors périmètre.
- [ ] Plan de développement en étapes testables.
- [ ] Fil Finance : la règle « le code calcule, l'IA classe et rédige » est explicitement notée.

## 🧠 À retenir
- **Plan critique, Build construit** : on garde cette séquence pour chaque étape importante de la journée.
- Un cahier des charges vague au départ coûte cher plus tard : la critique de l'Agent en Plan est gratuite, les erreurs en Build consomment des crédits.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'Agent a modifié ou créé un fichier alors que vous étiez en Plan | Vérifiez le sélecteur de mode avant de recommencer : il a pu repasser en Build. Revenez en Plan et reposez la question. |
| Les user stories restent vagues | `Chaque critère d'acceptation doit être une phrase qu'on peut vérifier par oui ou non. Récris-les.` |
| Le plan de développement propose une seule grosse étape | `Découpe cette étape en 3 sous-étapes plus petites, chacune testable seule.` |

</details>

---

➡️ **Lab suivant :** [LAB-04 · Assets : page d'accueil et site vitrine](LAB-04-assets.md)
