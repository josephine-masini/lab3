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
 
 15. On fait ```/gravelly ``` + ```Enter``` et ```dw``` pour enlever un mot + ```Enter```.
 
 16. ```:w```, pour sauvegarder un fichier sans le fermer, puis ```Enter```.
 
 17. ```/planet``` + ``` Enter``` et ```n```, le nombre de fois que le mot est repéré de nouveau en allant vers le bas du texte.
 
 19. On fait : ```G```, pour aller à la fin du fichier et on tape ```?BEEP```, pour trouver la dernière occurence du mot BEEP, puis on tape : ```n``` pour remonter vers le haut et cette fois-ci trouver les occurences précédentes du mot.
 
 20. Pour afficher les 20 dernières lignes d'un fichier : ``` tail -n 20 sardar3.txt ``` .
  
 21. Pour chercher le mot trust dans Microsoft :``` josephine@masini-x220:~/Bureau/lab3/5AS05-partie3$ grep -w "trust" Microsoft```
 ```University: "It's not that we don't trust the research, it's just that anti-trust laws.```

22. Pour chercher money dans tous les fichiers du répertoire : on écrit ```grep -R "money"```  ```5AS05-partie3/Microsoft:    2.$$ key--When this key is pressed, money is transferred```
```
5AS05-partie3/answering-machine.txt:	If you need any money, or if you just want to check out my
5AS05-partie3/answering-machine.txt:	the money.  If you are my parents, please send money.  If you
5AS05-partie3/answering-machine.txt:	money.  If you are my friends, you owe me money.  If you are a
5AS05-partie3/answering-machine.txt:	female, don't worry, I have plenty of money.```
5AS05-partie3/answering-machine.txt:	the money.  I'll get back to you as soon as it's safe for you to
5AS05-partie3/sardar/sardar3.txt:Santa Singh needed some money desperately.```
5AS05-partie3/sardar/sardar3.txt:Sikh will never accept the money. So he drops a 100 rupee note, from
5AS05-partie3/sardar/sardar3.txt:day for money. Now the priest is really annoyed with Santa. The Priest
5AS05-partie3/sardar/sardar3.txt:decides that he is not going to give any more money to```
5AS05-partie3/sardar/sardar3.txt:money.
5AS05-partie3/sardar/sardar3.txt:eyes and does not find any money. He slowly raises his head and now
5AS05-partie3/sardar/sardar3.txt:p.s. i was going to send you some money, but the
5AS05-partie3/sardar/sardar1.txt:LoveMom. P.S. I was going to send you some money but the envelope was
```

23. On utilise la flèche du haut pour réécrire automatiquement la commande précédente en remplacant le mot "money" par "Money". On affiche ensuite la liste de la même manière qu'à la question 22.

24. On se place dans le répertoire ```AS05-partie3```, et on tape : ```mv .lightbulb lightbulb```, afin que le fichier caché devienne apparent. Et on le voit à présent dans le répertoire :
```
josephine@masini-x220:~/Bureau/lab3/5AS05-partie3$ ls
 answering-machine.txt   lightbulb   sardar
'Compte rendu lab3.md'   README.md   sardar3.txt
```

25. On fait un ```cd sardar```, pour rentrer dans le répertoire, puis on tape ```pwd```, pour afficher le répertoire dans lequel on se trouve. On obtient :
```
josephine@masini-x220:~/Bureau/lab3/5AS05-partie3/sardar$ pwd
/home/panda/Bureau/lab3/5AS05-partie3/sardar
```
Nous sommes bien dans le répertoire sardar.

26. Pour déplacer un fichier on fait : ```mv sardar3.txt ..```, qui va le placer dans le répertoire précédent, fait ```cd ..```, afin de vérifier qu'il a bien été déplacé. On obtient : ( les questions précédentes ont déjà été faites au moment de la capture, on a donc le fichier Microsoft de supprimé ).
```
josephine@masini-x220:~/Bureau/lab3/5AS05-partie3$ ls
 answering-machine.txt   lightbulb   sardar
'Compte rendu lab3.md'   README.md   sardar3.txt

```
Le fichier a bien été déplacé dans le répertoire parent.

27. Déjà fait à la question précédente avec ```cd ..```.

28. On tape ```rm Microsoft``` et on fait ```ls``` dans le répertoire courant pour vérifier qu'il a été supprimé :
```
answering-machine.txt   lightbulb   sardar
'Compte rendu lab3.md'   README.md   sardar3.txt
```
Le fichier a bien été supprimé.

29. On retourne sur le répertoire parent du répertoire courant ```cd ..```, on crée le répertoire archive : ```mkdir archive```, et on copie le répertoire :
```
cp 5AS05-partie3/* /archive

```
30. On tape : ```ln -s sardar/* .```, pour créer un lien symbolique entre le répertoire courant et le répertoire sardar, lui même dans ce répertoire courant.

31. Oui, le répertoire d'origine du fichier est noté, le fichier est en gras d'une couleur différente des autres, on voit bien que c'est un fichier différent.
```
ls -l

total 176
-rw-r--r-- 1 josephine panda 70314 oct.   7 10:28  answering-machine.txt
-rw-r--r-- 1 josephine panda  4124 oct.   7 10:28 'Compte rendu lab3.md'
-rw-r--r-- 1 josephine panda    41 oct.   7 10:28  lightbulb
-rw-r--r-- 1 josephine panda    24 oct.   7 10:28  README.md
drwxr-xr-x 2 josephine panda  4096 nov.   1 20:15  sardar
lrwxrwxrwx 1 josephine panda    18 nov.   8 20:18  sardar1.txt -> sardar/sardar1.txt
lrwxrwxrwx 1 josephine panda    18 nov.   8 20:18  sardar2.txt -> sardar/sardar2.txt
-rw-r--r-- 1 josephine panda 81994 oct.   7 10:28  sardar3.txt

```
32. On écrit ```rm sardar/sardar2.txt``` et on refait ```ls -l```, le nom du fichier s'affichhe de la même facon mais en rouge, pour signaler qu'il a été supprimé, mais le lien existe toujours.





