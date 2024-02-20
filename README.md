# Minitrice

## Installation
### WSL 

Pour installer WSL (Windows Subsystem for Linux) sur votre ordinateur :
- Assurez-vous d'avoir au moins Windows 10 ou ultérieure.
- Ouvrez PowerShell en tant qu'administrateur et exécutez cette commande pour activer le sous système linux:
````bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
````
- Redémarrez votre ordinateur.
- Installez une distribution Linux depuis Microsoft Store.
- Lancez la distribution Linux et configurez un nom d'utilisateur et un mot de passe.
- Une fois installé, vous pouvez exécuter des commandes Linux directement depuis l'invite de commandes Windows ou PowerShell.

### Prérequis pour le programme minitrice
Pour pouvoir exécuter le programme minitrice, il faut s'assurer que vous avez les permissions pour lancer le script. C'est à dire quand vous faite la commande ll ou ls -l il faut que dans les permissions du script minitrice, on a des x qui permet de nous dire que l'on peut exécuter ce script. 
## Exécution

### Utilisation interactive
#### Scénario 1:
- Lancer le programme minitrice en faisant la commande ./minitrice
- Entrer une expression mathématique (par exemple, "3+9") de cette façon > 3+9
- Le programme affiche le résultat du calcul (par exemple, "12").
- Entrer une nouvelle expression ou quitter en appuyant sur `ctrl+D`.
Le programme affiche "Fin des calculs :)".
Le code de sortie du programme est 0, indiquant une exécution réussie.

Exemple d'utilisation :

```bash
$ ./minitrice
> 3+9
12
> 4*5
20
> 13-6
7
>
Fin des calculs :)
$ echo $?
0
$ 
```

### Utilisation en lisant STDIN avec `echo`
#### Scénario 2:
- Utiliser la commande echo pour envoyer une expression mathématique (par exemple, "3+12") au programme minitrice via STDIN.
- Le programme minitrice calcule le résultat de l'expression (par exemple, "15") et l'affiche.
- Le code de sortie du programme est 0, indiquant une exécution réussie.

Exemple d'utilisation :

```bash
$ echo "3+25" | ./minitrice
28
$ echo $?
0
$ 
```

