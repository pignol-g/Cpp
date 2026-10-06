# My PadThai — commande

Mini-app web statique (HTML/CSS/JS, sans dépendance ni build) pour préparer une commande au food
truck My PadThai (Pusignan) : carte avec les prix, quantités, nombre de personnes, plafond par
personne avec écart en temps réel (vert / rouge), heure de récupération, puis message prêt à
envoyer (affiché, copié dans le presse-papier, brouillon SMS). Outil personnel, non affilié au food truck.

- URL : https://pignol-g.github.io/Cpp/mypadthai/
- Installation sur Android : Chrome → menu ⋮ → « Installer l'application » (ou « Ajouter à l'écran
  d'accueil »). Une fois ouverte une fois, l'app fonctionne aussi hors ligne.

## Modifier la carte

Éditer le bloc `MENU` au début du `<script>` de `index.html` (prix en **centimes**). Plafond par
personne : `MAX_PER_PERSON`. Numéro du food truck : `SHOP`.

Prix relevés sur la photo du menu de septembre 2026 : faits volatils, à revérifier. Le prix du riz
au poulet teriyaki n'était pas lisible : supposé 11 € et affiché « prix à confirmer ».

## Tester en local

```bash
python3 -m http.server 8000   # à la racine du repo, puis http://localhost:8000/mypadthai/
```

## Hébergement

Les pages GitHub Pages d'un même compte partagent une seule origine (`pignol-g.github.io`) : le
stockage local et les caches du navigateur sont communs. L'app n'utilise que la clé `mypadthai.v1`
et les caches `mypadthai-*`. Le `index.html` à la racine du repo est une autre page : ne pas y toucher.
