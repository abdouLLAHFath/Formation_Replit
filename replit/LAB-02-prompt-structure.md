# LAB-02 · Prompt vague contre prompt structuré

> **En une phrase —** Le même objectif, un prompt vague puis un prompt structuré en quatre ingrédients : vous observez ce que l'Agent décide à votre place quand on ne précise rien.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 15 min | Le projet du LAB-01 | LAB-01 |

## 🎯 À la fin de ce lab
- Vous avez vu un prompt vague produire un résultat imprévisible.
- Vous avez un **modèle de prompt réutilisable** (contexte, objectif, contraintes, format), prêt pour le reste de la journée.

---

## Étape 1 · Un prompt vague · ⏱️ 5 min

1. Dans le projet du LAB-01, ouvrez une **nouvelle page** du site (ou un nouveau projet `Web app` si vous préférez repartir à zéro).
2. Collez le prompt ci-dessous, sans rien ajouter.

📋 **Prompt à coller**

```text
Fais-moi un site.
```

3. Une fois la réponse obtenue, notez par écrit **trois choses** que l'Agent a décidées à votre place (couleurs, structure, contenu, nom de l'activité…).

> [!TIP]
> **✅ Vous devez voir**
> - Un site généré, mais sur un sujet, des couleurs et une structure que vous n'avez pas choisis.
> - D'un binôme à l'autre, des résultats très différents pour le même prompt.

## Étape 2 · Un prompt structuré · ⏱️ 5 min

Le même objectif, avec les quatre ingrédients : **contexte, objectif, contraintes, format**.

📋 **Prompt à coller**

```text
Contexte : je gère Atelier Nova, une agence d'événementiel et de
décoration de 12 personnes à Paris.

Objectif : une page d'accueil à une seule section qui donne envie de
demander un devis.

Contraintes : ton sobre et professionnel, palette de deux couleurs
maximum, aucune donnée de contact réelle (utilise des valeurs fictives
du type contact@exemple.test), aucun nom de personne réelle.

Format : un titre, une phrase d'accroche, trois services (décoration
d'événements, location de matériel, coordination de prestataires),
un bouton « Demander un devis » qui ouvre un formulaire (nom, email,
date de l'événement, message).
```

> [!TIP]
> **✅ Vous devez voir**
> - Un résultat qui correspond précisément aux quatre ingrédients donnés.
> - Beaucoup moins d'écart d'un binôme à l'autre : le prompt a fait le travail de cadrage à votre place.

## Étape 3 · Comparer · ⏱️ 3 min

| | Prompt vague | Prompt structuré |
|---|:---:|:---:|
| Sujet choisi par | l'Agent | vous |
| Couleurs | imprévisibles | contraintes |
| Contenu vérifiable sans relire le prompt | non | oui |

> [!NOTE]
> 💬 **Le test à retenir :** avant d'envoyer un prompt, demandez-vous si vous pourriez faire le travail vous-même sans poser une seule question. Si non, l'Agent non plus : il va deviner.

## Étape 4 · Garder le modèle · ⏱️ 2 min

Notez ce modèle quelque part (bloc-notes, fichier texte) : vous le réutiliserez à chaque lab de la journée.

```text
Contexte : [qui vous êtes, ce qui existe déjà]
Objectif : [ce qui doit exister à la fin, en une phrase vérifiable]
Contraintes : [couleurs, langue, données autorisées, interdits]
Format : [pages, tableaux, boutons, exports attendus]
```

---

## ✅ Point de contrôle
- [ ] Les trois décisions prises par l'Agent sur le prompt vague sont notées.
- [ ] Le prompt structuré a produit un résultat conforme aux quatre ingrédients.
- [ ] Le modèle de prompt est gardé pour la suite de la journée.

## 🧠 À retenir
- **Contexte, objectif, contraintes, format** : à utiliser pour chaque prompt important de la journée.
- Un prompt vague n'est pas interdit — il sert à explorer — mais on ne construit rien de sérieux dessus sans repasser par ce modèle.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Le prompt structuré donne un résultat aussi imprévisible que le vague | Vérifiez que les quatre ingrédients sont bien dans le prompt collé, rien n'a été coupé au copier-coller. |
| L'Agent demande des précisions avant de construire | Répondez avec une phrase courte, ou laissez-le faire un choix raisonnable : ce n'est pas un échec du prompt. |

</details>

---

➡️ **Lab suivant :** [LAB-03 · Cahier des charges et plan de développement (mode Plan)](LAB-03-mode-plan.md)
