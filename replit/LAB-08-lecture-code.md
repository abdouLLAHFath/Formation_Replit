# LAB-08 · Faire expliquer son code (lecture en mode Plan)

> **En une phrase —** Avant de valider ce que l'Agent a construit, vous le faites expliquer en mode Plan — et vous vérifiez une explication en la modifiant vraiment, plutôt que de la croire sur parole.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 15 min | L'application construite au LAB-07 | LAB-07 |

## 🎯 À la fin de ce lab
- Une carte de votre projet : chaque fichier principal expliqué en une phrase.
- Les trois principaux risques identifiés par l'Agent lui-même.
- Une explication **vérifiée** en la testant, pas seulement crue sur parole.

> [!NOTE]
> 💬 « Code Companion » n'est pas un écran ou une fonction de Replit : il n'existe aucune page officielle sous ce nom. Ce lab réutilise simplement le **mode Plan** comme compagnon de lecture, puisqu'il est déjà en lecture seule.

---

## Étape 1 · Repasser en Plan · ⏱️ 1 min

Dans le sélecteur de mode, choisissez **Plan** : on lit, on ne touche à rien.

## Étape 2 · Expliquer chaque fichier principal · ⏱️ 6 min

📋 **Prompt à coller**

```text
Explique chaque fichier principal de ce projet (interface, logique,
base de données) en une phrase chacun, comme à un débutant. Puis
liste les trois principaux risques de ce code : ce qui pourrait casser
ou donner un résultat faux.
```

> [!TIP]
> **✅ Vous devez voir**
> - Une phrase par fichier principal, compréhensible sans connaître le code.
> - Trois risques concrets (pas des généralités du type « il peut y avoir des bugs ») : par exemple un calcul qui suppose une colonne toujours remplie, ou une donnée affichée sans vérification.

## Étape 3 · Comprendre une décision précise · ⏱️ 4 min

📋 **Prompt à coller**

```text
Dans le fichier qui calcule le score (ou qui gère le statut des
demandes), explique précisément ce qui se passe si une donnée
attendue est manquante.
```

## Étape 4 · Vérifier en testant · ⏱️ 4 min

1. Repassez en **Build**.
2. Demandez une petite modification liée à l'explication reçue (par exemple : gérer explicitement le cas d'une donnée manquante).
3. Testez : l'explication de l'Agent correspondait-elle à ce qui se passe vraiment ?

> [!WARNING]
> ⚠️ Une explication plausible n'est pas une garantie. C'est le test de l'étape 4, pas la qualité de la phrase, qui dit si elle était juste.

---

## ✅ Point de contrôle
- [ ] Carte du projet : chaque fichier principal expliqué en une phrase.
- [ ] Trois risques identifiés, concrets.
- [ ] Une explication vérifiée par une modification réelle et un test.

## 🧠 À retenir
- On relit en **Plan** pour ne rien casser pendant qu'on comprend.
- Une explication se vérifie en la testant, jamais en la croyant seule.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Les explications restent vagues (« ce fichier gère l'application ») | `Sois plus précis : que fait ce fichier exactement, avec quelles données en entrée et quel résultat en sortie ?` |
| Les trois risques sont génériques | `Donne-moi un risque concret : un exemple de donnée qui ferait planter ou fausser le calcul.` |

</details>

---

➡️ **Lab suivant :** [LAB-09 · Partir d'un modèle, justifier ses dépendances](LAB-09-library-bibliotheques.md)
