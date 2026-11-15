# Site personnel de Fidy Heritiana Andrianarivony

Site public : **https://fidy-heritiana.github.io/**

Ce dépôt contient la page personnelle, les liens vers les six projets de
recherche publics et les publications sélectionnées. Le site fonctionne
directement sur GitHub Pages, sans installation ni compilation.

## Fichiers du site

| Fichier | Rôle |
| --- | --- |
| `index.html` | Page complète : contenu, mise en forme, recherche, filtres et traduction française. |
| `sitemap.xml` | Adresse de la page et date de sa dernière modification significative. |
| `robots.txt` | Indique l'adresse du sitemap aux moteurs de recherche. |
| `googlec419fc1c171fb5b7.html` | Fichier existant de validation Google Search Console, à conserver tel quel. |
| `README.md` | Le présent guide de gestion du site. |

La nouvelle présentation n'exige aucune modification des réglages de publication
GitHub Pages. Elle conserve la même adresse et le fichier de validation Google.

## Mettre à jour la présentation

1. Ouvrir ce dépôt, puis **Add file → Upload files**.
2. Envoyer `index.html`, `sitemap.xml`, `robots.txt` et `README.md` à la racine.
3. Enregistrer avec **Commit changes** sur la branche `main`.
4. Attendre la publication GitHub Pages, puis consulter le site public.

Le fichier Google déjà présent n'est pas à remplacer ou à supprimer. Son adresse
doit rester accessible :
https://fidy-heritiana.github.io/googlec419fc1c171fb5b7.html

## Ce que propose la page

- Un accès aux **six dépôts de recherche**, même sans JavaScript.
- Des boutons vers les **trois applications Streamlit déjà référencées**.
- Des filtres par démonstration, hiérarchie et probabilités.
- Une recherche qui accepte les termes français ou anglais, avec ou sans accents.
- Un bouton **FR / EN**. L'anglais est affiché par défaut et le choix de langue
  est mémorisé dans le navigateur lorsque son stockage est disponible.
- Des liens vers les articles, les versions logicielles Zenodo, ORCID et GitHub.
- Une présentation adaptée au téléphone et à la navigation au clavier.

## Modifier un texte ou un lien

Dans GitHub, ouvrir `index.html` et cliquer sur le crayon pour modifier le fichier.
Rechercher le texte ou le nom du projet concerné.

Les textes traduits suivent cette convention :

```html
<p data-fr="Le texte en français.">The text in English.</p>
```

Modifier le texte anglais entre les balises et sa traduction dans `data-fr`.
Pour un lien, modifier uniquement l'adresse placée dans `href="..."`.

Le nom du dépôt de chaque projet apparaît dans un commentaire commençant par
`PROJECT`. Cela permet de retrouver rapidement la bonne fiche.

Après une modification significative de la page, actualiser la date `lastmod`
du fichier `sitemap.xml`, au format `AAAA-MM-JJ`.

## Ajouter un projet

1. Dans `index.html`, copier un bloc complet allant de
   `<article class="project" ...>` jusqu'à son `</article>`.
2. Le placer dans le bloc `project-grid`, avant le message `empty-state`.
3. Modifier son titre, sa description, son lien GitHub et ses éventuels liens
   vers une démonstration, un article ou un DOI.
4. Dans `data-categories`, indiquer les filtres pertinents, séparés par un espace :
   `demo`, `hierarchies`, `probability`.
5. Compléter `data-search` avec les mots utiles en français et en anglais.
6. Actualiser les totaux éditoriaux dans la description de la page et la ligne
   « 6 projects · 3 demonstrations », ainsi que leur traduction. Le compteur des
   résultats de recherche, lui, se recalcule automatiquement.

Ajouter `demo` uniquement lorsqu'une application a été effectivement déployée et
son adresse vérifiée. Le lien « Tous les dépôts GitHub » donne aussi accès aux
nouveaux dépôts avant leur ajout manuel au catalogue.

## État des projets présentés

| Projet | Ressources reliées depuis la page |
| --- | --- |
| Quicksort–Mallows | Démonstration, code et DOI logiciel. |
| Construction gloutonne | Démonstration, code et DOI logiciel. |
| Algorithme de Gras et comparaison | Démonstration, code et DOI logiciel. |
| Construction avec un tas et un parcours de graphe | Code, données et DOI logiciel. |
| Modèle aléatoire Ewens–Catalan | Dépôt de recherche. |
| Génération des structures par une approche de Boltzmann | Documentation et article associé. |

La démonstration du dépôt `A-fast-algorithm-for-constructing-an-oriented-hierarchy`
pourra être reliée à sa fiche après sa mise en ligne. Son DOI actuel identifie
la version `v1.0.0` des scripts.

Le dépôt de génération de structures est présenté comme une ressource
documentaire : ses fichiers Python actuels ne contiennent pas une implémentation
exécutable complète. La page ne leur attribue donc pas une démonstration active.

## Google Search Console

Le sitemap corrigé utilise l'espace de noms officiel :
`http://www.sitemaps.org/schemas/sitemap/0.9`.

Une fois la nouvelle page publiée, son adresse reste :
https://fidy-heritiana.github.io/sitemap.xml

La validation existante reste fondée sur la présence du fichier Google. Une
modification de la présentation n'exige pas à elle seule une nouvelle validation.
La prise en compte des changements dans les résultats de recherche dépend du
prochain passage de Google et n'est pas immédiate.

Documentation officielle :
- https://support.google.com/webmasters/answer/9008080?hl=fr
- https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap

## Annuler une modification

GitHub conserve les versions précédentes dans l'historique des commits. Pour une
correction ponctuelle, ouvrir une version antérieure du fichier dans **History**,
copier son contenu puis l'enregistrer dans un nouveau commit. Le fichier de
validation Google doit rester présent pendant ces opérations.
