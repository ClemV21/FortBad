#🏸 Fort Bad — Application de gestion de sessions de badminton

Description : Application web complète pour organiser des sessions de badminton entre amis/club : inscription aux sessions, gestion du covoiturage, partage des dépenses et QR codes d'accès aux terrains.

🔗 Lien live : (https://fortbad.zite.so)


Stack technique :
Frontend : React 18, TypeScript, Tailwind CSS, shadcn/ui
Routing : React Router DOM
Backend : API REST avec endpoints TypeScript (architecture serverless)
Base de données : Zite Database (relationnel)
Hébergement : Zite Platform


Fonctionnalités principales :

Gestion des sessions — Création, modification, suppression de sessions avec date, heure, lieu, nombre de terrains et durée
Inscription — Les joueurs s'inscrivent aux sessions (limite automatique basée sur le nombre de terrains × 5 joueurs). Fermeture des inscriptions 24h avant

Covoiturage — Les conducteurs proposent des places, les passagers choisissent un conducteur. Heure de départ configurable
Gestion des dépenses — Système de partage des frais (location terrain, volants, frais voiture). Mode "parts" pour répartition inégale. Calcul automatique des soldes et plan de remboursement

QR Codes — Upload de QR codes d'accès par terrain et créneau horaire, avec lightbox de visualisation
Rôles utilisateurs — Admin (accès total), Viewer (lecture seule), User (inscription et gestion)
Tableau de bord — Vue synthétique : prochaine session, solde, covoiturage, sessions à venir


Architecture :
13 pages : Dashboard, Sessions, Détail session, Covoiturage, Dépenses, Historique, Profil, Admin, etc.
30+ endpoints API : CRUD sessions, inscriptions, covoiturage, dépenses, QR codes, authentification
4 tables DB : Users, Sessions, Expenses, Session QR Codes
Contextes React : Authentification, notifications
