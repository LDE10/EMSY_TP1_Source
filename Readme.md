# TP1 - Installation Linux sur une VM - V0.1

## Groupe 

LDE-VMY

## But 

Cette manipulation a pour but d'installer une distribution linux [Sparky Linux](https://sparkylinux.org/) dans une machine virtuelle VMware Workstation Player, à l’aide d’une image disque (ISO).

## Materiels à disposition 

- VMware Workstation Player - V17
- Image disque (ISO) : sparkylinux-6.4-x86_64-minimalcli.iso

## Utilisation de VMware et de l'image ISO linux 

A. Lancez VMware Workstation Player (logiciel)  

B. Sélectionnez **Create a New Virtual Machine** 

C. Placez le fichier `.iso` dans une repertoire connu : 

`C:\LDE\VM\ISO`

D. Indiquez le chemin d’accès de l’image iso comme indiqué sous l’image ci-dessous :

![install image disk](/Images/Install_ISO.jpg) 

E. Choisir un nom d'OS : `Linux - Debian 11.x` 


F. Nommez la machine virtuelle : `SparkyLinux-VosInitiales` 
> SparkyLinux-LDE

G. Creez un disque virtuel -> capcité : **20GB** 

> remarque$$^1$$ : cocher **store virtual disk a single file**

![Virtual disk](/Images/VirtualDisk.jpg) 

> remarque$$^2$$ : ci-dessous, la configuration de la VM 

![Virtual disk](/Images/VM_Config.jpg) 

H. Lancez la machine virtuelle : **Play virtual machine** 

## Lancement de l'image ISO (Linux - Live CD) 

G. Lancement du live CD : 

<img width="802" height="657" alt="Linux-dep1" src="https://github.com/user-attachments/assets/3de58e06-e4b0-4cd1-aff3-9469650499d5" />

Shell Linux : 

<img width="800" height="649" alt="image" src="https://github.com/user-attachments/assets/62ebf67b-bd93-44ca-8836-9e2a062fa6ba" />


> **ATTENTION** : par défaut, le clavier est configuré est **Clavier Americain**

Q1. disposition du clavier américain ?

> qwerty

Q2. disposition du clavier suisse-romand ?

> qwertz

Q3. disposition du le clavier français ? 

> azerty


H. Déplacez-vous à la **racine du système** en utilisant la commande suivante : `cd` 

> cd /

I. Affichez le contenu de la racine avec la commande : `ls –l`	

<img width="710" height="404" alt="image" src="https://github.com/user-attachments/assets/5c97f3a0-c94c-4123-941d-8d13d9d3e0c0" />


Q5. Que signifie l'option `-l` avec la commande `ls` 

> Affiche des informations détaillées sur les fichiers(la taille et l'heure de modification)

Q6. Décrypter la ligne où se trouve le répertoire **home**    

<img width="381" height="18" alt="image" src="https://github.com/user-attachments/assets/fa6c4e98-af03-4e09-a6e7-77e75f972448" />

> drwxr-xr-x : (d) indique un répertoire (rwx) correspond aux permissions du propriétaire, le r pour la lecture du contenu, w la création ou la suppression de fichiers et sous-répertoires à l'intérieur de ce répertoire, x  l'accès au contenu du répertoire et aux fichiers qu'il contient.
> r-x correspond au droit pour le groupe : le r autorise la lecture du répertoire, - indique qu'iln'y a pas de permission d'écrir pour le groupe et x autorise l'accès au répertoire.
> Le deuxième r-x correspond aux droit pour les autres utilisateurs.
> 1 root root indique le nombre de personne lié au dossier le premier root indique l'utilisateur qui possède le répertoire et le deuxième indique le groupe auquel appartient le répertoire.
> Le nombre 60 indique l'escpace utilisé en octet et enfin la date (mois, jours et enfin heur ou année).

J. Créez un répertoire de travail nommé « EMSY_VosInitiales» dans quel dossier racine allez-vous le placer (justifiez votre réponse) et quelle commande allez-vous utiliser. 

> dans le répertoir home car c'est un répertoire personnel.
> cd home
> cd live
> mkdir EMSY_LDE

Q7. Si vous créez un répertoire de travail (pour éditer/sauvegarder des fichiers), dans quelle **répertoire racine** vous vous placez ? 

> home


K. Dans ce répertoire, créez un fichier texte que vous nommerez `TESTSLO_XXX_XXX` et éditez celui en écrivant un texte, exemple : "TP linux by XXX et XXX".
	Utiliser la commande `vi`

> vi TESTSLO_LDE_MBY

Q9. dans le répertoire `/home`, pouvez-vous éditez un fichier uniquement avec la commande `vi` 

> oui

Q10. Si vous éteignez la machine virtuelle et que vous la rallumez, est-ce que le répertoire créé ci-dessus existe toujours (justifiez votre réponse) ? 

> oui car éteindre et allumer ne supprime pas les fichiers stockés sur le disque virtuel, et les dossier dans le home sont écrits sur ce disque virtuel.

L. Tapez la commande `ls -l /dev/sda` 

<img width="404" height="35" alt="image" src="https://github.com/user-attachments/assets/e590c837-99d7-4110-b22a-8434f916799a" />


Q11. Que signifie **sda** ? 

> c'est le disque entier du VM

Q12. Décrypter la réponse après avoir taper la commande `ls -l /dev/sda` -> voir résultat point 13.

> b: indique un fichier de périphérique bloc.
> rw-rw---- : les permissions du fichier.
> 1 : le nombre de liens physiques vers le fichier.
> root : le propriétaire.
> disk : le group auquel appartient le fichier.
> 8, 0 : numéros majeur et mineur
> la date et l'heur
> et enfin le disque entier


## Tips 

> $$Tips^1$$ : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt` 

> $$Tips^2$$ : arrêter la VM proprement -> commande : `shutdown`

> $$Tips^3$$ : arrêter la VM pour cause de plantage -> commande : `halt` ou `poweroff`

> $$Tips^4$$ : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)

> $$Tips^5$$ : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)
>
Q13. Quell est la taille de disque minimum recommandée pour installer la distribution sparky ?
>Pour l'édition standard 10G au minimum.
>Pour l'édition Multimédia recommandé à 20G.
>Et pour la version en ligne (CLI) 2G minimum.

Q14. A quoi sert la partition swap ? Est-ce que ce principe existe sur les OS Microsoft Windows ?
>C'est un espace de stockage supplémentaire qui se trouve dans la RAM
 
Q15. Quel format pourriez-vous utiliser pour la 3ème partition afin qu’elle soit également accessible depuis un OS Microsoft ?
>Microsoft basic data
 
Q16. Durant l’installation, on vous demande deux noms d’utilisateur. A quoi correspondent-ils ?
un nom est pour le nom du compte d'utilisateur et le deuxième est le nom de l'administrateur
<img width="803" height="593" alt="image" src="https://github.com/user-attachments/assets/f765912a-f13d-499e-87b7-30022729f708" />

N. Après l’installation de Linux, prenez une capture d’écran du démarrage de votre système (GRUB).
![Image](https://github.com/user-attachments/assets/b88b8e87-8465-414b-b303-dec9ce36e294)

O.Trouvez la ou les lignes de commande permettant de changer le clavier (clavier suisse romand trouvable sous « German (Switzerland)) et procédez à la configuration du clavier.
 
P.Testez si l’application « nano » est installée sur votre machine, tapez la commande :

nano -version
 
Q17. À quoi sert « nano » ?restar
 >C'est un éditeur de texte qui peut être lancé avec une commande
Q.Testez si l’application « git » est installée sur votre distribution, si ce n’est pas le cas installez un client git.
 
Q18. Comment savoir si « git » est déjà installé ?
 
Q19. Quelle(s) commande(s) utilisez-vous pour l’installer ?
 
Q20. Que veut dire « apt » ?
 
Q21. Est-ce que cette commande peut être utilisée sur toutes les distributions Linux ?
 
LABO EMSY ETML-ES
 
PBY/NMI/SCA EMSY01 TP1A - InstVMLinux_v2_6.docx 5/5

R.Créez un sous-répertoire « EMSY_TP1_XXX-YYY » dans le répertoire de votre utilisateur. Attention : Ici on veut que l’utilisateur (vous) ait les droits de lecture, d’écriture et d’exécution. Q22. Quel est le répertoire utilisateur ?
 
Q23. Quelles sont les commandes que vous allez utiliser ?
 
S.Dans ce répertoire, tapez la commande :

git clone https://github.com/votreDepot/EMSY_TP1_Source
 
Il faut au préalable que vous ayez mis en place à cette adresse un fork du dépôt fourni.
 
Q24. Qu’observez-vous dans votre répertoire ?
 
T.Editez le fichier source .c avec l’éditeur de texte « nano ».

Réalisez un petit programme en C (par exemple de type « Hello world »).
 
U.Vérifiez si le compilateur « gcc » est bien installé.
 
Notez la version du logiciel.
 
Tapez les commandes suivantes :
 
gcc -Wall -o fichier.o -c fichier.c
 
gcc -o fichier fichier.o
 
Remarque : « fichier » est à remplacer par le nom de votre choix
 
Q25. Quels sont les fichiers qui ont été générés ?
 
V.Entrez la commande suivante :./fichier
 
Q26. Que se passe-t-il ?
 
## Tips
 
> $$Tips^1$$ : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt`
 
> $$Tips^2$$ : arrêter la VM proprement -> commande : `shutdown`
 
> $$Tips^3$$ : arrêter la VM pour cause de plantage -> commande : `halt` ou `poweroff`
 
> $$Tips^4$$ : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)
 
> $$Tips^5$$ : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)
 
 

