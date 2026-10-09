# Portfolio BTS SIO — Gwenaël PLEDEL

Portfolio personnel réalisé dans le cadre du BTS SIO et publié gratuitement avec **Jekyll et GitHub Pages**.

🌐 **Site public :** https://vzsca.github.io/Portfolio-Gwenael/

## Présentation

Ce site présente mon profil, mes réalisations scolaires et personnelles ainsi que les compétences du bloc 1 du BTS SIO associées à ces projets. Je m'intéresse particulièrement à la **cybersécurité**, au **pentest**, aux systèmes et aux réseaux.

Le portfolio est conçu pour évoluer au fil de ma formation et servir de support pour présenter mes travaux, notamment dans le cadre de la recherche de stage et de l'épreuve E5.

## Identité visuelle et interface

Le site utilise un thème sombre inspiré des terminaux Linux et des éditeurs de code :

- arrière-plan très sombre, panneaux discrets et accents verts ;
- fenêtres de type terminal avec barre supérieure et trois pastilles ;
- typographies **JetBrains Mono** et **Space Grotesk** ;
- interface sobre, sans éléments décoratifs superflus ;
- navigation commune entre l'accueil, les fiches projets et les mentions légales ;
- mise en page responsive pour les écrans d'ordinateur et de téléphone ;
- états de survol et indicateurs visuels cohérents avec la palette du site.

Les fiches projets et la page des mentions légales reprennent la même identité visuelle que l'accueil, afin d'éviter les ruptures de style entre les pages.

## Fonctionnalités

- Présentation du profil et des objectifs professionnels.
- Classement automatique des projets scolaires et personnels.
- Tableau des compétences du bloc 1 relié aux fiches projets.
- Pages détaillées pour les réalisations, avec contexte, moyens, étapes, preuves et bilan.
- Page de mentions légales.
- Liens de contact et vers GitHub / LinkedIn.
- Génération statique avec Jekyll et publication par GitHub Pages.

## Organisation du dépôt

- `index.html` — accueil, profil, projets, tableau des compétences et contact
- `_projets/` — fiches des réalisations, générées automatiquement
- `_layouts/default.html` — structure commune, navigation et pied de page
- `_layouts/projet.html` — mise en page des fiches projets
- `_data/competences.yml` — référentiel des compétences
- `css/style.css` — thème visuel, composants et règles responsive
- `images/` — captures utilisées dans les fiches projets
- `mentions-legales.md` — mentions légales
- `_config.yml` — configuration Jekyll, URL, collection et coordonnées
- `LICENSE` — licence du code

## Ajouter une réalisation

1. Copier `_projets/_A-COPIER.md` dans le dossier `_projets/`.
2. Nommer le fichier au format `AAAA-MM-sujet.md`, avec des minuscules et des tirets.
3. Renseigner les métadonnées Jekyll : titre, date, cadre, type, résumé et compétences.
4. Décrire le contexte, les moyens, les étapes réalisées, les preuves et les enseignements tirés.
5. Ajouter les captures utiles dans `images/` avec un texte alternatif descriptif.
6. Vérifier les liens et le rendu de la fiche, puis commit les changements.
7. Contrôler le déploiement GitHub Pages sur ordinateur et mobile.

La page d'accueil trie les fiches à partir de leur champ `type` (`ecole` ou `perso`) et génère les liens ainsi que le tableau des compétences depuis les données des projets.

## Publication et maintenance

Le site est publié via GitHub Pages à partir de la branche `main`. Jekyll génère les pages à partir des fichiers Markdown, des layouts et des données du dépôt.

Après une modification importante, vérifier notamment :

- le chargement du CSS et des polices ;
- la navigation et les liens entre les pages ;
- l'affichage des fiches projets et des mentions légales ;
- la lisibilité sur ordinateur et téléphone ;
- le statut du déploiement GitHub Pages.

La feuille de style utilise un paramètre de version dans le layout pour faciliter le rafraîchissement du cache après une modification visuelle.

## Licences

- **Code HTML/CSS et éléments techniques :** licence MIT, selon le fichier `LICENSE`.
- **Textes et captures personnelles du portfolio :** licence CC BY 4.0, sauf mention contraire.

Consulter le fichier `LICENSE` et les [mentions légales](https://vzsca.github.io/Portfolio-Gwenael/mentions-legales/).

## Auteur

**Gwenaël PLEDEL** — étudiant en première année de BTS SIO.
