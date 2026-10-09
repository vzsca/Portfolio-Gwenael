# Portfolio BTS SIO — Gwenaël PLEDEL

Portfolio professionnel réalisé dans le cadre du BTS SIO et publié gratuitement avec **Jekyll + GitHub Pages**.

🌐 **Site public :** https://vzsca.github.io/Portfolio-Gwenael/

## À propos

Ce portfolio présente mes réalisations scolaires et personnelles, ainsi que les compétences du bloc 1 du BTS SIO auxquelles elles sont associées. Je m'intéresse particulièrement à la **cybersécurité**, au **pentest** et à l'administration des systèmes et réseaux.

## Direction visuelle

Le site adopte une esthétique inspirée des terminaux et éditeurs de code : fond sombre, accents verts, fenêtres avec barre supérieure, typographie monospace et interface volontairement épurée. Le site reste une page web classique, navigable au clavier et adaptée aux écrans mobiles. Le contenu est en français.

## Structure

- `index.html` — page d'accueil, projets, profil, tableau des compétences et contact
- `_projets/` — fiches de réalisations alimentées automatiquement sur l'accueil
- `_layouts/` — mises en page Jekyll pour le site et les fiches projets
- `_data/competences.yml` — référentiel des six compétences
- `css/style.css` — styles et adaptation mobile
- `images/` — captures utilisées dans les fiches
- `mentions-legales.md` — mentions légales
- `_config.yml` — configuration Jekyll
- `LICENSE` — licence du code

## Ajouter une réalisation

1. Copier le modèle `_projets/_A-COPIER.md` dans un nouveau fichier du dossier `_projets/`.
2. Nommer le fichier au format `AAAA-MM-sujet.md`, en minuscules, avec des tirets.
3. Renseigner le contexte, les moyens, les étapes, les preuves et ce que j'en retiens.
4. Définir le champ `type` à `ecole` ou `perso`, un résumé et les codes de compétences démontrées.
5. Ajouter les captures nécessaires dans `images/` avec un texte alternatif pertinent.
6. Faire un commit puis vérifier le déploiement GitHub Pages.

La page d'accueil classe automatiquement les réalisations en **projets scolaires** et **projets personnels** et met à jour le tableau des compétences.

## Publication et vérifications

Le site est généré par Jekyll et publié avec GitHub Pages. Après chaque modification importante, vérifier le rendu sur ordinateur et mobile, les liens des projets, les mentions légales et le déploiement.

## Licences

- **Code HTML/CSS et éléments techniques du site :** licence MIT.
- **Contenu éditorial et captures personnelles :** licence CC BY 4.0 lorsque cette licence est indiquée sur le site.

Voir `LICENSE` et les [mentions légales](https://vzsca.github.io/Portfolio-Gwenael/mentions-legales/).

## Auteur

**Gwenaël PLEDEL** — étudiant en première année de BTS SIO.
