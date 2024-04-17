# Go Language 
## Histoire du Go
Go est un langage de programmation compilé et concurrent inspiré de C et Pascal. Il a été développé par Google à partir d’un concept initial de Robert Griesemer (en), Rob Pike et Ken Thompson.

Go veut faciliter et accélérer la programmation à grande échelle : en raison de sa simplicité, il est donc concevable de l’utiliser aussi bien pour écrire des applications, des scripts ou de grands systèmes. Cette simplicité est nécessaire aussi pour assurer la maintenance et l’évolution des programmes sur plusieurs générations de développeurs.

S’il vise aussi la rapidité d’exécution, indispensable à la programmation système, il considère le multithreading comme le moyen le plus robuste d’assurer sur les processeurs actuels cette rapidité6 tout en rendant la maintenance facile par séparation de tâches simples exécutées indépendamment afin d’éviter de créer des « usines à gaz ». Cette conception permet également le fonctionnement sans réécriture sur des architectures multi-cœurs en exploitant immédiatement l’augmentation de puissance correspondante. 

## Installation du Go
Tout d'abord, téléchargez la dernière version de Go depuis le site officiel (https://golang.org/dl/).

Une fois téléchargé, extrayez l'archive dans un répertoire de votre choix. Par exemple, vous pouvez extraire l'archive dans /usr/local/ :

    sudo tar -C /usr/local -xzf go1.X.X.linux-amd64.tar.gz

Ajoutez le répertoire bin de Go à votre variable d'environnement PATH. Vous pouvez le faire en ajoutant la ligne suivante à votre fichier ~/.profile, ~/.bashrc ou ~/.zshrc :

    export PATH=$PATH:/usr/local/go/bin

Après avoir enregistré les modifications, rechargez le fichier de configuration de votre shell :

    source ~/.bashrc

Vérification de l'installation :

    Vous pouvez maintenant vérifier si Go a été installé correctement en exécutant la commande go version :

    go version

## Hello World

Exécution de programmes Go :

Pour exécuter un programme Go, vous devez d'abord écrire le code source dans un fichier avec l'extension .go, puis le compiler et l'exécuter.
Par exemple, si vous avez un fichier hello.go contenant :

    package main

    import "fmt"

    func main() {
        fmt.Println("Hello, World!")
    }

Vous pouvez compiler et exécuter le programme en utilisant la commande suivante :

    go run hello.go

Si vous souhaitez seulement compiler le programme sans l'exécuter, vous pouvez utiliser la commande go build suivie du nom du fichier :

    go build hello.go

Cela créera un exécutable nommé hello que vous pouvez exécuter en utilisant ./hello.

## Bon bon bon...
`Passons aux choses sérieuse, ces petits exercice vous permettrons de comprendre les bases du Go alors bon courage:`

1 - Addition simple :
Écrivez un programme Go qui prend deux nombres entiers en entrée et affiche leur somme.

2 - Vérification de nombre pair/impaire :
Écrivez un programme Go qui prend un nombre entier en entrée et détermine s'il est pair ou impair.

3 - Calcul de la factorielle :
Écrivez un programme Go qui calcule la factorielle d'un nombre entier positif.

4 - Conversion de température :
Écrivez un programme Go qui convertit une température donnée en degrés Celsius en degrés Fahrenheit.

5 - Recherche de nombres premiers :
Écrivez un programme Go qui trouve tous les nombres premiers jusqu'à un certain nombre donné.

6 - Calcul de la somme des chiffres :
Écrivez un programme Go qui calcule la somme des chiffres d'un nombre entier.

7 - Vérification de palindrome :
Écrivez un programme Go qui vérifie si un mot donné est un palindrome.

8 - Calcul du PGCD :
Écrivez un programme Go qui calcule le Plus Grand Commun Diviseur (PGCD) de deux nombres donnés.

9 - Tri d'une liste d'entiers :
Écrivez un programme Go qui trie une liste d'entiers donnée dans l'ordre croissant.

10 - Jeu de devinettes :
Écrivez un programme Go qui génère un nombre aléatoire entre 1 et 100, puis permet à l'utilisateur de deviner ce nombre. Le programme doit donner des indications sur la direction dans laquelle l'utilisateur doit ajuster sa devin

11 - BONUS
Vous connaissez my_str_to_word_array ?

