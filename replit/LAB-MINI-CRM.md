# LAB-MINI-CRM · Site, formulaire et mini CRM

> **En une phrase —** Un site vitrine pour Atelier Nova, un formulaire qui tombe sur un mini CRM, des leads qui deviennent des prospects, et les demandes B2B traitées en priorité.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 2 h 55 (9 étapes) | Nouveau projet `Web app`, `atelier-nova-crm` | LAB-PROJECT-MANAGEMENT |

## 🎯 À la fin de ce lab
- Une page vitrine publiée, avec assets cités dans le prompt.
- Un formulaire de contact qui crée un lead dans le mini CRM.
- Un connecteur natif et un serveur MCP, connectés puis déconnectés.
- Des leads suivis, des prospects créés, des actions prioritaires définies, avec les demandes B2B en tête.

---

## Étape 1 · Page vitrine avec assets · ⏱️ 20 min

1. Trouvez ou créez un logo simple et deux images libres de droits. À défaut, utilisez les trois fichiers fournis dans [`data/assets/`](data/assets/) (`logo-atelier-nova.svg`, `illustration-salle.svg`, `illustration-fleurs.svg`).
2. Téléversez-les dans le dossier `assets/` du projet Replit, avec des noms clairs (`logo-atelier-nova.svg`, pas `image1.svg`).

📋 **Prompt à coller (en Build)**

```text
Construis la page d'accueil du site vitrine d'Atelier Nova en
utilisant assets/logo-atelier-nova.svg comme logo et les deux images
du dossier assets/ en illustration. Trois services, un bouton de
contact.
```

3. Publiez (Deployments).

> [!TIP]
> **✅ Vous devez voir**
> Logo et images réellement affichés sur la page publiée, pas seulement dans l'éditeur.

## Étape 2 · Formulaire de contact · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Ajoute un formulaire de contact : nom, e-mail, entreprise (facultatif),
besoin. Les champs nom, e-mail et besoin sont obligatoires. Affiche
une erreur claire si un champ obligatoire manque.
```

> [!TIP]
> **✅ Vous devez voir**
> Un envoi réussi avec tous les champs remplis, une erreur claire si un champ obligatoire manque.

## Étape 3 · Formulaire → CRM · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Chaque envoi du formulaire doit créer un lead dans un mini CRM : nom,
e-mail, entreprise, besoin, source « Formulaire », statut « Nouveau ».
Affiche la liste des leads dans un écran réservé à l'équipe.
```

1. Envoyez un formulaire de test et retrouvez le lead créé.

> [!TIP]
> **✅ Vous devez voir**
> Le lead apparaît avec la source « Formulaire » et le statut « Nouveau ».

## Étape 4 · Connecteur et MCP · ⏱️ 20 min

1. Dans la barre latérale, ouvrez **Integrations**.
2. Recherchez **Google Drive**  choisissez un compte de **test**.

📋 **Prompt à coller (connecteur natif)**

```text
Quand un nouveau lead est créé, dépose un résumé dans un dossier de
test sur le Drive connecté.
```

3. Installez ensuite un serveur MCP en un clic, et utilisez-le une fois dans le chat.
4. Déconnectez les deux accès en fin d'étape.

> [!WARNING]
> ⚠️ Compte de test uniquement, aucune donnée réelle.

> [!TIP]
> **✅ Vous devez voir**
> Les deux connexions fonctionnelles, puis déconnectées — vous savez dire laquelle demande une autorisation OAuth, laquelle une URL.

## Étape 5 · Vérifier la liaison de bout en bout · ⏱️ 20 min

1. Ouvrez le site publié dans un nouvel onglet, sans être connecté à l'équipe.
2. Envoyez un formulaire test avec des données clairement identifiables (« Test liaison »).
3. Revenez à la liste des leads et retrouvez-le en moins d'une minute.
4. Si la liaison échoue, diagnostiquez en **Plan**, corrigez en **Build**.

> [!TIP]
> **✅ Vous devez voir**
> Le lead « Test liaison » visible côté équipe, avec la bonne source.

## Étape 6 · Ajouter des leads à la main · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Permets à l'équipe d'ajouter un lead manuellement (nom, e-mail,
entreprise, besoin, source libre) et de changer son statut parmi :
Nouveau, Contacté, Qualifié, Gagné, Perdu.
```

1. Créez trois leads à la main, avec la source « Manuelle ».
2. Faites passer l'un d'eux de « Nouveau » à « Contacté » puis « Qualifié ».

> [!TIP]
> **✅ Vous devez voir**
> Trois leads créés, statut modifiable et persistant.

## Étape 7 · Créer des prospects · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Ajoute une fiche « Prospect » distincte du lead : entreprise, contact
principal, besoin détaillé, historique des échanges. Un bouton
« Convertir en prospect » sur un lead Qualifié crée cette fiche et
garde le lien vers le lead d'origine.
```

1. Convertissez le lead « Qualifié » de l'étape 6 en prospect.

> [!TIP]
> **✅ Vous devez voir**
> Une fiche prospect complète, avec l'historique qui remonte au lead d'origine.

## Étape 8 · Actions prioritaires du CRM · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Ajoute un champ « Priorité » sur les prospects (Normale, B2B) et un
tri qui place les prospects B2B en tête de liste. Ajoute un champ
« Prochaine action » (texte libre) sur chaque prospect.
```

1. Marquez deux prospects « B2B » et vérifiez qu'ils remontent en tête.
2. Définissez une prochaine action pour chacun des trois prospects.

> [!TIP]
> **✅ Vous devez voir**
> Les prospects B2B en tête de liste, une action écrite pour chacun.

## Étape 9 · Relances et filtres · ⏱️ 15 min

📋 **Prompt à coller (en Build)**

```text
Ajoute une date de relance sur chaque prospect, un filtre par statut
ou par priorité sur la liste, et un bouton d'export de la liste
filtrée (CSV ou Excel).
```

> [!TIP]
> **✅ Vous devez voir**
> Une relance visible et triable par date, un export qui s'ouvre et correspond au filtre appliqué.

---

## ✅ Point de contrôle
- [ ] Site publié avec logo et images réellement affichés.
- [ ] Formulaire → lead fonctionnel, source correcte.
- [ ] Connecteur et MCP testés puis déconnectés.
- [ ] Liaison de bout en bout vérifiée.
- [ ] Trois leads créés à la main, un converti en prospect.
- [ ] Prospects B2B en tête, actions et relances définies, export fonctionnel.

## 🧠 À retenir
- Un formulaire qui ne crée pas de lead vérifiable n'est qu'une page qui a l'air de marcher.
- Les priorités (B2B en tête) sont une décision métier à câbler explicitement : l'Agent ne les devine pas.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Le lead du formulaire public n'apparaît pas | Vérifiez que le formulaire écrit bien dans la même base que l'écran CRM de l'équipe. |
| La conversion lead → prospect perd des données | Redemandez explicitement que tous les champs du lead soient repris dans la fiche prospect. |
| Les prospects B2B ne remontent pas en tête | Vérifiez l'ordre de tri exact demandé (priorité, puis date) dans le prompt de l'étape 8. |

</details>

---

➡️ **Lab suivant :** [LAB-DEBOGAGE · Cinq cas, un par fil](LAB-DEBOGAGE.md)
