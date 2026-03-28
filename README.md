# Conception et mise en œuvre System Call Monitor, un moniteur d’appels systèmes temps réel: cas Linux Mint


# Objectifs:

1. Comprendre ce qu’est un appel système et son rôle dans l’architecture OS.
   
2. Utiliser des outils bas niveau pour tracer l’activité système.


# Fonctionnalités attendues
Développer un Dashboard web qui : identifie les appels systèmes, les classe par catégorie (fichier, réseau, processus, mémoire, etc.), et les présente de manière conviviale (statistiques, graphiques…).
Mint System Call Monitor 🛡️

Projet de Surveillance des Appels Systèmes en Temps Réel Master 1 en Sécurité des Systèmes d’Information

📝 Présentation du Projet

Ce projet consiste en la conception et la mise en œuvre d'une solution de surveillance des appels systèmes (syscalls) sur Linux Mint. Grâce à la puissance de l'outil eBPF (Extended Berkeley Packet Filter), nous capturons l'activité du noyau (kernel) pour l'analyser et la visualiser via un Dashboard web convivial.

L'objectif est d'offrir une visibilité précise sur les actions exécutées par les applications au niveau du système d'exploitation, facilitant ainsi l'audit de sécurité et l'analyse de stabilité.

Objectifs

Comprendre le rôle des appels systèmes dans l'architecture d'un OS.

Tracer l'activité système avec des outils bas-niveau (eBPF, BCC).

Classifier les appels par catégories (Processus, Mémoire, Réseau, Fichiers).

Visualiser les statistiques en temps réel sur une interface web moderne.

Architecture Technique

Le projet suit une architecture modulaire basée sur le modèle MVC :

Capture (Kernel) : Utilisation de programmes C injectés via eBPF.

Backend : Serveur Python (Flask + SocketIO) pour le traitement des données.

Frontend : Dashboard Web dynamique (HTML5, TailwindCSS, Socket.io).

Modélisation (UML)

Le projet a été conçu selon la méthode 2TUP :

Acteurs : Utilisateur, eBPF, Kernel Linux.

Cas d'utilisation : Authentification, Consultation du Dashboard, Visualisation des statistiques, Capture et Classification des appels.

Installation & Déploiement

Prérequis

Système : Linux Mint (Noyau LTS compatible eBPF)

Outils : python3, pip3, bcc-tools, linux-headers

Installation des dépendances

sudo apt update
sudo apt install -y python3-bpfcc bpfcc-tools linux-headers-$(uname -r)
pip3 install flask flask-socketio


Lancement du Monitor

# Se déplacer dans le dossier du projet
cd MintMonitorApp

# Lancer l'application avec les privilèges root (nécessaire pour eBPF)
sudo python3 app.py


Accédez ensuite à l'interface via : http://localhost:5000

Intervenants

Maitre d’ouvrage : M. NGUIMBUS Emmanuel (Professeur SE)

Maitres d’œuvre : - Mme. NDIOMO MBAZOA Jacinta

M. LONDJI Jean Christian

État d'avancement

[x] Analyse & Cahier des charges

[x] Conception & Modélisation UML

[x] Développement du moteur de capture eBPF

[x] Développement du Dashboard Web

[ ] Déploiement final (Février 2026)

Projet réalisé dans le cadre du Master 1 SSI.

# NB: README complet et fini
