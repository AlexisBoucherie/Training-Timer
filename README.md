# Timer d'entraînement — PWA

## Fonctionnalités
- Travail, repos et nombre de répétitions configurables.
- 10 secondes de préparation avant la première phase de travail.
- Alternance automatique travail/repos ; pas de repos après la dernière répétition.
- Alertes en voix anglaise ou en bips pendant les cinq dernières secondes et aux transitions.
- Pause/reprise, reset et maintien de l'écran actif lorsque le navigateur le permet.
- Cache hors ligne après le premier chargement.

## Installation sur Samsung Galaxy A55
1. Héberge le contenu de ce dossier sur un hébergement HTTPS statique (par exemple GitHub Pages ou Netlify).
2. Ouvre l'adresse du site dans Chrome sur le téléphone.
3. Menu ⋮ > **Ajouter à l'écran d'accueil** (ou **Installer l'application** si cette option apparaît).
4. Lance le timer depuis l'icône installée et appuie sur **Start** pour autoriser l'audio.

Le service worker et le maintien de l'écran actif nécessitent un contexte sécurisé, généralement HTTPS (localhost est également accepté pour les tests).

## Limites importantes
- La Wake Lock empêche normalement l'extinction automatique de l'écran pendant une séance active, mais Android ou le navigateur peut la révoquer. Le verrouillage manuel du téléphone suspendra ou perturbera le timer : cette PWA n'est pas conçue pour continuer de manière fiable écran verrouillé.
- La voix dépend de la synthèse vocale disponible sur l'appareil et du navigateur. Le mode bips est une alternative.
- Les annonces sonores nécessitent que le navigateur autorise la lecture audio après l'interaction initiale.
