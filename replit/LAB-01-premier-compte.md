# LAB-01 · Premier compte, premier résultat

> **En une phrase —** Un compte créé en connaissance des crédits, un seul prompt simple donné à l'Agent, et une première page publiée avec une URL que vous pouvez ouvrir vous-même.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 20 min | replit.com, nouvel artifact `Web app` | Aucun |

## 🎯 À la fin de ce lab
- Vous avez un compte Replit, créé en connaissance de l'offre et des crédits.
- Vous avez une page publiée, avec une URL publique que vous pouvez montrer à votre voisin.
- Vous savez retrouver l'aperçu (Preview) et la publication (Deployments) sans les confondre.

---

## Étape 1 · Créer le compte · ⏱️ 5 min

1. Allez sur **replit.com** et créez un compte (email ou SSO).
2. Choisissez une offre. Pour cette formation, **Starter** (gratuite) suffit ; les éléments 8 et 9 de la journée (Intégrations, Routines) vous diront si votre offre a une limite.
3. Arrivé sur l'accueil, repérez le bouton **New** en haut de la barre latérale : c'est par là qu'on crée tout.

> [!IMPORTANT]
> **💳 Avant de continuer**
> Ne saisissez **aucune donnée réelle** aujourd'hui : ni vos vraies coordonnées professionnelles, ni un vrai numéro de carte dans un projet. Tout ce qu'on construit est fictif.

## Étape 2 · Nouveau projet · ⏱️ 3 min

1. Cliquez sur **New**.
2. Dans la liste des types d'artifact, choisissez **Web app**.
3. Donnez un nom au projet, par exemple `mon-premier-projet`.

> [!NOTE]
> 💬 Le menu **New** propose aussi Mobile app, Data Visualization, Slide deck, Animation, 3D game, Design, Document, Spreadsheet. On ne pratique que **Web app** aujourd'hui ; les autres sont à explorer de votre côté.

## Étape 3 · Un seul prompt simple · ⏱️ 5 min

1. Dans la zone de saisie de l'Agent, collez le prompt ci-dessous tel quel.
2. Appuyez sur **Entrée**.
3. Laissez l'Agent travailler : il écrit le code, puis affiche un aperçu.

📋 **Prompt à coller**

```text
Crée une page qui présente une agence fictive d'événementiel appelée
« Atelier Nova » : un titre, une courte description, trois services
proposés (décoration d'événements, location de matériel, coordination
de prestataires), et un bouton de contact qui ouvre un formulaire simple
(nom, email, message). Couleurs sobres, une seule page.
```

> [!TIP]
> **✅ Vous devez voir**
> - Une page avec un titre, une description, trois services, un bouton de contact.
> - Un aperçu (Preview) qui se met à jour pendant que l'Agent travaille.

## Étape 4 · Regarder l'aperçu · ⏱️ 2 min

1. Ouvrez l'onglet **Preview**, à côté de l'éditeur de fichiers.
2. Cliquez sur le bouton de contact : le formulaire doit s'ouvrir.
3. Si quelque chose manque, ne corrigez pas encore : c'est le sujet du LAB-02 et du LAB-07.

## Étape 5 · Publier · ⏱️ 5 min

1. Ouvrez **Deployments**, dans la barre latérale du projet.
2. Choisissez un déploiement simple (statique ou autoscale selon ce que Replit propose pour ce projet).
3. Lancez la publication et attendez l'URL publique.
4. Ouvrez cette URL dans un nouvel onglet : c'est la preuve que ça fonctionne en dehors de l'éditeur.

> [!WARNING]
> ⚠️ Si Deployments vous demande un plan payant pour ce type de déploiement, repassez sur un déploiement statique simple : l'objectif ici est d'obtenir une URL, pas de choisir le réglage le plus robuste.

---

## ✅ Point de contrôle
- [ ] Compte créé, offre choisie en connaissance de cause.
- [ ] Projet `Web app` créé avec un seul prompt.
- [ ] Page conforme au prompt dans l'aperçu.
- [ ] URL publique ouverte avec succès, aucune donnée réelle saisie.

## 🧠 À retenir
- **New → type d'artifact → prompt** : le geste de base, à refaire pour chaque nouveau projet de la journée.
- **Preview** montre le brouillon, **Deployments** le publie réellement : deux étapes distinctes.
- Un seul prompt simple laisse l'Agent décider beaucoup de choses à votre place : c'est le sujet du prochain lab.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'offre bloque la création de compte | Choisissez Starter (gratuite) : elle suffit pour toute la journée, sauf la démonstration des Routines. |
| L'Agent pose une question avant de construire | Répondez simplement, ou dites : `Fais des choix raisonnables et montre-moi le résultat.` |
| Le bouton de contact ne fait rien dans l'aperçu | Normal à ce stade : ne corrigez pas, c'est le sujet des labs suivants. |
| Deployments ne propose aucune option gratuite | Essayez un déploiement de type statique ; sinon, montrez l'aperçu (Preview) à votre voisin et revenez à la publication plus tard dans la journée. |

</details>

---

➡️ **Lab suivant :** [LAB-02 · Prompt vague contre prompt structuré](LAB-02-prompt-structure.md)
