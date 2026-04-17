# Projet-Tutoré
Ce dépôt contient l'ensemble des configurations et scripts utilisés pour le déploiement d'une solution de gestion de parc informatique et de helpdesk basée sur GLPI. Ce projet a été réalisé dans le cadre de ma 3ème année de BUT Réseaux et Télécommunications.

📋 Contexte du projet

L'objectif était de concevoir une infrastructure répondant à un besoin réel d'entreprise (inspiré de la société Dem Dikk) : centraliser la gestion des incidents, le suivi du matériel et améliorer la communication technique.

L'environnement complet a été simulé sur VirtualBox avec :

    Serveur GLPI : Ubuntu 22.04.

    Serveur de Domaine : Windows Server 2022 (Active Directory & Messagerie).

    Poste Client : Windows 11 pour les tests de déploiement d'agents via GPO.

🚀 Fonctionnalités & Choix Techniques

Le projet repose sur une approche DevOps moderne pour garantir la reproductibilité du déploiement.

    Conteneurisation (Docker) : Isolation des services Web (Apache/PHP/GLPI) et de la base de données (MariaDB) pour plus de stabilité.

    Automatisation (Ansible) : Utilisation de playbooks YAML pour l'installation et la configuration automatique de l'ensemble de la pile technique.

    Liaison Active Directory (LDAP) : Synchronisation des utilisateurs et des groupes pour permettre le Single Sign-On (SSO).

    Optimisation du Ticketing :

        Mise en place d'une arborescence de catégories ITIL complète.

        Gestion des niveaux de service avec TTO (4h) et TTR (3j).

        Escalades automatiques en cas de dépassement des délais.

    Gestion Automatisée du Parc :

        Mise en place du module de gestion de parc pour le suivi du matériel.

        Déploiement automatisé de l'agent GLPI sur les postes clients via GPO (Group Policy Objects)

    Sécurité : Accès distant sécurisé via un service OpenVPN avec un router Mikrotik hAP.

📦 Livrables inclus

Pour permettre une revue complète ou une reprise du projet, ce dépôt contient :

    Le Rapport de Projet : Un compte rendu détaillé (PDF) reprenant l'analyse, les choix techniques et les étapes de réalisation.

    Environnement Virtuel (Fichiers .ova) : Les fichiers d'exportation pour les trois machines virtuelles clés du projet (Serveur GLPI Ubuntu, Windows Server 2022 et Poste Client). Ces images permettent de déployer instantanément l'infrastructure complète dans VirtualBox pour tester la solution en conditions réelles.
