# Exercice 2
## Manuel

1. Afin d'identifier le role de la commande which, on utilise la commande man which.
2. Pour chercher un terme particulier comme option dans un man on utilise la commande /option.
3. Enfin pour le quitter, on utilise la commande q.
4. Pour afficher la premiere page de la section 6 on utilise la commande man -K 6, cette page affiche le man de dpkg-maintscript-helper

## Navigation dans l'arborescence des fichiers

1. afin d'aller dans le dossier /var/log on utilise la commande cd /var/log.
2. Afin de remonter dans le dossier /var, on utilise la commande cd ..
3. Afin de retourner dans le dossier personnel (dossier User), on a juste a utiliser cd
4. Afin de retourner dans le dossier var sans utiliser de chemin, on utilise la commande cd ../../var
5. On ne peut pas accéder au dossier root sans permission.
6. La commande ne fonctionne pas non plus car la commande cd n'est pas abilité a rentrer dans un dossier root.
7. On utilise pour cela les commandes mkdir (création de dossiers) et touch (création de fichiers).
8. La commande rm permet de supprimer le fichier mais pas le dossier.
9. Pour supprimer le dossier, on utilise la commande rmdir
10. Cette commande ne marche pas sur le /dossier2 car le dossier est rempli.
11. On utilise donc la commande rm -rf /dossier2 afin de le supprimer lui et son contenu.

## Commandes importantes

1. La commande permettant d'afficher l'heure est la commande date. La commande time permet d'afficher le temps d'exécution d'une commande.
2. Les fichiers commençant par un . sont des fichiers invisibles.
3. Le programme ls se situe dans le fichier ls lui même présent dans le dossier bin
4. Il n'existe pas de man pour la commande ll, la commande ll est en fait la commande ls - alF.
5. Pour afficher le contenu du /bin, il faut juste utiliser la commande ls dans ce fichier ou alors utiliser la commande ls /bin
6. La commande ls permet d'afficher le contenu d'un dossier.
7. Afin d'afficher le chemin d'un dossier, on utilise la commande find
8. La commande echo 'bip' > plop permet de créer un fichier plop dont le contenu sera le texte 'bip' la deuxieme exécution de la commande ne change rien.
9. La commande echo 'bip' >> plop permet d'ajouter au fichier blop le texte 'bip'. Apres deux exécution de cette commande il y a donc trois fois le texte 'bip' (il était deja présent un fois grace a la question 8.
10. La commande sleep 10 | echo 'toto' permet d'afficher le texte 'toto' pendant 10 seconde.
11. La commande file permet d'afficher le type du contenu d'un fichier. Dans le cas du fichier plop crée précedement, son contenu est de l'ASCII text.
12. Lorsque l'on modifie le contenu de original, le contenu de lien_phy est aussi modifié. Cependant, lorsque l'on supprime original, lien_phy reste comme précédemment.
13. Lorsque l'on effectue une modification sur l'un des deux fichiers, l'autre est aussi modifié. De plus, lorsque l'on supprime lien_phy, lien_sym n'est pas supprimé mais n'est plus reconnu par l'ordinateur.
14. Afin d'interrompre le défilement, on utilise le raccourci ctrl + s et pour reprendre le défilement, on utilise le raccourci ctrl + q.
15. Pour afficher les 5 premières lignes du fichier syslog, on utilise la commande head-5 syslog. Pour afficher les 15 dernières, on utilise la commande tail -15 syslog. Enfin pour afficher les lignes 10 à 20, on utilise la commande sed -n 10,20p syslog.
16. La commande dmesg | less demande des permissions spécials.
17. Le fichier passwd affiche les utilisateurs de la machine.
18. On utilise la commande cut -d: -f1 /etc/passwd | sort -r afin d'afficher seulement la première colonne en ordre alphabétique inversé.
19. Pour connaitre le nombre d'utilisateur de la machine, il suffit de connaitre le nombre de ligne du fichier passwd. On utilise pour cela la commande wc -l /ect/passwd
20. On utilise la commande man -k conversion pour retrouver le nombre de manuel contenant conversion comme mot-clé.
21. Il y a un fichier passwd lorsque j'execute la commande find passwd.
22. Afin de mettre mettre le résultat de la commande précédente dans un fichier et de mettre ses erreurs dans un second fichier, on utilise la commande find passwd > list_passwd_files.txt 2 > /dev/null
23. Pour trouver ou est défini l'alias ll on utilise la commande grep ll
24. On utilise la commande locate history.log qui nous donne le chemin du fichier history.log
25. Rien ne se passe lorsque l'on utilise la commande locate sur un fichier du répertoire personnel car c'est le répertoire principal par défaut. En effet lorsque l'on utilise simplement la commande cd sans chemin, on arrive dans son répertoire personnel.

# Exercice 3

1. Afin de déplacer puis de renommer le fichier syslog, on utilise les commande sudo cp /var/log/syslog /home/User puis sudo mv syslog log.txt puis on utilise nano log.txt pour l'ouvrir.
2. Pour remplacer les occurrences du mort kernel pour le mot noyau, on utilise la commande ctrl + /
3. On déplace les 10 premières lignes a la fin via le raccourci alt + a ainsi que copier/coller classique.
4. Pour annuler notre action, on utilise alt + u
5. Pour enregistrer les modifications apporter avec nano, on utilise la commande ctrl + o

# Exercice 4

1. Comme pour l'exercice 3, on utilise les commandes cp et mv
2. On suit l'exercice en modifiant le bashrc.
3. Apres exécution de la commande source .bashrc, la couleur du terminal est passé de blanc a vert.
