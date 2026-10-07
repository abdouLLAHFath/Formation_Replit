# LAB-PROJECT-MANAGEMENT · Suivi de projet

> **En une phrase —** Un événement de 120 invités à organiser pour Atelier Nova : un besoin décrit en Plan, transformé en tâches suivies en Build, puis un bug volontaire corrigé avec la méthode du point de retour.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 1 h 15 (4 étapes) | Nouveau projet `Web app`, `atelier-nova-projets` | LAB-CODE-BIBLIOTHEQUES |

## 🎯 À la fin de ce lab
- Un cahier des charges v0 pour un suivi de projet, avec user stories, critères et hors périmètre.
- Des tâches suivies par statut, créées et modifiées.
- Le code de suivi expliqué et un risque corrigé.
- Un bug volontaire diagnostiqué, corrigé, avec un retour arrière testé.

---

## Étape 1 · Cahier des charges en Plan · ⏱️ 20 min

1. Mode **Plan**.

📋 **Prompt à coller (en Plan)**

```text
Atelier Nova organise un mariage de 120 invités dans six semaines.
Je veux un outil de suivi de projet pour cet événement : tâches,
responsable, échéance, statut. Pose-moi les questions nécessaires,
puis propose 3 à 5 user stories avec critères d'acceptation, et un
hors périmètre (ex. pas de facturation, pas de messagerie intégrée).
```

> [!TIP]
> **✅ Vous devez voir**
> 3 à 5 user stories, des critères d'acceptation vérifiables, et un hors périmètre écrit.

## Étape 2 · Tâches en Build · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Construis la liste des tâches du mariage : titre, responsable,
échéance, statut (À faire, En cours, Terminé, Bloqué). Ajoute cinq
tâches fictives pour démarrer (traiteur, fleuriste, plan de salle,
invitations, musique).
```

1. Ajoutez une sixième tâche à la main.
2. Changez le statut d'une tâche existante.

> [!TIP]
> **✅ Vous devez voir**
> Six tâches au total, chacune avec un statut modifiable qui persiste après rechargement.

## Étape 3 · Suivi · ⏱️ 20 min

1. Mode **Plan** : faites expliquer le code de suivi.

📋 **Prompt à coller (en Plan)**

```text
Explique en une phrase comment chaque statut de tâche est stocké et
affiché, puis liste trois risques : ce qui pourrait faire perdre une
tâche ou afficher un statut faux.
```

2. Choisissez le risque le plus préoccupant et corrigez-le en **Build**.

> [!TIP]
> **✅ Vous devez voir**
> Trois risques listés, et au moins un corrigé avec une modification ciblée.

## Étape 4 · Bug de suivi · ⏱️ 15 min

1. En Build, provoquez volontairement un bug : demandez une modification qui casse l'enregistrement du statut (par exemple, un changement qui empêche la sauvegarde).

📋 **Prompt à coller (en Build, à des fins de démonstration)**

```text
Modifie la sauvegarde du statut d'une tâche pour qu'elle ne
s'enregistre plus en base (uniquement à l'écran), afin que je
puisse m'entraîner à diagnostiquer ce bug.
```

2. Constatez le bug : le statut revient à son ancienne valeur après rechargement.
3. Diagnostiquez en **Plan**, corrigez en **Build**.
4. Si la correction aggrave la situation, revenez au point de retour précédent.

> [!TIP]
> **✅ Vous devez voir**
> Le statut persiste correctement après correction, et un retour arrière testé au moins une fois pendant le lab.

---

## ✅ Point de contrôle
- [ ] User stories, critères et hors périmètre écrits.
- [ ] Six tâches créées, statut modifiable et persistant.
- [ ] Un risque identifié et corrigé.
- [ ] Bug volontaire corrigé, retour arrière testé.

## 🧠 À retenir
- Un suivi de projet se construit comme n'importe quelle application : besoin, tâches, test, correction.
- Un statut qui ne survit pas au rechargement n'est pas un statut enregistré.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Les tâches disparaissent au rechargement | Vérifiez qu'elles sont bien écrites en base de données, pas seulement en mémoire côté navigateur. |
| Le bug volontaire ne se reproduit pas | Redemandez-le en précisant « uniquement l'écriture en base, pas l'affichage ». |
| Le point de retour restaure trop, ou pas assez | Vérifiez la liste des points de retour et choisissez celui juste avant la tâche fautive. |

</details>

---

➡️ **Lab suivant :** [LAB-MINI-CRM · Site, formulaire et mini CRM](LAB-MINI-CRM.md)
