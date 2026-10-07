# LAB-ROUTINES-DEPLOIEMENT · Routines, secrets et mise en ligne

> **En une phrase —** Une routine qui résume sans jamais agir seule, une clé de test révoquée, et une application publiée après avoir passé la checklist.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 50 min (3 étapes) | Barre latérale **Routines**, puis vos projets du jour | LAB-DEBOGAGE |

## 🎯 À la fin de ce lab
- Une routine planifiée, son résultat lu, son budget fixé, puis mise en pause.
- La clé de test révoquée, et la preuve qu'aucune clé ne traîne dans le code.
- Une application publiée, avec un parcours testé sur l'URL publique.

> [!WARNING]
> ⚠️ **Vérifiez votre offre avant de commencer.** Les routines sont indisponibles sur l'offre Starter ; limitées à 5 routines actives par utilisateur sur Core, 10 sur Pro ; et fonctionnent uniquement en mode Power ou Max. Si votre offre ne le permet pas, suivez cette étape en **démonstration** avec le formateur.

---

## Étape 1 · Routine hebdomadaire · ⏱️ 15 min

1. Ouvrez **Routines** dans la barre latérale, dans le projet `finance-cloture`.
2. Créez une routine.

📋 **Prompt à coller**

```text
Chaque lundi à 9h, relis le dernier rapport du tableau de bord
financier d'Atelier Nova et donne-moi un résumé en 5 lignes dans ce
fil : montant total, anomalies en attente, pièces manquantes.
N'envoie rien à l'extérieur, ne modifie aucun fichier, contente-toi
de résumer.
```

3. Validez l'intervalle (une semaine, minimum une heure entre deux exécutions).
4. Lisez le résumé produit, fixez un budget de crédits pour cette routine, puis mettez-la en pause.

> [!TIP]
> **✅ Vous devez voir**
> Un résumé en cinq lignes maximum, aucun fichier modifié, aucun envoi externe. Routine mise en pause en fin d'étape.

## Étape 2 · Secrets et accès · ⏱️ 15 min

1. Choisissez un des projets du jour qui contient une clé de test (`DEEPSEEK_API_KEY` dans `rh-tri-cv`, par exemple).
2. Ouvrez **Tools › Setup › Secrets** et listez les clés présentes.

📋 **Prompt à coller (en Plan)**

```text
Cherche dans tout le code, le chat et les logs si la valeur de la clé
DEEPSEEK_API_KEY apparaît ailleurs que dans les Secrets. Ne modifie
rien, liste simplement ce que tu trouves.
```

3. Si tout est propre, révoquez la clé de test dans Secrets.

> [!TIP]
> **✅ Vous devez voir**
> Aucune occurrence de la valeur de la clé en dehors des Secrets, puis la clé révoquée.

## Étape 3 · Mise en ligne · ⏱️ 20 min

1. Choisissez un projet à publier (par exemple `atelier-nova-crm`).
2. Passez la checklist avant publication :

> [!IMPORTANT]
> **Checklist avant l'URL publique**
> - [ ] Aucune donnée réelle dans le projet.
> - [ ] Clés dans Secrets, jamais dans le code.
> - [ ] Connecteurs limités au compte de test, déconnectés si plus utiles.
> - [ ] Validation humaine en place avant tout envoi.
> - [ ] Code relu au moins une fois en mode Plan.

3. Cliquez sur **Publier** (Deployments).
4. Ouvrez l'URL publique dans un nouvel onglet et testez un parcours complet (par exemple : remplir le formulaire de contact, retrouver le lead).

> [!TIP]
> **✅ Vous devez voir**
> Une URL publique accessible, et le parcours testé qui fonctionne de bout en bout, comme en local.

---

## ✅ Point de contrôle
- [ ] Routine planifiée, résumé lu, budget fixé, routine en pause.
- [ ] Clé de test révoquée, aucune trace ailleurs que dans Secrets.
- [ ] Checklist de publication passée en entier.
- [ ] URL publique testée sur un parcours complet.

## 🧠 À retenir
- Une routine résume ; elle n'agit jamais seule sans validation humaine.
- Publier n'est pas la dernière étape technique : c'est la dernière étape de la checklist.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Routines indisponible dans la barre latérale | Votre offre ne le permet pas (Starter) : suivez l'étape 1 en démonstration avec le formateur. |
| La clé révoquée casse un appel encore utile ailleurs | Générez une nouvelle clé de test et mettez-la à jour dans Secrets avant de continuer. |
| L'URL publique affiche une erreur que vous n'aviez pas en local | Revenez en Plan, demandez d'expliquer la différence entre l'environnement de développement et celui de production. |

</details>

---

➡️ **Suite :** le bloc 11, récapitulatif, est en théorie seule — voir la présentation [`../Fondamentaux-Replit/formation-replit.html`](../Fondamentaux-Replit/formation-replit.html).
