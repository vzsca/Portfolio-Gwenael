---
title: "Coffre de mots de passe pour une agence immobilière"
date: 2026-11-06
cadre: "Atelier de professionnalisation — Sujet 04"
type: "ecole"
resume: "Déploiement local de Vaultwarden avec Docker et Caddy, organisation des accès par collections, gestion des permissions et révocation d'un membre."
competences: [c5]
---

## Contexte

Dans le cadre du BTS SIO, j'ai réalisé une maquette de coffre de mots de passe pour une agence immobilière fictive. Le besoin était de remplacer le partage informel d'identifiants par un espace centralisé, de limiter l'accès aux informations selon le rôle des employés et de pouvoir retirer les droits d'un salarié lors de son départ.

## Conditions et moyens

- **Système :** Windows 11 avec Docker Desktop et moteur WSL 2.
- **Conteneurs :** Vaultwarden et Caddy, orchestrés avec Docker Compose.
- **Accès local :** HTTPS sur `https://vault.lan`, avec certificat généré par l'autorité interne de Caddy.
- **Stockage :** dossier local `vw-data/` pour les données du coffre.
- **Documentation :** recommandations ANSSI et vérifications Have I Been Pwned.
- **Dépôt :** [GitHub — vzsca/keepass](https://github.com/vzsca/keepass).

## Description de l'activité

1. J'ai préparé un environnement Docker local sur Windows et créé les fichiers de configuration Compose et Caddy.
2. J'ai déployé Vaultwarden derrière Caddy afin de rendre le coffre accessible en HTTPS sur le nom local `vault.lan`.
3. J'ai configuré le stockage persistant des données du coffre et protégé l'accès à l'administration avec un jeton dont le condensat est conservé dans un fichier local non versionné.
4. J'ai créé l'organisation `Agence` et les collections `Direction` et `Négociateurs`.
5. J'ai invité un compte négociateur et attribué les droits de modification des éléments de la collection `Négociateurs`, sans lui attribuer la gestion de la collection.
6. J'ai testé le retrait de l'accès du membre depuis l'organisation.
7. J'ai rédigé une politique de mots de passe en m'appuyant sur le guide ANSSI et consigné cinq recherches HIBP qui n'ont signalé aucune fuite connue.
8. J'ai documenté les procédures d'installation, de sauvegarde, de restauration et de départ d'un salarié dans le dépôt GitHub.

## Productions et preuves

- [Dépôt GitHub et livrables](https://github.com/vzsca/keepass).
- Fichiers Docker Compose et Caddy sans secret.
- Procédure d'installation et de configuration HTTPS.
- Documentation de sauvegarde et de restauration.
- Tableau de tests des accès et des collections.
- Procédure de départ d'un salarié.
- Politique de mots de passe et compte rendu des recherches HIBP.

## État des validations et limites

Le déploiement HTTPS, la création de l'organisation et des collections, l'attribution des droits au négociateur et le test de révocation ont été réalisés.

Certains livrables restent à compléter avant de considérer le sujet entièrement terminé : création et classement des dix identifiants fictifs, renouvellement des six secrets après le départ, test réel de restauration de la sauvegarde et ajout des captures d'écran. Ces points sont suivis dans le dépôt.

La maquette est accessible uniquement depuis le poste hôte. Vaultwarden est une implémentation communautaire compatible avec les clients Bitwarden ; ce projet est une démonstration pédagogique locale et non un déploiement de production.

## Ce que j'en retiens

Ce projet m'a permis de mettre à disposition un service informatique conteneurisé, de configurer un accès HTTPS local et de gérer des droits d'accès à des ressources partagées. J'ai également travaillé sur les procédures de retrait d'un utilisateur, la protection des secrets et la formalisation de règles de sécurité.

Cette réalisation contribue à la compétence **C5 — Mettre à disposition des utilisateurs un service informatique**.
