# LAB-06 · Clés API et Secrets

> **En une phrase —** Une clé de test ajoutée dans les Secrets, un appel réussi, la preuve qu'elle n'apparaît nulle part dans le code ou le chat, puis sa révocation — le réflexe compte plus que la clé elle-même.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 25 min | Le projet de votre fil rouge | LAB-05 |

## 🎯 À la fin de ce lab
- Une clé ajoutée dans **Secrets**, utilisée par un appel de test, puis révoquée.
- Vous avez vérifié, par vous-même, qu'elle n'apparaît ni dans le code, ni dans le chat, ni dans la Console.
- 🧵 Selon votre fil : des CV fictifs sécurisés (RH), une classification par compte (Finance), ou la clé prête pour le chatbot RAG (Service client).

---

## Étape 1 · Ajouter la clé de test · ⏱️ 5 min

1. Ouvrez **Tools › Setup › Secrets**.
2. Cliquez sur **New Secret**.
3. Nom (en majuscules) : `LLM_API_KEY`. Valeur : la clé de test fournie par le formateur.
4. Validez.

> [!WARNING]
> ⚠️ Ne collez **jamais** cette clé ailleurs que dans ce champ : pas dans le chat de l'Agent, pas dans un fichier, pas dans la Console.

## Étape 2 · Appel de test · ⏱️ 5 min

📋 **Prompt à coller**

```text
Fais un appel de test au modèle de langage en utilisant la clé
LLM_API_KEY depuis les Secrets (jamais écrite en dur dans le code).
Demande-lui simplement de répondre « test réussi », et affiche le
résultat à l'écran.
```

> [!TIP]
> **✅ Vous devez voir**
> - « test réussi » affiché.
> - Dans le code généré, une lecture par variable d'environnement (`process.env.LLM_API_KEY` ou équivalent), jamais la valeur elle-même.

## Étape 3 · Vérifier qu'elle n'apparaît nulle part · ⏱️ 3 min

1. Ouvrez l'éditeur de fichiers : cherchez (Ctrl+F ou recherche du projet) les premiers caractères de votre clé. Aucun résultat attendu.
2. Faites défiler le chat : la clé ne doit apparaître dans aucun message.
3. Ouvrez la **Console** : même vérification.

## Étape 4 · 🧵 Selon votre fil rouge · ⏱️ 10 min

### Fil RH

📋 **Prompt à coller**

```text
Pour chaque candidature importée, calcule un score sur 100 avec la
grille : compétences 40 %, expérience 30 %, formation 20 %,
langues 10 %, chaque critère noté de 0 à 100 par toi. Explique
chaque sous-note en une phrase. N'utilise aucun nom de personne dans
tes réponses : désigne les candidats par leur identifiant (CAND-01…).
```

> [!TIP]
> **✅ Vous devez voir**
> - Un score par candidature, avec le détail des quatre sous-notes.
> - **CAND-02** (l'ingénieur logiciel senior) obtient un score **moyen**, malgré un profil impressionnant : ses compétences et son expérience ne correspondent pas au poste. C'est le but de ce cas piégé.
> - **CAND-03** (CV incomplet) obtient un score bas, avec une note qui dit explicitement que l'information manquante a été estimée par défaut.
> - **CAND-05** et **CAND-06** (profils identiques, âge et prénom différents) obtiennent le **même score** : si ce n'est pas le cas, c'est un signal de biais à documenter (synthèse de fin de journée).

### Fil Finance

📋 **Prompt à coller**

```text
Classe chacune de ces transactions dans l'un des comptes du plan
comptable simplifié (Loyer, Fournitures, Salaires, Honoraires,
Marketing, Deplacement), avec un niveau de confiance (haut, moyen,
bas) :
TX-0901 Immo Centre SCI, 1450,00 EUR
TX-0904 URSSAF, 3120,50 EUR
TX-0906 SNCF Connect, 134,20 EUR
TX-0910 Bureau Vallée, 54,90 EUR
TX-0912 Meta Ads, 310,00 EUR
TX-0914 Agence Web Plume, 1200,00 EUR
TX-0919 Fournisseur Inconnu SARL, 45000,00 EUR
```

> [!TIP]
> **✅ Vous devez voir**
> - TX-0901→Loyer, TX-0904→Salaires, TX-0906→Deplacement, TX-0910→Fournitures, TX-0912→Marketing, TX-0914→Honoraires, tous en confiance **haute**.
> - **TX-0919** classée avec une confiance **basse** ou signalée comme douteuse : le montant (45 000 € pour un fournisseur inconnu, catégorie Fournitures) ne ressemble à aucune autre ligne. C'est le cas piégé du jeu de données.

### Fil Service client

📋 **Prompt à coller**

```text
Prépare l'appel au modèle pour le futur chatbot : une fonction qui
reçoit une question et un contexte (des passages de la FAQ), et
renvoie une réponse rédigée uniquement à partir de ce contexte. Utilise
la clé LLM_API_KEY depuis les Secrets. Ne construis pas encore la
recherche dans la FAQ : ce sera le LAB-06 (chatbot RAG), étape suivante.
```

> [!TIP]
> **✅ Vous devez voir**
> - Une fonction d'appel au modèle qui lit la clé depuis les Secrets, sans recherche dans la FAQ pour l'instant.

## Étape 5 · Révoquer et remplacer · ⏱️ 2 min

1. Retournez dans **Secrets**, supprimez `LLM_API_KEY`.
2. Si le formateur fournit une seconde clé pour la suite de la journée, ajoutez-la sous le même nom.

---

## ✅ Point de contrôle
- [ ] Appel de test réussi, clé absente du code, du chat et de la Console.
- [ ] 🧵 RH : CAND-05 et CAND-06 ont le même score (ou l'écart est noté comme anomalie).
- [ ] 🧵 Finance : TX-0919 signalée à confiance basse.
- [ ] Clé révoquée en fin de lab.

## 🧠 À retenir
- Les Secrets sont lus comme variable d'environnement, jamais écrits en dur : ce réflexe vaut pour toute clé, toute la journée.
- Une clé qui fuit se révoque et se remplace — elle ne se « cache » pas après coup.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'appel de test échoue | Vérifiez l'orthographe exacte du nom du secret (`LLM_API_KEY`) dans le code généré : une majuscule ou un tiret bas manquant suffit à casser la lecture. |
| CAND-05 et CAND-06 ont des scores différents | `Ces deux candidatures ont des compétences, une expérience, une formation et des langues identiques. Explique pourquoi leurs scores diffèrent, puis recalcule.` |
| TX-0919 est classée en confiance haute | `Un fournisseur inconnu avec un montant aussi élevé que 45 000 € pour la catégorie Fournitures doit être signalé en confiance basse, pas haute. Reclasse.` |

</details>

---

➡️ **Lab suivant :** [LAB-07 · Construire en petites étapes (mode Build)](LAB-07-mode-build.md)
