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

- Toujours pousser directement sur `main` (GitHub Pages sert depuis main)
- Le site se déploie en 1-2 minutes après chaque push
