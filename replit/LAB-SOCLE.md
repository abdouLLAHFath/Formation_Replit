# LAB-SOCLE · Replit Agent et socle

> **En une phrase —** Un compte créé en connaissance des crédits, un prompt vague puis un prompt structuré pour voir ce que l'Agent décide à votre place, et un premier aller-retour entre Plan et Build avec un point de retour.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 55 min (3 étapes) | replit.com, nouvel artifact `Web app` | Aucun |

## 🎯 À la fin de ce lab
- Vous avez un compte Replit, créé en connaissance de l'offre et des crédits, et une page publiée avec une URL publique.
- Vous avez vu ce qu'un prompt vague laisse l'Agent décider à votre place, et vous avez un modèle de prompt réutilisable (contexte, objectif, contraintes, format).
- Vous avez utilisé le mode Plan sans modifier un fichier, construit une tâche en mode Build, et utilisé un point de retour.

---

## Étape 1 · Premier compte, premier résultat · ⏱️ 20 min

1. Allez sur **replit.com** et créez un compte (email ou SSO).
2. Choisissez une offre. Pour cette formation, **Starter** (gratuite) suffit ; l'étape Routines du bloc 10 vous dira si votre offre a une limite.
3. Cliquez sur **New**, choisissez l'artifact **Web app**, nommez le projet `atelier-nova-accueil`.

> [!IMPORTANT]
> **💳 Avant de continuer**
> Ne saisissez **aucune donnée réelle** aujourd'hui : ni vos vraies coordonnées professionnelles, ni un vrai numéro de carte. Tout ce qu'on construit est fictif, pour **Atelier Nova**, une agence d'événementiel et de décoration de 12 personnes.

📋 **Prompt à coller**

```text
Crée une page qui présente Atelier Nova, une agence d'événementiel et
de décoration, avec un titre, un logo texte, trois services et un
bouton de contact.
```

> [!TIP]
> **✅ Vous devez voir**
> - Un résultat dans l'**aperçu** (Preview).
> - Après avoir cliqué sur **Publier** (Deployments), une URL publique que vous pouvez ouvrir vous-même.

## Étape 2 · Prompt vague contre prompt structuré · ⏱️ 15 min

1. Ouvrez une nouvelle page du site (ou un nouveau projet `Web app`).
2. Collez ce prompt, sans rien ajouter :

📋 **Prompt à coller**

```text
Fais-moi un site.
```

3. Notez par écrit **trois choses** que l'Agent a décidées à votre place (couleurs, structure, contenu, nom de l'activité…).

> [!TIP]
> **✅ Vous devez voir**
> Un site généré, mais sur un sujet, des couleurs et une structure que vous n'avez pas choisis. D'un binôme à l'autre, des résultats très différents pour le même prompt.

4. Reprenez le même objectif avec les quatre ingrédients : **contexte, objectif, contraintes, format**.

📋 **Prompt à coller**

```text
Contexte : je gère Atelier Nova, une agence d'événementiel de 12
personnes.
Objectif : une page qui présente nos trois services.
Contraintes : garder une palette sobre, aucune donnée réelle, texte
en français.
Format : un titre, trois blocs et un bouton de contact.
```

5. Comparez les deux résultats avec votre voisin.

## Étape 3 · Plan contre Build, points de retour · ⏱️ 20 min

1. Dans le sélecteur de mode de l'Agent, choisissez **Plan**.

> [!IMPORTANT]
> **🎛️ Ce que fait le mode Plan**
> Lecture seule : l'Agent explore, pose des questions, découpe en tâches — mais **ne modifie aucun fichier**. Aucun point de retour n'est créé, puisque rien ne change.

📋 **Prompt à coller (en Plan)**

```text
Je veux ajouter une page « Nos réalisations » avec une galerie de
photos fictives. Propose-moi un plan en étapes testables, sans rien
construire.
```

2. Vérifiez qu'aucun fichier n'a changé dans l'éditeur.
3. Passez en mode **Build**.

> [!IMPORTANT]
> **🎛️ Ce que fait le mode Build**
> Mode par défaut : l'Agent écrit le code, installe des dépendances, configure la base de données, corrige des bugs. Un **point de retour** est créé à chaque tâche terminée.

4. Envoyez la première tâche du plan, une seule à la fois.
5. Une fois le résultat vérifié, provoquez une régression volontaire (demandez une modification qui casse manifestement la page), puis revenez au point de retour précédent.

> [!TIP]
> **✅ Vous devez voir**
> - En Plan : un plan reçu, aucun fichier modifié.
> - En Build : une tâche construite, testée, puis un retour en arrière réussi après la régression volontaire.

---

## ✅ Point de contrôle
- [ ] URL publique obtenue et accessible.
- [ ] Deux résultats comparés (prompt vague, prompt structuré), modèle de prompt noté.
- [ ] Plan lu sans modification, point de retour utilisé une fois.
- [ ] Aucune donnée réelle saisie.

## 🧠 À retenir
- Un modèle de langage génère du code **plausible**, pas du code **garanti** : d'où l'habitude de vérifier.
- Plan pour réfléchir, Build pour construire, point de retour en filet de sécurité.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Bloqué sur un écran de facturation | Vérifiez que l'offre Starter (gratuite) est bien sélectionnée, pas une offre payante. |
| L'aperçu ne se met pas à jour | Rafraîchissez l'onglet Preview, ou redemandez l'aperçu à l'Agent. |
| Le point de retour ne restaure rien | Vérifiez que vous sélectionnez bien le point *avant* la tâche qui a cassé la page, pas après. |

</details>

---

➡️ **Lab suivant :** [LAB-RH · Tri et score de CV](LAB-RH.md)
