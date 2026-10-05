# LAB-07 · Construire en petites étapes (mode Build)

> **En une phrase —** Un prompt, un test, un point de retour, répété jusqu'à l'application complète — puis une régression provoquée exprès, pour apprendre à revenir en arrière avant que ça n'arrive pour de vrai.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 35 min | Le projet de votre fil rouge | LAB-06 |

## 🎯 À la fin de ce lab
- Une application construite **tâche par tâche**, avec un point de retour après chacune.
- Vous avez comparé la même demande en Plan puis en Build.
- Vous avez provoqué une régression volontaire, et vous savez y survivre.

---

## Étape 1 · Basculer en Build · ⏱️ 1 min

Dans le sélecteur de mode de l'Agent, choisissez **Build**.

> [!IMPORTANT]
> **🎛️ Ce que fait le mode Build**
> Mode par défaut : l'Agent écrit le code, installe des dépendances, configure la base de données, corrige des bugs. Un **point de retour** est créé à chaque tâche terminée.

## Étape 2 · 🧵 Selon votre fil rouge — construire tâche par tâche · ⏱️ 20 min

Envoyez les prompts **un par un**, dans l'ordre. Après chacun : regardez le résultat dans Preview, testez-le, puis seulement envoyez le suivant.

### Fil RH

📋 **Prompts à coller, un par un**

```text
1) Ajoute un formulaire : fiche de poste pré-remplie (lecture seule)
   et un tableau qui liste les 10 candidatures déjà importées.
```
```text
2) Pour chaque candidature, affiche le score calculé au LAB-06 et le
   détail des quatre sous-notes, dans le tableau.
```
```text
3) Trie le tableau par score décroissant. Ajoute une colonne
   « justification » avec la phrase d'explication de chaque sous-note.
```
```text
4) Ajoute un bouton d'export CSV du tableau trié.
```

### Fil Service client

📋 **Prompts à coller, un par un**

```text
1) Crée une page « Demandes clients » (mini-CRM) qui enregistre :
   nom, email, message, catégorie, date, statut (en attente).
```
```text
2) Relie le formulaire de contact du site vitrine à ce mini-CRM : chaque
   envoi crée une nouvelle demande au statut « en attente ».
```
```text
3) Ajoute, sur la page « Demandes clients », une action pour marquer
   une demande « traitée » ou « rejetée », avec un commentaire.
```

> [!TIP]
> **✅ Vous devez voir, après chaque prompt**
> - Un **point de retour** nouveau (visible dans l'historique du projet ou confirmé par l'Agent).
> - Le résultat testé dans Preview avant d'envoyer le prompt suivant.

## Étape 3 · Comparer Plan puis Build · ⏱️ 8 min

1. Repassez en **Plan**. Collez :

```text
Ajouter un champ de recherche par mot-clé sur le tableau principal.
```

2. Lisez le plan proposé, sans rien valider à l'aveugle.
3. Repassez en **Build** et collez le même prompt.
4. Comparez : qu'est-ce qui a changé entre les deux modes (fichiers touchés, points de retour créés) ?

## Étape 4 · Provoquer une régression, puis l'annuler · ⏱️ 6 min

📋 **Prompt à coller (toujours en Build)**

```text
Supprime la colonne de score du tableau principal et remplace-la par
un simple drapeau « bon » / « pas bon » sans explication.
```

1. Observez : c'est une régression, le détail du score a disparu.
2. Revenez au **point de retour précédent** (dans l'historique des checkpoints du projet).
3. Vérifiez que le score détaillé est revenu.

> [!NOTE]
> 💬 Le mode Plan ne crée **jamais** de point de retour, puisqu'il ne modifie rien : ce réflexe de retour en arrière appartient entièrement au mode Build.

---

## ✅ Point de contrôle
- [ ] Application construite en plusieurs petites étapes, chacune testée.
- [ ] Tableau Plan / Build rempli de tête : fichiers touchés, points de retour créés.
- [ ] Régression provoquée puis annulée avec succès.

## 🧠 À retenir
- **Un prompt, un test, un point de retour** : la règle qui évite de devoir tout refaire après une mauvaise série de demandes.
- Revenir en arrière n'est pas un échec : c'est le réflexe que ce lab installe avant que l'enjeu soit réel.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'Agent construit tout en un seul gros prompt malgré les étapes séparées | Renvoyez les prompts un par un, en attendant la fin de chacun avant d'envoyer le suivant. |
| Pas de point de retour visible après une tâche | Demandez : `Confirme que cette tâche a créé un point de retour, et donne-moi son nom.` |
| Le retour en arrière ne restaure pas le score détaillé | Revenez d'un point de retour supplémentaire en arrière, puis redemandez l'étape 2 du fil choisi. |

</details>

---

➡️ **Lab suivant :** [LAB-08 · Faire expliquer son code (lecture en mode Plan)](LAB-08-lecture-code.md)
