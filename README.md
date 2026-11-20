# Fond d'écran Libre — flux de données

Miroir statique des données du site [Fond d'écran Libre](https://fondsecranlibre.free.je),
servi par GitHub Pages pour l'application Android.

Pourquoi ce dépôt ? L'hébergeur du site (InfinityFree) bloque les clients HTTP
non-navigateurs avec un défi JavaScript : l'appli Android ne peut pas récupérer
les données ni les images directement depuis le site. Ce dépôt public sert donc
de source de données : JSON + images WebP, accessibles sans défi.

## Contenu

- `wallpapers.json` — catalogue complet : version, date de mise à jour,
  6 collections thématiques, liste des fonds (id, titre, catégorie, tags,
  description, nom d'image, date d'ajout, téléchargements).
- `images/` — les images WebP (1152×2048, 9:16), une par fond.
- `.nojekyll` — désactive Jekyll pour que GitHub Pages serve les fichiers tels quels.

## URLs (GitHub Pages)

- Catalogue : <https://arthur-falola.github.io/fond-ecran-libre-data/wallpapers.json>
- Images : `https://arthur-falola.github.io/fond-ecran-libre-data/images/<nom-de-fichier>`
  (voir aussi le champ `images_base_url` dans `wallpapers.json`).

## Mise à jour

Chaque nouveau fond publié sur le site est synchronisé ici :
image copiée dans `images/`, entrée ajoutée à `wallpapers.json`
(nouvel id = max + 1, `updated` rafraîchi), puis commit + push.
Voir `SYNC-DATA.md` dans le projet (espace de travail Muse).

## Données

100 % publiques : titres, descriptions, tags et images des fonds.
Aucun secret, aucun identifiant, aucune donnée personnelle dans ce dépôt.
