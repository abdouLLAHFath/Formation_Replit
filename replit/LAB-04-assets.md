# LAB-04 · Assets : page d'accueil et site vitrine

> **En une phrase —** Vous ajoutez un logo et des images dans le dossier d'assets, vous les citez explicitement dans le prompt, puis vous publiez — et si vous suivez le fil Service client, vous posez aujourd'hui la FAQ qui nourrira le chatbot du LAB-06.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 20 min | Le projet du LAB-01 (ou un nouveau `Web app` pour le fil Service client) | LAB-01 |

## 🎯 À la fin de ce lab
- Un logo et des images, téléversés dans le dossier d'assets et cités dans le prompt — pas laissés « en l'air ».
- Une page publiée qui les affiche réellement.
- 🧵 Fil Service client : un site vitrine avec formulaire de contact, et une FAQ découpée en passages courts, prête pour le RAG.

> 🧵 **À partir d'ici, vous pouvez aussi choisir le fil Service client** si vous préférez ce troisième parcours à RH ou Finance.

---

## Étape 1 · Préparer les assets · ⏱️ 5 min

1. Trouvez ou créez rapidement un logo simple (texte stylisé, pas besoin de graphisme élaboré) et deux images libres de droits.
2. Dans l'éditeur de fichiers du projet, repérez le dossier d'assets (ou créez-en un, par exemple `assets/`).
3. Téléversez logo et images par glisser-déposer.

> [!WARNING]
> ⚠️ Vérifiez trois choses avant de téléverser : des **noms de fichiers clairs** (`logo-atelier-nova.png`, pas `image1.png`), des **images compressées** (quelques centaines de Ko, pas plusieurs Mo), et des **droits d'utilisation** réels si vous sortez d'un vrai moteur de recherche d'images — préférez une banque libre de droits.

## Étape 2 · Un prompt qui cite les assets · ⏱️ 5 min

Réutilisez le modèle de prompt du LAB-02, en citant explicitement les fichiers.

📋 **Prompt à coller**

```text
Contexte : la page d'accueil d'Atelier Nova existe déjà.

Objectif : intégrer le logo et les deux images du dossier assets/ à
la page actuelle.

Contraintes : utilise le fichier assets/logo-atelier-nova.png en haut
de page, et les deux autres images dans la section des services.
Garde la palette de couleurs actuelle.

Format : pas de nouvelle section, seulement l'intégration visuelle.
```

> [!TIP]
> **✅ Vous devez voir**
> - Le logo et les images affichés dans l'aperçu (Preview), à l'endroit demandé.

## Étape 3 · Publier de nouveau · ⏱️ 3 min

1. Retournez dans **Deployments** et republiez.
2. Ouvrez l'URL publique : les assets doivent s'afficher.

> [!NOTE]
> 💬 Un asset placé dans un projet publié devient **public**, comme le reste du site. N'y mettez jamais une donnée réelle sensible.

---

## 🧵 Fil Service client · ⏱️ 12 min (si vous suivez ce parcours)

### Étape SC-1 · Site vitrine

📋 **Prompt à coller**

```text
Contexte : Atelier Nova, agence d'événementiel et de décoration.

Objectif : un site vitrine à une page : présentation, galerie de
3 réalisations fictives (utilise des images génériques), formulaire
de contact, et une fenêtre de chatbot en bas à droite (vide pour
l'instant, elle sera connectée au LAB-06).

Contraintes : aucune donnée de contact réelle.

Format : une page, responsive.
```

### Étape SC-2 · La FAQ comme asset

1. Téléversez `data/faq-atelier-nova.md` (fourni) dans le dossier d'assets du projet.
2. Demandez à l'Agent de vérifier le découpage.

📋 **Prompt à coller**

```text
J'ai ajouté assets/faq-atelier-nova.md. Vérifie qu'elle est bien
découpée en passages courts, chacun avec un titre de question clair :
c'est ce découpage qui servira de base de recherche au chatbot.
Ne construis rien d'autre pour l'instant.
```

> [!TIP]
> **✅ Vous devez voir**
> - L'Agent confirme un découpage par question (Horaires, Tarifs, Délais, Annulations et retours), ou propose un ajustement si un passage est trop long.

---

## ✅ Point de contrôle
- [ ] Logo et images visibles sur la page publiée.
- [ ] Noms de fichiers clairs, images compressées, droits vérifiés.
- [ ] 🧵 Service client : site vitrine publié, FAQ chargée et découpée par question.

## 🧠 À retenir
- Un asset existe, mais il ne sert que s'il est **cité dans le prompt**.
- Ce qui est publié est public : jamais de donnée réelle dans un asset.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'Agent ne trouve pas le fichier cité | Vérifiez le chemin exact dans l'éditeur de fichiers (`assets/logo-...png`) et recopiez-le tel quel dans le prompt. |
| Les images téléversées sont trop lourdes | Compressez-les avant de recommencer (un outil en ligne gratuit suffit), ou utilisez des images plus petites. |
| La FAQ est reconnue comme un seul bloc, pas découpée par question | `Redécoupe assets/faq-atelier-nova.md en un passage par question, avec le titre de la question en gras devant chaque réponse.` |

</details>

---

➡️ **Lab suivant :** [LAB-05 · Importer un projet de départ](LAB-05-import.md)
