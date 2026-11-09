ASLM — Éditeur Tactique Football (PWA)
======================================

Déploiement
-----------
1. Décompressez l’archive en conservant tous les fichiers et dossiers.
2. Publiez le dossier sur un hébergement HTTPS (le service worker exige HTTPS, sauf sur localhost).
3. Ouvrez index.html depuis l’adresse HTTPS publiée.
4. Utilisez « Installer l’app » ou la commande d’installation du navigateur.

Test local
----------
Depuis ce dossier :
  python3 -m http.server 8080
Puis ouvrez :
  http://localhost:8080/

Fonctionnement hors ligne
-------------------------
- L’interface, le logo, les tactiques, les sauvegardes locales et les photos déjà stockées restent accessibles.
- La mise à jour Google Sheets nécessite une connexion Internet.
- Sans réseau, la dernière composition locale enregistrée peut toujours être chargée.

Mise à jour
-----------
Le service worker contrôle la version du cache dans sw.js (CACHE_NAME). Pour forcer une nouvelle version après modification, incrémentez ce nom, par exemple aslm-tactique-v2.
