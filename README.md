# Wellness Maison Beauté — Landing Page

Maquette semi-fonctionnelle de la landing page du salon **Wellness Maison Beauté** (Agen, 47000).

## Ouvrir dans un navigateur

Aucune installation requise. Double-cliquez simplement sur `index.html`, ou faites un glisser-déposer du fichier dans Chrome ou Firefox.

> **Note :** Le chargement des images Unsplash et de la police Google Fonts nécessite une connexion internet.

---

## Modifier les couleurs

Les couleurs sont centralisées dans le bloc `tailwind.config` situé en haut du fichier `index.html` (balise `<script>` après le CDN Tailwind) :

```js
tailwind.config = {
  theme: {
    extend: {
      colors: {
        nude:        '#E6D5C3',   // Fond secondaire, cartes
        dore:        '#B4975A',   // Accents, boutons, bordures
        'dore-dark': '#8f7340',   // Hover sur boutons dorés
        creme:       '#FAF7F2',   // Fond principal
        anthracite:  '#2B2B2B',   // Texte principal
      },
    },
  },
}
```

Changez une valeur hexadécimale et rechargez le navigateur — toutes les classes Tailwind (`bg-dore`, `text-nude`, etc.) s'adapteront automatiquement.

---

## Remplacer les images placeholder

Toutes les images proviennent d'Unsplash via URL directe. Remplacez chaque attribut `src` par le chemin de votre vraie photo :

| Section | Sélecteur à trouver dans le code | Remplacer par |
|---------|----------------------------------|---------------|
| Hero | `photo-1560066984` | Photo d'ambiance salon |
| À propos | `photo-1522337360` | Photo intérieur salon |
| Prestations (×7) | `photo-161668...` etc. | Photos de chaque soin |
| Maëva | `photo-1508214751` | Portrait Maëva |
| Nawel | `photo-1531746020` | Portrait Nawel |
| Mélanie | `photo-1487412720` | Portrait Mélanie |

**Conseil :** Placez vos photos dans un dossier `images/` à côté de `index.html` et utilisez des chemins relatifs, par exemple `src="images/hero.jpg"`.

---

## Modifier le lien Planity

Recherchez dans `index.html` la chaîne :

```
https://www.planity.com/wellness-maison-beaute-47000-agen
```

Elle apparaît 4 fois (header, hero, prestations, contact). Remplacez-la par votre URL Planity définitive.

---

## Structure des sections

```
#accueil      → Hero plein écran
#a-propos     → Présentation de la maison
#prestations  → Grille de 7 cartes de soins
#equipe       → Portraits de Maëva, Nawel, Mélanie
#infos        → Infos pratiques (retards, paiements)
#contact      → Adresse, horaires, Google Maps
footer        → Navigation légale, SEO local
```

---

## Checklist avant mise en ligne

- [ ] Remplacer toutes les images placeholder par les vraies photos
- [ ] Renseigner l'adresse exacte du salon (section Contact)
- [ ] Ajouter le numéro de téléphone
- [ ] Lier les profils Instagram et Facebook réels
- [ ] Rédiger les pages Mentions légales, CGV, Politique de confidentialité
- [ ] Vérifier l'URL Planity définitive
- [ ] Héberger sur un serveur HTTPS (requis pour les iframes Google Maps)
- [ ] Mettre à jour `og:url` dans les balises Open Graph
