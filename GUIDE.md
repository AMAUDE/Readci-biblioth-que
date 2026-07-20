# 📖 Guide d'utilisation — Bibliothèque Numérique de Recherche (Côte d'Ivoire)

Ce guide est écrit pour une personne **qui ne code pas**. Suivez simplement les étapes.

---

## 1. Ce que fait la plateforme

C'est un site web où l'on peut **chercher, consulter et télécharger** des documents de recherche :
**livres, articles, mémoires et thèses**.

- Page d'accueil (`index.html`) : recherche par titre / auteur / mot-clé, filtres par **type**, **revue**, **domaine** et **année**.
- Page « Ajouter un document » (`ajouter.html`) : pour enrichir la bibliothèque **sans écrire de code**.

Le site est déjà rempli avec **305 articles réels** des revues **GÉOTROPE** et **RETSSA**.

---

## 2. Mettre le site en ligne (GitHub Pages — gratuit)

> À faire **une seule fois**. Vous avez déjà un compte GitHub.

### Étape A — Créer le dépôt
1. Allez sur **https://github.com/new**.
2. **Repository name** : `bibliotheque-ci` (ou un autre nom).
3. Laissez **Public**, ne cochez rien d'autre, cliquez **Create repository**.

### Étape B — Envoyer les fichiers
1. Sur la page du dépôt, cliquez **Add file → Upload files**.
2. **Glissez-déposez tous les fichiers** : `index.html`, `ajouter.html`,
   `catalogue.json`, `README.md`, `GUIDE.md`, `.nojekyll` (et le dossier `pdfs/`).
3. En bas, cliquez **Commit changes**.

> 💡 Le fichier `catalogue.json` doit rester **à la racine** (à côté de `index.html`).

### Étape C — Activer la mise en ligne
1. Dans le dépôt, ouvrez **Settings** (⚙️) → menu de gauche **Pages**.
2. Sous **Branch**, choisissez **`main`** et le dossier **`/ (root)`**, puis **Save**.
3. Patientez 1–2 minutes : l'adresse de votre site apparaît en haut, du type :
   **`https://VOTRE-NOM.github.io/bibliotheque-ci/`**

C'est en ligne ! Partagez ce lien.

---

## 3. Ajouter un document (la méthode facile, sans code)

> C'est la méthode recommandée. Vous utilisez le formulaire du site.

1. **Préparez le PDF.** Renommez-le proprement, sans espaces ni accents
   (ex. `these-koffi-2024.pdf`).
2. **Déposez le PDF dans le dossier `pdfs/`** sur GitHub :
   - Ouvrez le dossier `pdfs` dans votre dépôt → **Add file → Upload files** → déposez le PDF → **Commit changes**.
3. **Ouvrez la page « Ajouter un document »** de votre site en ligne
   (`https://VOTRE-NOM.github.io/bibliotheque-ci/ajouter.html`).
4. **Remplissez la fiche** : type, titre, auteurs, année, revue/source, domaine.
   - Laissez l'option **« PDF dans le dossier pdfs »** et écrivez le **nom exact** du fichier déposé.
   - (Ou choisissez **« Lien web »** et collez une adresse `https://…` si le PDF est ailleurs.)
5. Cliquez **« Ajouter à la liste »**. Répétez pour plusieurs documents si besoin.
6. Cliquez **« ⬇ Télécharger catalogue.json »**. Un fichier `catalogue.json` est téléchargé.
7. **Remplacez l'ancien catalogue** sur GitHub :
   - Ouvrez la racine du dépôt → cliquez sur `catalogue.json` → icône **crayon** (Edit)… 
   - **Le plus simple** : dans la racine du dépôt, faites **Add file → Upload files**, déposez le nouveau `catalogue.json` (même nom) → **Commit changes**. Il remplace l'ancien.

Rafraîchissez le site : votre document apparaît. 🎉

---

## 4. Ajouter un document (méthode manuelle, en secours)

Si vous préférez éditer la liste directement :

1. Déposez le PDF dans `pdfs/` (comme ci-dessus).
2. Ouvrez `catalogue.json` sur GitHub, cliquez le **crayon** (Edit).
3. Copiez un bloc existant et adaptez-le. Un document ressemble à ceci :

```json
{
 "id": "doc-306",
 "type": "these",
 "titre": "Titre complet du document",
 "auteurs": "NOM Prénom, NOM Prénom",
 "annee": "2024",
 "revue": "Université Félix Houphouët-Boigny",
 "numero": "",
 "source": "UFHB",
 "domaine": "Géographie & Environnement",
 "lien": "",
 "fichier": "mon-document.pdf"
}
```

- `type` doit être : `article`, `livre`, `memoire` ou `these`.
- Mettez **soit** `fichier` (nom du PDF dans `pdfs/`) **soit** `lien` (adresse web).
- Chaque `id` doit être **unique**.
- Séparez chaque document par une **virgule**. Le tout reste entre les crochets `[...]`.

> ⚠️ Cette méthode demande de respecter la ponctuation (virgules, guillemets).
> En cas de doute, préférez la **méthode facile (section 3)** qui évite toute erreur.

---

## 5. Types de documents

| Type à saisir | Affiché comme |
|---|---|
| `article` | Article |
| `livre` | Livre |
| `memoire` | Mémoire |
| `these` | Thèse |

La bibliothèque accepte donc **livres, articles, mémoires et thèses**, chacun avec son étiquette de couleur.

---

## 6. Questions fréquentes

**Le PDF ne s'ouvre pas ?**
Vérifiez que le nom écrit dans la fiche est **exactement** le même que le fichier dans `pdfs/`
(mêmes majuscules, pas d'espace en trop).

**Puis-je utiliser des liens vers des PDF déjà en ligne ?**
Oui. Dans la fiche, choisissez **« Lien web »** et collez l'adresse. C'est ce qui est utilisé
pour les 305 articles de départ (ils pointent vers les sites des revues GÉOTROPE et RETSSA).

**Comment changer le titre ou les couleurs du site ?**
Tout est dans `index.html`. Vous pouvez demander de l'aide pour toute personnalisation.

**Est-ce vraiment gratuit ?**
Oui, GitHub Pages héberge gratuitement ce type de site.

---

## 7. Origine des données de départ

Les 305 documents pré-chargés proviennent des sites officiels :
- GÉOTROPE — https://www.revuegeotrope.com/
- RETSSA — https://www.retssa-ci.com/

Ces revues offrent déjà un **accès libre** ; la plateforme ne fait que les rassembler et faciliter
la recherche. Les droits restent la propriété des auteurs et des revues.
