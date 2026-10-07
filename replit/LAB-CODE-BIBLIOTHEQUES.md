# LAB-CODE-BIBLIOTHEQUES · Lecture du code et bibliothèques

> **En une phrase —** Faire expliquer son code en mode Plan, vérifier une explication en la testant vraiment, puis justifier — ou retirer — chaque bibliothèque installée.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 1 h (4 étapes) | Le projet `finance-cloture` (ou un autre projet déjà construit) | LAB-FINANCE |

## 🎯 À la fin de ce lab
- Une carte du projet : chaque fichier principal expliqué en une phrase, et trois risques identifiés par l'Agent lui-même.
- Une explication vérifiée en la testant, pas seulement crue sur parole.
- La liste des bibliothèques installées, chacune justifiée en une phrase — ou retirée.

---

## Étape 1 · Expliquer le code en Plan · ⏱️ 15 min

1. Dans le sélecteur de mode, choisissez **Plan** : on lit, on ne touche à rien.

📋 **Prompt à coller (en Plan)**

```text
Explique chaque fichier principal de ce projet (interface, logique,
base de données) en une phrase chacun, comme à un débutant. Puis
liste les trois principaux risques de ce code : ce qui pourrait
casser ou donner un résultat faux.
```

> [!TIP]
> **✅ Vous devez voir**
> Une phrase par fichier principal, compréhensible sans connaître le code, et trois risques concrets (pas « des bugs peuvent survenir »).

## Étape 2 · Vérifier une explication en la modifiant · ⏱️ 15 min

1. Choisissez une des explications données (par exemple, comment le total de contrôle est calculé).
2. Passez en **Build** et modifiez une valeur précise liée à cette explication (par exemple, changez un montant dans une transaction).

📋 **Prompt à coller (en Build)**

```text
Change le montant de la transaction TX-0903 à 999 €, et montre-moi où
cette modification se répercute (total de contrôle, fiche comptable,
tableau de bord).
```

3. Vérifiez que le résultat change exactement comme l'explication de l'étape 1 le prévoyait.

> [!TIP]
> **✅ Vous devez voir**
> Le changement se répercute aux endroits annoncés. Si ce n'est pas le cas, l'explication était fausse ou incomplète — corrigez-la.

## Étape 3 · Justifier une dépendance · ⏱️ 15 min

📋 **Prompt à coller (en Plan)**

```text
Liste toutes les bibliothèques installées dans ce projet, et pour
chacune, explique en une phrase à quoi elle sert et si elle est
réellement utilisée quelque part dans le code.
```

1. Pour chaque bibliothèque « non réellement utilisée », demandez sa suppression en Build.

> [!NOTE]
> 💬 **Deux sens à ne pas confondre.** La **Library** de Replit (barre latérale) est un panneau de templates propre à l'outil **Design** (canvas) : elle n'existe pas pour un artifact Web app comme les nôtres. Ce qu'on pratique ici, ce sont les **bibliothèques de code** (dépendances), un sens différent du même mot.

> [!TIP]
> **✅ Vous devez voir**
> Une justification par dépendance, et au moins une suppression si une bibliothèque inutile a été trouvée.

## Étape 4 · Ajouter une bibliothèque · ⏱️ 15 min

📋 **Prompt à coller (en Build)**

```text
Ajoute une bibliothèque reconnue pour générer l'export Excel du
rapport financier (lab Finance, étape 6). Avant de l'installer,
indique son nom, sa popularité et sa dernière mise à jour.
```

1. Vérifiez la licence et la date de dernière mise à jour annoncées.
2. Testez l'export.

> [!WARNING]
> ⚠️ Une bibliothèque peu maintenue (dernière mise à jour vieille de plusieurs années) est un risque à signaler, même si elle fonctionne aujourd'hui.

> [!TIP]
> **✅ Vous devez voir**
> Un export fonctionnel, et une justification écrite pour cette nouvelle dépendance.

---

## ✅ Point de contrôle
- [ ] Une phrase par fichier principal, trois risques identifiés.
- [ ] Une explication vérifiée en la modifiant, confirmée ou corrigée.
- [ ] Chaque dépendance installée justifiée ; au moins une retirée si inutile.
- [ ] Une nouvelle dépendance ajoutée et justifiée, export testé.

## 🧠 À retenir
- Une explication qui ne se vérifie pas en la testant n'est qu'une affirmation.
- Une dépendance qui ne se justifie pas en une phrase ne reste pas dans le projet.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'explication reste vague malgré la relance | Redemandez en citant un fichier précis par son nom. |
| La modification de test ne se répercute nulle part | C'est un signal que l'explication de l'étape 1 était incomplète : redemandez une explication plus précise. |
| La suppression d'une bibliothèque casse le projet | Elle était en fait utilisée ailleurs : revenez au point de retour et redemandez une vérification plus large avant de la retirer. |

</details>

---

➡️ **Lab suivant :** [LAB-PROJECT-MANAGEMENT · Suivi de projet](LAB-PROJECT-MANAGEMENT.md)
