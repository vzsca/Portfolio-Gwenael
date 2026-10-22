---
title: "HomeLab — Serveur personnel"
date: 2026-10-23
cadre: "Projet personnel"
type: "perso"
resume: "Administration d'un serveur personnel Linux avec Docker, accès distant privé via NetBird, DNS avec AdGuard Home et mise en place du HTTPS avec Caddy."
competences: [c1, c5]
---

## Contexte

J'utilise un ancien ordinateur comme serveur personnel afin de pratiquer l'administration Linux, les réseaux et le déploiement de services auto-hébergés. Le HomeLab me sert également d'environnement d'expérimentation pour mes projets personnels, dont v-bot.

## Conditions et moyens

Le serveur dispose de 8 Go de RAM et d'un processeur Intel Pentium N6000. L'environnement repose sur Linux, Docker et des services organisés dans des répertoires dédiés sous `/srv/docker` et `/opt`. NetBird fournit un accès distant privé au serveur.

## Description de l'activité

1. Installation et administration d'un serveur Linux sur une ancienne machine.
2. Configuration de l'accès SSH et du réseau pour administrer le serveur à distance.
3. Mise en place de NetBird pour l'accès privé aux services et à la machine.
4. Déploiement et gestion de services conteneurisés avec Docker.
5. Configuration d'AdGuard Home pour les fonctions de filtrage DNS et de gestion DNS locale.
6. Mise en place de Caddy comme serveur web / reverse proxy, avec travail sur l'accès HTTPS aux services.
7. Organisation des fichiers de configuration et des volumes persistants pour séparer les données des conteneurs.
8. Préparation du serveur pour héberger des services personnels et des outils de développement.

## Productions et preuves

- Serveur Linux accessible à distance par SSH.
- Services Docker organisés dans une arborescence dédiée.
- Accès distant privé géré par NetBird.
- Déploiement d'AdGuard Home pour le DNS.
- Configuration de Caddy pour le reverse proxy et le HTTPS.
- Fichiers de configuration et volumes persistants des services.

## Sécurité et maintenance

Les services sont isolés en conteneurs lorsque c'est adapté. Les accès distants sont organisés autour du réseau privé NetBird ; les configurations et données persistantes sont séparées des conteneurs afin de faciliter leur maintenance. Les secrets et fichiers d'environnement ne doivent pas être publiés dans le dépôt.

## Ce que j'en retiens

Ce projet me permet de pratiquer l'administration d'un système Linux réel, la conteneurisation, la gestion de services réseau et l'accès distant sécurisé. Il me fait aussi travailler sur la maintenance, l'organisation des configurations et le diagnostic des problèmes de connectivité et de HTTPS.
