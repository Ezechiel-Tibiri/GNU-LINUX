# GNU-LINUX
Administration niveau 1
## Introduction
Les commandes LINUX sont pratiquement les même que sous UNIX (il existe des variantes notamment pour les options, et il convient de consulter l'aide en ligne pour connaître les spécifications de son système et de son shell de connexion). Le shell de connexion est un programme qui sert d'interface entre le noyau et l'utilisateur. C'est le shell qui est à l'écoute des commandes que peut saisir l'utilisateur. Le shell présente l'invite de commandes dès la connexion du compte de l'utilisateur en mode texte (run level 3 du fichier "/etc/inittab"). En mode graphique , l'utilisateur peut ouvrir un terminal avec les touches CTRL + ALT + F1 à F6 et F7 pour revenir au mode graphique, l'utilisateur peut également lancer une console virtuelle (une fenêtre de terminal) tout en restant à l'intérieur de l'interface graphique.

## Installation
https://www.clubic.com/tutoriels/article-864991-1-comment-installer-ubuntu.html

## Architecture de LINUX
Le système d'exploitation Linux n’est pas un bloc monolithique fixé une fois pour toutes. En réalité, de nombreuses composantes travaillent ensemble, rédigés par des personnes différentes et assemblés en distributions. Ce n’est que vu de l’extérieur que le noyau de Linux semble être une unité indissociable. Les distributions ont néanmoins toutes le même noyau du système d’exploitation, et de nombreuses applications communes.
### Le noyau
Est la partie du code en mémoire. Le noyau s’occupe de la : 

#### Gestion de la mémoire 

La mémoire physique est étendu virtuellement. Les programmes ou les sections de programmes inutilisés sont déchargés vers le disque dur et chargés en mémoire vive  lorsque l’exécution l’exige. 

#### Gestion des fichiers 

Linux possède un système hiérarchisé de fichiers dont la structure interne peut varier. Des espaces disques d’autres systèmes peuvent être montés. 

#### Gestions des périphériques 

L’accès aux périphériques se fait par l’entremise de fichiers qui constituent l’interface entre les pilotes de périphériques et le noyau. 

#### Gestion des programmes et des processus 

Linux assure que chaque programme fonctionne en toute indépendance. 

#### Gestion des droits d’accès 

Les données enregistrées dans le système de fichiers doivent être protégées contre les accès non autorisés. 

### Le shell 

Le shell est la liaison la plus élémentaire entre vous, l’utilisateur, et le système d’exploitation. Vous tapez les commandes qui seront interprétées par le shell et transmises au système d’exploitation. Il existe plusieurs versions de shell : 

#### bash 

C’est le shell standard de Linux le Bourne Again Shell 

#### sh 

Le shell original le Bourne shell 

#### csh 

Le C shell utilise une interface de programmation différente de bash 

#### ksh 

Le Korn shell est un des plus populaire sous Unix. Il est compatible avec bash 

#### tcsh 

Le C shell amélioré 

#### zsh 

Le Z shell est compatible avec bash 

[Commandes LINUX](https://github.com/Ezechiel-Tibiri/GNU-LINUX/blob/main/cmd_linux.md)
