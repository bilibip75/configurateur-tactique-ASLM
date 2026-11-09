# ASLM — Éditeur Tactique Football (PWA)

PWA mobile d'aide à la composition d'équipes de football à 11 pour l'AS Laneuveville Marainviller.

## Déploiement GitHub + Render

Le dépôt est prêt pour un **site statique Render**. Le fichier `render.yaml` contient la configuration du service.

1. Ouvrir le dépôt GitHub `https://github.com/bilibip75/configurateur-tactique-ASLM`.
2. Déposer **le contenu de ce dossier à la racine du dépôt**, sur la branche principale.
3. Dans Render, choisir **New > Blueprint**.
4. Connecter le dépôt `bilibip75/configurateur-tactique-ASLM`, puis valider la configuration détectée dans `render.yaml`.
5. Attendre le statut **Live**, puis ouvrir l'adresse HTTPS `*.onrender.com`.
6. Sur mobile, ouvrir l'adresse puis utiliser **Installer l'app** ou **Ajouter à l'écran d'accueil**.

Les mises à jour poussées sur la branche principale sont redéployées automatiquement par Render.

## Test local

```bash
python3 -m http.server 8080
```

Puis ouvrir `http://localhost:8080/`.

## Fichiers principaux

- `index.html` : application complète
- `manifest.webmanifest` : métadonnées PWA
- `sw.js` : service worker et cache hors ligne
- `icons/` : icônes standards, adaptatives et Apple Touch
- `render.yaml` : configuration du site statique Render et en-têtes de sécurité

## Points importants

- L'actualisation depuis Google Sheets nécessite une connexion Internet et des feuilles accessibles à l'application.
- Les photos et les sauvegardes restent locales à chaque navigateur/appareil.
- Les identifiants administrateur sont stockés localement dans le navigateur. Le contrôle administrateur de cette version masque l'interface sensible, mais ne constitue pas une authentification serveur.
- Pour forcer les appareils à recevoir une nouvelle version de l'application après modification, incrémenter `CACHE_NAME` dans `sw.js`.
