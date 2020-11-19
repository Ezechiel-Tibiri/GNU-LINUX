## 1. Les commandes de base de LINUX
### 1.1. Les commandes de gestion des répertoires et des fichiers
* `pwd` (affiche le chemin absolu du répertoire courant)
* `ls` (list, affiche les répertoires et les fichiers du répertoire actif)
* `ls` (affiche seulement les noms)
* `ls toto*` (affiche les fichiers commençant par toto)
* `ls -l` (affiche le format long : types + droits + Nbre de liens + ....)
* `cd` (change directory)
* `cp` chemin (vers le répertoire dont le chemin absolu est donné)
* `cd ..` (répertoire parent)
* `cd ~` (répertoire de base)
* `cd -` (répertoire précedent)
* `cd /` (répertoire racine)
* `cp` (copie)
* `cp` rapport*.txt sauvegarde
* `cp *` dossier (copie
* `mv` (move, renomme et déplace un fichier)
* `mv` source destination
* `mv *` dossier (déplace tous les fichiers du répertoire actif vers le répertoire
dossier)
* `mkdir` (créer un répertoire)
* `mkdir` répertoire
* `rmdir` (effacer un répertoire)
* `rmdir` dossier (supprime un répertoire vide)
* `rm` (remove, éfface!!!)
* `rm -R` (enlèvement récursif!!!)
* `rm` fichier
* `rm -i` fichier (interactivement, avec demande de confirmation)
* `rm -f` fichier (avec force, sans demande de confirmation)
* `rm -r` fichier (avec récursivité, avec les sous répertoires)
* `rm -rf` dossier (supprime le répertoire et tou son contenu, sans confirmation)

### 1.2. Les commandes d'édition
* `more` ("pager" qui affiche page par page sans retour en arrière, "h" affiche
l'aide contextuelle)
* `more nom_du_fichier`
* `more *.txt`
* `cat` (concatenate avec le code de fin de fichier eof=CTRL + D)
* `cat fichier-un fichier-deux > fichier-un-deux`
* `cat -n fichier > fichier-numéroté` (crée un fichier dont les lignes sont
numérotés)
* `cat -nb fichier` (affiche sur la sortie standard des lignes numéroté, sauf les
* lignes vides)
* `less`(affiche page par page avec défilement arrière, "h" affiche l'aide contextuelle)
* `less fichier`
* `head` (affiche les 10 premières lignes d'un fichier)
* `head -n22 nom_fichier` (affiche les 22 premières lignes)
* `tail` (affiche les 10 dernières lignes d'un fichier, pour surveiller les fichiers journaux en temps réel)
* `tail -n22 fichier` (affiche les 22 dernières lignes)
* `tail -v fichier` ("verbose", affiche le nom du fichier)
* `touch` (crée un fichier ou actualise la date de dernière modification)
* `gedit /chemin/fichier ` (la commande [**gedit**](https://help.gnome.org/users/gedit/stable/index.html.fr) edite un fichier de manière graphique)
* `vi` ([l'éditeur en mode texte universel](https://github.com/Ezechiel-Tibiri/GNU-LINUX/blob/main/Cours-vi-Ouaga-2019.pdf))
* `emacs` (l'éditeur [GNU Emacs multi fonction pour](https://doc.ubuntu-fr.org/emacs) l'édition, les mails, les news,
la programmation, la gestion des fichiers,...)
* `xemacs` (l'[éditeur GNU Emacs sous X](https://www.xemacs.org/))
* `diff` (différence entre deux fichiers, utiles pour chercher les modifications)
* `diff fishier1 fichier2`
* `sed` (stream editor)
* `sed '/mot/d' fichier > nouveaufichier`
* `awk`

### 1.3. Les autres commandes

* `cal` (calendar)
* `cal` 2002
* `date` (affiche la date, le mois, l'heure et l'année du jour. Les messages d'erreur et les e-mails sont toujours datés avec la date système)
* `date -u`
* `wc` ("word & count", affiche le nombre de lignes + mots + caractères)
* `who | wc -l` (affiche uniquement le nombre de lignes)
* `spell` (programme de correction orthographique)
* `cat rapport.txt | spell > faute.txt`
* `read` (lit dans un script shell la ligne saisie à partir de l'entrée par défaut, le clavier)

## 2. Quelques commandes de l'administrateur
### 2.1. Les commandes de gestion des utilisateurs
* `w`(affiche les informations de connexion de l'utilisateur)
* `who`(affiche la liste des utilisateurs connectés)
* `whoami`(indique le "logon" de l'utilisateur)
* `id` (identité de l'utilisateur actif, UID, GID)
* `finger` (affiche des informations sur les utilisateurs)
* `adduser` (ajouter un compte utilisateur, les UID des utilisateurs commencent à partir du numéro 500)
* `useradd` (ajouter un compte utilisateur)
* `userdel` (supprimer un compte utilisateur)
* `usermod` (modifier les informations d'un compte utilisateur)

### 2.2. Modification des droits d'accès
* Les droits des fichiers d'un répertoire peuvent être affichés par la commande `ls -l`
* Les droits d'accès apparaissent alors comme une liste de 10 symboles. 
```
drwxr-xr-x
```
Le premier symbole peut être « - », « d », soit « l », entres autres (toutes les options sur la page permissions Unix sur wikipédia)). Il indique la nature du fichier :

* - : fichier classique
* d : répertoire
* l : lien symbolique

Il se traduit de la manière suivante :

* **d** : c'est un répertoire.
* **rwx** pour le 1er groupe de 3 symboles : son propriétaire peut lire, écrire et exécuter.
* **r-x** pour le 2e groupe de 3 symboles : le groupe peut uniquement lire et exécuter le fichier, sans pouvoir le modifier.
* **r-x** pour le 3ème groupe de 3 symboles : le reste du monde peut uniquement lire et exécuter le fichier, sans pouvoir le modifier.
`chmod`
* Signification : *change mode*

### 2.3. Quelques commande système
```
sudo
```
* Signification : *substitute user do*
Permet d'exécuter des commandes en tant qu'un autre utilisateur, donc avec d'autres privilèges que les siens.
      Options les plus fréquentes :
              * `-s` : Importe les variables d'environnement du shell
              * `-k` : Lorsque l'on utilise sudo, il garde en mémoire le mot de passe ; cette option déconnecte l'utilisateur et forcera à redemander un mot de passe si sudo est exécuté avant le timeout défini.
```              
 apt-get
```
* Signification : *avanced package tool - get*

Permet l'​installation et la désinstallation ​de paquets ​en tenant compte des dépendances ainsi que le téléchargement des paquets ​s'ils sont sur une source réseau.
Commandes les plus fréquentes :
 * **update** : Met à jour la liste des paquets disponibles en fonction des sources fournies.
 * **upgrade** : Met à jour tous les paquets déjà installés.
 * **dist-upgrade** : Pareil à upgrade mais permet en plus de passer à une version supérieure du noyau et de certains paquets, sans changer de version d'ubuntu.
 * **install** : Installe un ou plusieurs paquets.
 * **remove** : Supprime un ou plusieurs paquets.
 * **clean** : Efface du système les installateurs, sans désinstaller de paquets.

Options les plus fréquentes :
* `-f` (Utilisée avec install ou remove cette option permet de réparer un système dont les dépendances sont défectueuses).
* `-m`  (Ignore les paquets manquants (à éviter si on ne sait pas exactement ce que l'on fait).
* `-s ` (Fait une simulation des actions à mener sans rien toucher au système).
* `-y ` (Répond automatiquement oui à toutes les questions).
* `-u ` (Affiche les paquets mis à jour).
* `--purge`  (À utiliser conjointement avec remove pour supprimer tout ce qui peut l'​être fichiers de configuration par exemple, sauf ceux éventuellement présents dans **/home**).
* `--reinstall`  (Réinstaller les paquets avec leur version plus récente).
              
Exemples d'utilisation :
* `sudo apt-get update` (Met à jour la liste des paquets disponibles).
* `sudo apt-get upgrade` (Met à jour tous les paquets ​installés).
* `sudo apt-get install nom_paquet` (pour installer un paquets) 
              
## 3. Les opérateurs de redirection des Entrées/Sorties

La redirection de la sortie standard (l'écran) vers un fichier permet de consulter le résultat ultérieurement et de le conserver. La redirection de l'entrée standard (le clavier) est moins usitée .La redirection entre processus  (entre commande ou entre programme avec le tube ou le pipe) permet de créer des "pipelines", c'est à dire une seule ligne de commande constituée d'une succession de commandes avec la sortie de chacune redirigée vers l'entrée de la suivante.

* `|`(pipe **AltGr+6**)
* `commande1 | commande2`
* `ls | cat`
* `cat fichier | lp`
* `>` (redirection de la sortie standard, le fichier de destination écrase le précédent)
* `commande > sortie`
* `ls > fichier`
* `commande 2> erreurs.txt` (redirige les erreurs de syntaxe, le flux "stden" vers un fichier)
* `commande < entrée> sortie`
* `<`(redirection de l'entré standard)
* `commande < fichier d'entrée`
* `>>`(redirection et concaténation en fin de fichier)
* `cat fichier1 fichier2 >> ensemble`

## 4. Les commandes d'archivage et de compression
* `tar`(tape archive ressource, pour archiver ou restaurer des "tar file" avec l'extension "**.tar**")
* `tar -cvf cible source` (archive la "source" dans la "cible")
* `tar -xvf archive.tar` (restaure le fichier "archive.tar" dans le répertoire courant)
* `tar -xvf archive.tar /tmp` (restaure le fichier "archive.tar" dans le répertoire "**/tmp**")
* `tar -xvof archive.tar`
* `compress` (compression de fichiers en un seul avec l'extension "**.Z**")
`compress fichier`
* `compress -v fichier`
* `compress fichier.tar` (compression en un fichier avec l'extension **"tar.Z"**)
* `uncompress`(décompression ou restauration des fichiers compressés avec l'extension "**.Z**")
* `uncompress fichier.Z`
* `uncompress fichier.tar.Z`
* `uncompress un.Z deux.Z`
* `gzip` (programme de compression GNU qui forme des fichiers compressés avec l'extension "**.gz**")
* `gunzip` (programme de décompression GNU (g "unzip")des fichiers compressés avec l'extension "**.gz**")
* `gunzip fichier.gz`
* `zcat`
* `zcat fichier.gz | more` (pour décompresser un fichier "**.gz**" et l'afficher sur la sortie standard (l'écran))
* `zgrep`
* `zgrep "disk" /répertoire/*.gz` (recherche le terme "**disk**" à l'intérieur de plusieurs fichiers compressés)

## 5. Les programmes de connexion distante
`ssh` ("secure shell")
### Exercice 1: Se connecter à un serveur Linux avec ```ssh```
* 1. Dans le shell taper
```
ssh formationX@@master.univ-ouaga.bf
```
* X = [1-15]

Dans le champ, entrer le mot de passe `formationX` quand il est demandé

## 6. Création et gestion d'un script bash {: .red #red-h}
      
### 6.1. Création de script
* La création d'un script bash n'est pas très compliquée. Il suffit de créer un fichier vierge, de lui donner un nom, de l'ouvrir par un double-clic et enfin d'écrire la ligne suivante comme première ligne de ce fichier.
* sheband (prémière ligne de script)

```
#!/bin/bash
```
* Remarque : il n'est pas nécessaire d'indiquer une extension pour le nom du fichier, la première ligne du fichier est suffisante pour que le système Linux reconnaisse qu'il s'agit d'un script bash.

### 6.2. Édition d'un script

* On peut éditer le fichier qui contient un script en ligne de commande à l'aide d'une des lignes de commande suivantes :

```
gedit nom_du_script
nano nom_du_script
```
### 6.3. Lancement d'un script

* Pour lancer un script, le mieux est de le faire avec une console.

Avant de lancer le script, il est nécessaire de modifier les permissions le concernant et de le rendre exécutable. Cela se fait avec la ligne de commande suivante, si l'on est dans le répertoire contenant le script (sinon, il faudra indiquer le chemin complet du fichier, du style /home/répertoire_utilisateur/chemin/nom_du_script) :

```
chmod u+x nom_du_script
```

Une fois les permissions ainsi modifiées, le lancement d'un script se fait, par exemple, à l'aide de la ligne de commande suivante, si l'on est dans le répertoire contenant le script :

```
bash nom_du_script
```

# Documentation 
Voici quelques sites pour plus de détails sur la programmation Bash :
* [Les scripts bash](http://www.unixmaniax.fr/wiki/index.php?title=Les_scripts_bash)
* [Documentation pour débutant](https://guidespratiques.traduc.org/guides/vf/Bash-Beginners-Guide/Bash-Beginners-Guide.html)
* [encore plus de la documentation](https://abs.traduc.org/abs-fr/)

Et sur des commandes utiles 

* [Les commandes Bash](http://www.unixmaniax.fr/wiki/index.php?title=Bash_-_les_commandes)
* [Commandes partie 1](http://www.softndesign.org/manuels/unix-1.html)
* [Commandes partie 2](http://www.softndesign.org/manuels/unix-2.html)
* [Commandes partie 3](http://www.softndesign.org/manuels/unix-3.html)

## TP
* [TP1](https://github.com/Ezechiel-Tibiri/GNU-LINUX/blob/main/exo.zip)
* [TP2](https://github.com/Ezechiel-Tibiri/GNU-LINUX/blob/main/TP1.zip)
* [TP3](https://github.com/Ezechiel-Tibiri/GNU-LINUX/blob/main/TP3.zip)
