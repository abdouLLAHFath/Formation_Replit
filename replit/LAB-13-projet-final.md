# LAB-13 · Projet final : application IA métier

> **En une phrase —** Un problème métier choisi par vous, construit avec les éléments fondamentaux de votre choix, testé, sécurisé, déployé, puis présenté en 5 à 10 minutes.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| Reste de la journée | Un nouveau projet `Web app` | LAB-01 → LAB-12 |

## 🎯 À la fin de ce lab
- Une grille des éléments fondamentaux mobilisés, remplie et justifiée.
- Une application déployée, avec une URL publique.
- Une soutenance de 5 à 10 minutes, qui nomme explicitement deux éléments fondamentaux utilisés.

---

## Étape 0 · Choisir les éléments fondamentaux · ⏱️ 15 min

Remplissez cette grille **avant** de construire quoi que ce soit.

| Élément | Utilisé ? | Pourquoi |
|---|:---:|---|
| EF1 · Mode Plan | — | — |
| EF2 · Assets | — | — |
| EF3 · Import | — | — |
| EF4 · Clés API & Secrets | — | — |
| EF5 · Mode Build | — | — |
| EF6 · Lecture du code | — | — |
| EF7 · Library & bibliothèques | — | — |
| EF8 · Intégrations / MCP | — | — |
| EF9 · Routines | — | — |

> [!IMPORTANT]
> **🧱 Socle minimum proposé**
> **Mode Plan + Mode Build + clés API + assets**, et au moins **une intégration ou une routine**. Import, Library et lecture du code, selon votre besoin réel — ne les cochez pas juste pour remplir la grille.

## Étape 1 · Cahier des charges · ⏱️ 20 min

Reprenez et affinez le cahier des charges v0 rédigé au LAB-03 (ou rédigez-en un nouveau, même méthode : mode **Plan**, user stories, critères d'acceptation, hors périmètre, puis plan de développement en étapes testables).

## Étape 2 · Construction · ⏱️ reste de la journée

Construisez en **Build**, tâche par tâche (LAB-07), avec au moins une fonctionnalité IA validée par un humain (LAB-12). Mobilisez les éléments choisis à l'étape 0.

> [!TIP]
> **✅ Vous devez voir, en continu**
> - Un point de retour après chaque tâche.
> - Les clés API dans les Secrets, jamais dans le code ou le chat (LAB-06).

## Étape 3 · Test, correction, sécurisation · ⏱️ 20 min

Reprenez la méthode du LAB-12 (expliquer en Plan, corriger en Build, tester) sur vos propres cas. Contrôlez : secrets, accès, permissions minimales sur toute intégration connectée.

## Étape 4 · Déploiement et documentation · ⏱️ 15 min

> [!WARNING]
> ⚠️ **Checklist avant l'URL publique**
> - Secrets ajoutés séparément sous **Publishing › Adjust settings › Production app secrets** (ils ne suivent pas automatiquement).
> - Assets publiés : données fictives uniquement.
> - Accès et rôles contrôlés si des pages sont sensibles.
> - Toute intégration testée reste en compte de test, jamais en production aujourd'hui.

Publiez, puis complétez la grille des éléments fondamentaux de l'étape 0 avec ce qui a été réellement utilisé.

## Étape 5 · Soutenance · ⏱️ 5 à 10 min par projet

Présentez : pourquoi ce problème, comment ça fonctionne, comment c'est testé, quelles limites, et le rôle de **deux éléments fondamentaux** de votre choix.

---

## ✅ Point de contrôle
- [ ] Grille des éléments fondamentaux complétée.
- [ ] Application déployée, URL publique ouverte avec succès.
- [ ] Au moins une fonctionnalité IA validée par un humain.
- [ ] Soutenance préparée, deux éléments fondamentaux nommés.

## 🧠 À retenir
- Les neuf éléments sont une boîte à outils, pas une liste à cocher en entier.
- Le réflexe qui compte depuis le LAB-01 : vérifier avant de valider.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Le projet est trop ambitieux pour le temps restant | Retournez à l'étape 0 : réduisez la grille au socle minimum, laissez le reste pour plus tard. |
| L'application publiée plante avec des valeurs manquantes | Vérifiez les Secrets de production (Publishing › Adjust settings) : c'est la cause la plus fréquente. |

</details>

---

🏁 **Fin du parcours.** Prochain devoir : revenir sur votre cahier des charges v0 et le préciser à la lumière de ce que vous avez construit.
