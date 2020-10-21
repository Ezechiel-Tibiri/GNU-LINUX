## 1. Les commandes de base de LINUX
### 1.1. Les commandes de gestion des répertoires et des fichiers
`pwd` (affiche le chemin absolu du répertoire courant)
`ls` (list, affiche les répertoires et les fichiers du répertoire actif)
`ls` (affiche seulement les noms)
`ls toto*` (affiche les fichiers commençant par toto)
`ls -l` (affiche le format long : types + droits + Nbre de liens + ....)
`cd` (change directory)
`cp` chemin (vers le répertoire dont le chemin absolu est donné)
`cd ..` (répertoire parent)
`cd ~` (répertoire de base)
`cd -` (répertoire précedent)
`cd /` (répertoire racine)
`cp` (copie)
`cp` rapport*.txt sauvegarde
`cp *` dossier (copie
`mv` (move, renomme et déplace un fichier)
`mv` source destination
`mv *` dossier (déplace tous les fichiers du répertoire actif vers le répertoire
dossier)
`mkdir` (créer un répertoire)
`mkdir` répertoire
`rmdir` (effacer un répertoire)
`rmdir` dossier (supprime un répertoire vide)
`rm` (remove, éfface!!!)
`rm -R` (enlèvement récursif!!!)
`rm` fichier
`rm -i` fichier (interactivement, avec demande de confirmation)
`rm -f` fichier (avec force, sans demande de confirmation)
`rm -r` fichier (avec récursivité, avec les sous répertoires)
`rm -rf` dossier (supprime le répertoire et tou son contenu, sans confirmation)

### 1.2. Les commandes d'édition
`more` ("pager" qui affiche page par page sans retour en arrière, "h" affiche
l'aide contextuelle)
`more nom_du_fichier`
`more *.txt`
`cat` (concatenate avec le code de fin de fichier eof=CTRL + D)
`cat fichier-un fichier-deux > fichier-un-deux`
`cat -n fichier > fichier-numéroté` (crée un fichier dont les lignes sont
numérotés)
`cat -nb fichier` (affiche sur la sortie standard des lignes numéroté, sauf les
lignes vides)
`less`(affiche page par page avec défilement arrière, "h" affiche l'aide contextuelle)
`less fichier`
`head` (affiche les 10 premières lignes d'un fichier)
`head -n22 nom_fichier` (affiche les 22 premières lignes)
`tail` (affiche les 10 dernières lignes d'un fichier, pour surveiller les fichiers journaux en temps réel)
`tail -n22 fichier` (affiche les 22 dernières lignes)
`tail -v fichier` ("verbose", affiche le nom du fichier)
`touch` (crée un fichier ou actualise la date de dernière modification)
`vi` ([l'éditeur en mode texte universel](https://github.com/Ezechiel-Tibiri/GNU-LINUX/blob/main/Cours-vi-Ouaga-2019.pdf))
`emacs` (l'éditeur [GNU Emacs multi fonction pour](https://doc.ubuntu-fr.org/emacs) l'édition, les mails, les news,
la programmation, la gestion des fichiers,...)
`xemacs` (l'[éditeur GNU Emacs sous X](https://www.xemacs.org/))
`diff` (différence entre deux fichiers, utiles pour chercher les modifications)
`diff fishier1 fichier2`
`sed` (stream editor)
`sed '/mot/d' fichier > nouveaufichier`
`awk`

### 1.3. Les autres commandes

`cal` (calendar)
`cal` 2002
`date` (affiche la date, le mois, l'heure et l'année du jour. Les messages d'erreur et les e-mails sont toujours datés avec la date système)
`date -u`
`wc` ("word & count", affiche le nombre de lignes + mots + caractères)
`who | wc -l` (affiche uniquement le nombre de lignes)
`spell` (programme de correction orthographique)
`cat rapport.txt | spell > faute.txt`
`read` (lit dans un script shell la ligne saisie à partir de l'entrée par défaut, le clavier)

## Quelques commandes de l'administrateur

