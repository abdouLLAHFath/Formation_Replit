# LAB-09 · Partir d'un modèle, justifier ses dépendances

> **En une phrase —** Plutôt qu'une page blanche, vous repartez d'un projet existant ; et pour le tableau de bord financier, chaque bibliothèque installée est justifiée avant d'être acceptée.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 20 min | Un nouveau projet + celui du fil Finance | LAB-04 |

## 🎯 À la fin de ce lab
- Un nouveau projet démarré depuis une page existante, pas depuis zéro.
- La liste des dépendances installées, chacune justifiée en une phrase.
- 🧵 Fil Finance : un rapport d'anomalies et un tableau de bord, avec export Excel.

> [!NOTE]
> 💬 **Deux sens à ne pas confondre.** La **Library** de Replit (barre latérale) est un panneau de templates propre à l'outil **Design** (canvas) : elle n'existe pas pour un artifact Web app comme les nôtres. Ce qu'on pratique ici, ce sont les **bibliothèques de code** (dépendances), un sens différent du même mot.

---

## Étape 1 · Repartir d'un modèle · ⏱️ 5 min

1. Créez un nouveau projet `Web app`.
2. Collez le prompt ci-dessous.

📋 **Prompt à coller**

```text
Reprends la structure visuelle de la page d'accueil d'Atelier Nova
(titre, trois services, bouton de contact) comme point de départ, et
transforme-la en page d'accueil pour un deuxième produit fictif :
un abonnement mensuel de décoration florale. Garde la même palette.
```

## Étape 2 · Ajouter une bibliothèque justifiée · ⏱️ 5 min

📋 **Prompt à coller**

```text
Ajoute un graphique simple (nombre d'abonnés fictifs par mois, données
inventées) sur cette page. Avant d'installer une bibliothèque de
graphiques, dis-moi laquelle, pourquoi, et une alternative possible.
```

> [!TIP]
> **✅ Vous devez voir**
> - Une bibliothèque nommée, une raison en une phrase, une alternative citée — avant l'installation, pas après.
> - La liste des dépendances du projet (fichier de dépendances), relisible.

> [!WARNING]
> ⚠️ Si l'Agent installe sans expliquer, demandez : `Avant d'installer quoi que ce soit, dis-moi quelle bibliothèque et pourquoi.` Une dépendance non justifiée est un risque de sécurité et de poids, pas un détail.

## Étape 3 · 🧵 Fil Finance — anomalies et rapprochement · ⏱️ 7 min

Dans le projet Finance (LAB-05/06), repassez en Build.

📋 **Prompt à coller**

```text
Sur les 28 transactions nettoyées et classées, détecte les anomalies
par du code, pas par estimation : montants très inhabituels pour leur
catégorie, dates incohérentes, pièces justificatives manquantes pour
les statuts « soumise ». Liste chaque anomalie avec son identifiant
et la règle qui la signale.
```

> [!TIP]
> **✅ Vous devez voir, entre autres**
> - **TX-0919** (45 000 €, Fournitures) signalée comme montant très inhabituel pour sa catégorie.
> - **TX-0909** et **TX-0917** signalées sans pièce jointe (statut « soumise »).

## Étape 4 · Tableau de bord et export · ⏱️ 3 min

📋 **Prompt à coller**

```text
Calcule, par du code : le total par catégorie et le total général sur
les 28 transactions nettoyées (hors TX-0919, mise à part en attendant
vérification). Affiche-les dans un tableau de bord, et ajoute un
bouton d'export Excel.
```

> [!TIP]
> **✅ Vous devez voir un total proche de :**
> | Catégorie | Lignes | Montant |
> |---|---:|---:|
> | Salaires | 3 | 9 150,50 € |
> | Loyer | 3 | 4 350,00 € |
> | Honoraires | 6 | 4 100,00 € |
> | Marketing | 4 | 958,50 € |
> | Déplacement | 6 | 796,60 € |
> | Fournitures | 6 | 484,75 € |
> | **Total** | **28** | **19 840,35 €** |

---

## ✅ Point de contrôle
- [ ] Nouveau projet démarré depuis un modèle existant, pas une page blanche.
- [ ] Bibliothèque de graphiques justifiée avant installation.
- [ ] 🧵 Finance : TX-0919, TX-0909 et TX-0917 détectées comme anomalies ; tableau de bord proche de 19 840,35 € ; export Excel disponible.

## 🧠 À retenir
- La **Library** (Design) et les **bibliothèques de code** sont deux choses différentes : seule la seconde s'utilise sur un Web app.
- « Quelle bibliothèque, pourquoi, quelle alternative » avant chaque installation — refuser les ajouts non justifiés.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'Agent installe une bibliothèque sans l'annoncer | `Désinstalle cette dépendance et recommence : annonce-la d'abord, avec une raison.` |
| TX-0919 n'apparaît pas dans les anomalies | `Compare chaque montant Fournitures à la moyenne de sa catégorie : signale tout écart supérieur à 10 fois la moyenne.` |
| Le total du tableau de bord ne correspond pas | `Recalcule en excluant uniquement TX-0907 (doublon) du jeu de 29 lignes, puis mets de côté TX-0919 pour obtenir 28 lignes à 19 840,35 €.` |

</details>

---

➡️ **Lab suivant :** [LAB-10 · Connecteur natif et serveur MCP](LAB-10-integrations-mcp.md)
