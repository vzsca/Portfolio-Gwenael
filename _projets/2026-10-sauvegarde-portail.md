---
title: "Sauvegarde du portail de l'auto-école"
date: 2026-10-14
cadre: "Atelier de professionnalisation"
type: "ecole"
resume: "Mise en place d'une sauvegarde quotidienne du site et de sa base, avec un test de restauration."
competences: [c1, c5]
---

## Contexte

Dans le cadre d'une mission sur le portail d'une auto-école, il fallait mettre en place une sauvegarde de la base de données afin de conserver des copies récentes du service et disposer d'une solution de restauration.

## Conditions et moyens

Travail réalisé dans le cadre de la formation BTS SIO. Le projet utilise un serveur Linux avec Nginx, PHP et une base SQLite. Un script Bash est utilisé pour automatiser la sauvegarde de la base de l'auto-école.

## Description de l'activité

1. Création du dossier de sauvegarde `/var/backups/permis`.
2. Utilisation de SQLite pour effectuer une copie de la base `permis.db` avec la commande `.backup`.
3. Compression de la copie avec `gzip` afin de conserver des fichiers de sauvegarde moins volumineux.
4. Conservation des sauvegardes récentes et suppression des anciennes copies avec `find`.
5. Affichage de la date et du nom de la sauvegarde réalisée afin de pouvoir vérifier l'exécution du script.

Le script utilise une copie SQLite dédiée afin d'éviter de copier directement une base pendant qu'elle est modifiée.

## Productions et preuves

- Le script Bash de sauvegarde `sauvegarde.sh`.
- La base SQLite du portail de l'auto-école.
- Les fichiers de sauvegarde compressés produits par le script.
- La configuration du serveur et l'organisation du projet.

### Script de sauvegarde

    #!/bin/bash
    set -e
    horodatage=$(date +%Y-%m-%d)
    dossier=/var/backups/permis
    mkdir -p "$dossier"

    sqlite3 /var/www/permis/data/permis.db ".backup '$dossier/permis-$horodatage.db'"
    gzip -f "$dossier/permis-$horodatage.db"

    find "$dossier" -name 'permis-*.db.gz' -mtime +7 -delete
    echo "$(date +%FT%T) sauvegarde faite : permis-$horodatage.db.gz"

## Ce que j'en retiens

Cette activité m'a permis de comprendre comment automatiser la sauvegarde d'une base SQLite sur un serveur Linux. J'ai également vu l'intérêt de conserver plusieurs sauvegardes datées et de supprimer automatiquement les anciennes afin de limiter l'espace utilisé.
