# La Ferme Fanost — Instructions pour Claude

## Règle bilingue FR/EN — OBLIGATOIRE

Le site est bilingue français/anglais. **Toute modification de texte doit être faite dans les deux langues simultanément**, sans exception.

### Pattern utilisé dans le HTML

```html
<span class="fr">Texte en français</span><span class="en">English text</span>
```

- La classe `lang-fr` sur `<html>` affiche les `.fr` et masque les `.en`
- La classe `lang-en` fait l'inverse
- Le bouton FR/EN dans la nav bascule entre les deux via `localStorage`

### À faire à chaque modification

- Modifier du texte → mettre à jour **les deux** `<span class="fr">` et `<span class="en">`
- Ajouter une nouvelle section → inclure **les deux versions** dès le départ
- Ajouter un bouton ou lien avec du texte → wrap avec les deux spans

### Structure des fichiers

- `index.html` — site principal (lafermefanost.com)
- `bienvenue/index.html` — page d'accueil clients (lafermefanost.com/bienvenue/)
- `photos/` — toutes les images du site
- `photos/favicon.jpg` — favicon (FF sur fond vert)
- `photos/1774740617407_logolaferme-02.png` — logo beige (utilisé dans bienvenue)
- `photos/1774740617407_logolaferme-01.png` — logo blanc

### Déploiement

- Site servi par **Cloudflare Pages** (compte Cloudflare lafermefanost@gmail.com, projet `ferme-fanost`, relié à ce dépôt) : chaque mise à jour de `main` est mise en ligne automatiquement en 1-2 minutes ; chaque branche a son aperçu `<id>.ferme-fanost.pages.dev`. **Pas GitHub Pages** (désactivé — ne pas l'activer, ne pas ajouter de fichier CNAME).
- Domaine `lafermefanost.com` enregistré chez iwantmyname, DNS géré chez Cloudflare (serveurs `nikon` / `rosa.ns.cloudflare.com`) : `lafermefanost.com` et `www.lafermefanost.com` → CNAME `ferme-fanost.pages.dev` (17/11/2026 : `www` pointait encore vers Cargo, l'ancien site). Adresse officielle : `https://www.lafermefanost.com` (canonique, sitemap, robots).
- Pas d'e-mail en @lafermefanost.com (aucun MX) ; contact = lafermefanost@gmail.com en lien `mailto:` (jamais le lien codé `/cdn-cgi/…` de Cloudflare).
