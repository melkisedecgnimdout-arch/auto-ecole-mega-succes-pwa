# AUTO-ECOLE MEGA SUCCES — Dossier de Production PWA

Développeur (Approbation & Support) : melkisedecgnimdout@gmail.com
Auto-École (Admin) : succesmega70@gmail.com
Lieux : Sanguéra à côté de la poste • Noépé rond-point Akassimé
Tarif d'activation : 1 000 FCFA par apprenant • Numéro marchand : 93 73 66 65

## Contenu du dossier
- `index.html` : Interface PWA mobile-first.
- `style.css` : Feuille de styles responsive mobile-first.
- `manifest.json` : Métadonnées PWA pour installation sur écran d'accueil.
- `sw.js` : Service Worker de mise en cache et fonctionnement hors-ligne.
- `icon-192.png` et `icon-512.png` : Icônes d'application.
- `Code.gs` : Script backend Google Apps Script connecté à Google Sheets.

## Étapes de déploiement en production
1. Créez un Google Sheet avec 4 onglets : `Users`, `Cours`, `Questions_Examen`, `Forum`.
2. Dans `Users`, ajoutez la ligne d'en-tête puis le compte administrateur avec `succesmega70@gmail.com`, `role` = `admin`, `statut` = `actif`, `ecole_id` = `MEGA_SUCCES_01`.
3. Dans **Extensions > Apps Script**, collez `Code.gs`, puis cliquez sur **Déployer > Nouveau déploiement > Application Web** (*Exécuter en tant que : Moi*, *Qui a accès : Tout le monde*).
4. Copiez l'URL `/exec` générée et collez-la dans `DEFAULT_API_URL` de `index.html` (ou saisissez-la sur l'écran de connexion).
5. Mettez en ligne `index.html`, `style.css`, `manifest.json`, `sw.js`, `icon-192.png` et `icon-512.png` sur un hébergeur HTTPS (GitHub Pages, Netlify ou Vercel).
6. Ouvrez le lien HTTPS sur smartphone (Chrome ou Safari) et choisissez **Ajouter à l'écran d'accueil**.
