# Compte rendu - lab3
# Josephine MASINI

--------------------

1. On clique sur vmware pour l' ouvrir et fait play.

2. Pour démarrer la console, on va dans Activities, et on tape "term" dans la barre de recherche.

3. On fait cd home/student/Desktop et on crée un répertoire avec ```mkdir lab3```. Ensuite on fait cd lab3 et on clone le répertoire git du TP :
```git clone https://github.com/khachicha/5AS05-partie3.git```

4. On vérifie et on fait ls dans lab3, puis cd 5AS05-partie3, puis ```ls -lrth```. La taille du répertoire est de 116K octets, il est composé de 4 fichiers : un .txt, un .md, un sans extension et un répertoire sardar.

```
tota 116K
-rw-r--r-- 1 josephine panda   24 oct.   6 10:58 README.md
-rw-r--r-- 1 josephine panda  34K oct.   6 10:58 Microsoft
drwxr-xr-x 2 josephine panda 4,0K oct.   6 10:58 sardar
-rw-r--r-- 1 josephine panda  69K oct.   6 10:58 answering-machine.txt

``` 
5. On fait cd sardar, puis ls -lrth :

```
total 108K
-rw-r--r-- 1 josephine panda  81K oct.   6 10:58 sardar3.txt
-rw-r--r-- 1 josephine panda 5,9K oct.   6 10:58 sardar2.txt
-rw-r--r-- 1 josephine panda  14K oct.   6 10:58 sardar1.txt

```
On remarque la taille est différente, elle est de 4,0K octets dans le premier cas et de 108K octets dans le 2ème cas. 4,0K octets doit être la taille du fichier directeur, et non de son contenu qui lui est de de 108K octets. Le répertoire contient en effet 3 fichiers .txt.

6. La taille du fichier Microsoft est de 34K octects (34 359) avec ```ls Microsoft```. Avec ```du -sh Microsoft```, elle est de 36K octets, ce qui correspond à la taille que prend réellement le fichier dans le disque dur. La taille mesurée par ```ls -lrth```, ne prend pas en compte l'inode du fichier qui indique son emplacement dans le système de fichiers et ce qu'il y a dedans.

7. En tapant la commande : ```stat Microsoft```, on obtient les informations suivantes :

```
 Fichier : Microsoft
   Taille : 34359     	Blocs : 72         Blocs d'E/S : 4096   fichier
Périphérique : 802h/2050d	Inœud : 1444365     Liens : 1
Accès : (0644/-rw-r--r--)  UID : ( 1000/josephine)   GID : ( 1000/   panda)
Accès : 2020-10-06 10:58:57.479477390 +0200
Modif. : 2020-10-06 10:58:57.479477390 +0200
Changt : 2020-10-06 10:58:57.479477390 +0200
  Créé : -

```
On 72 blocs de 4096 octets, le Inoeud est le numéro d'identification, le reste nous donne des informations sur les droits d'accès et autres méta-données.

8. On retourne dans le répertoire avec ``` cd ..``` et ```cd 5AS05-partie3``` , on tape la conmmande ```ls.*``` et on a 2 types de fichiers cachés : un .lightbulb et un .git.

9. On fait un ```ls -t```, qui nous classe les fichiers du plus récent au plus ancien et on fait ```ls -r``` pour inverser cet ordre et afficher les fichiers du plus ancien au plus récent. On peut également faire plus simple en tapant : ``` ls -tr ```.

```
README.md  Microsoft  sardar  answering-machine.txt

```

10. Pour les classer par taille, ```ls -s```, qui place les plus gros en premier, puis ```ls -r```, pour inverser cet ordre, ou directement ```ls -sr```, qui les affiche du plus petit au plus gros.
On remarque que sardar est le plus petit avec 4,0K octets, alors que son contenu est plus lourd que tout le reste des autres fichiers, ce qui s'explique à la question 5. Les tailles affichées sont en K octets.

```
 4 sardar   4 README.md  36 Microsoft  72 answering-machine.txt
 
 ```
 11. Pour afficher le contenu d'un fichier texte : ``` cat answering-machine.txt```. Tout le texte s'affiche et défile d'un coup, on se retrouve à la fin.
 
 12. Pour avoir le temps de lire le long texte qui défile : ```more answering-machine.txt```, puis on appuie sur ```Entrer```pour le parcourir en ajoutant chaque ligne à la lecture.
 
 13. On installe vim en faisant ```sudo apt get-install vim```, pour lire le texte on fait : ```vim answering-machine.txt```.
 
 14. On va à la dernière ligne avec la commande ```G``` et on ajoute une ligne à la fin de la dernière écrite avec ```o```, on écrit ensuite : Welcome systemes communicants.
 
 15. 
 
 


