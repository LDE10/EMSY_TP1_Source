# TP1 - Installation Linux sur une VM - V0.1

## Groupe 

- vos noms 

## But 

Cette manipulation a pour but d'installer une distribution linux [Sparky Linux](https://sparkylinux.org/) dans une machine virtuelle VMware Workstation Player, à l’aide d’une image disque (ISO).

## Materiels à disposition 

- VMware Workstation Player - V17
- Image disque (ISO) : sparkylinux-6.4-x86_64-minimalcli.iso

## Utilisation de VMware et de l'image ISO linux 

A. Lancez VMware Workstation Player (logiciel)  

B. Sélectionnez **Create a New Virtual Machine** 

C. Placez le fichier `.iso` dans une repertoire connu : 

`C:\VosInitiales\VM\ISO`

D. Indiquez le chemin d’accès de l’image iso comme indiqué sous l’image ci-dessous :

![install image disk](/Images/Install_ISO.jpg) 

E. Choisir un nom d'OS : `Linux - Debian 11.x` 

![OS name choice](/Images/OS_Choice.jpg) 

F. Nommez la machine virtuelle : `SparkyLinux-VosInitiales` 
SparkyLinux-LDE

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
> Le deuxième r-x correspond aux droit pour les autres utilisateurs :  le r autorise la lecture du répertoire, - indique qu'iln'y a pas de permission d'écrir pour les autres utilisateurs et x autorise l'accès au répertoire.
> 1 root root indique le nombre de personne lié au dossier le premier root indique l'utilisateur qui possède le répertoire et le deuxième indique le groupe auquel appartient le répertoire.
> Le nombre 60 indique l'escpace utilisé en octet et enfin la date (mois, jours et enfin heur ou année).

J. Créez un répertoire de travail nommé « EMSY_VosInitiales» dans quel dossier racine allez-vous le placer (justifiez votre réponse) et quelle commande allez-vous utiliser. 

> dans le répertoir home car c'est un répertoire personnel.
> cd home
> cd live
> mkdir ...

Q7. Si vous créez un répertoire de travail (pour éditer/sauvegarder des fichiers), dans quelle **répertoire racine** vous vous placez ? 

> home


K. Dans ce répertoire, créez un fichier texte que vous nommerez `TESTSLO_XXX_XXX` et éditez celui en écrivant un texte, exemple : "TP linux by XXX et XXX".
	Utiliser la commande `vi`

> votre commande ?! 

Q9. dans le répertoire `/home`, pouvez-vous éditez un fichier uniquement avec la commande `vi` 

> votre réponse ?!

Q10. Si vous éteignez la machine virtuelle et que vous la rallumez, est-ce que le répertoire créé ci-dessus existe toujours (justifiez votre réponse) ? 

> votre réponse ?!

L. Tapez la commande `ls -l /dev/sda` 

![Placer votre capture d'écran]() 

Q11. Que signifie **sda** ? 

> votre réponse ?!

Q12. Décrypter la réponse après avoir taper la commande `ls -l /dev/sda` -> voir résultat point 13.

> votre réponse ?!


## Tips 

> $$Tips^1$$ : sortir de la VM -> appuyer simultanément sur `Ctrl` et `Alt` 

> $$Tips^2$$ : arrêter la VM proprement -> commande : `shutdown`

> $$Tips^3$$ : arrêter la VM pour cause de plantage -> commande : `halt` ou `poweroff`

> $$Tips^4$$ : [commande vi avec ses options](https://www.linuxtricks.fr/wiki/guide-de-sur-vi-utilisation-de-vi)

> $$Tips^5$$ : [éditer un fichier type markdown (.md)](https://ashki23.github.io/markdown-latex.html)

