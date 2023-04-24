# 1. Notion de Fonction

Une **fonction** est un bloc (un ensemble) d'instructions créées pour effectuer une tâche précise.
On peut exécuter une fonction autant de fois qu'on le souhaite en **l’appelant** avec son **nom**.

L'**appel** d'une fonction conduit à l’**exécution** des instructions qu’elle **contient**.

Syntaxe :
```Python
def nom_de_la_fonction (parametre1 , parametre2 , ... , parametreN ) :
    Bloc d'Instructions
```
Exemple :

Une fonction pour le calcul du double d’un nombre :
```Python
def double(n):
    m=n*2
    print(m)
```
Exemple d’Exécution :
```Python
double(3)
```
Output :
```Python
6
```
Remarques :
* Les fonctions se nomment exac tement comme une variable.
* Les paramètres seront fournis lors d'un appel à la fonction.

Exemple :

Fonction Sans Paramètres :
```Python
def Hello():
    print("Hello World!")
```
Exemple d’exécution :
```Python
Hello()
```
Output :
```Python
Hello World!
```
***
# 2. L’Instruction `return`
En programmation, nous voudrons souvent récupérer le résultat d’une fonction afin de l’utiliser dans le reste de notre programme. Pour cela, il va falloir qu’on demande à notre fonction de **retourner** (**renvoyer**) le résultat de ses opérations. Nous pouvons faire cela en Python grâce à l’instruction `return`.

Exemple :

Une fonction qui renvoie le carrée un entier.
```Python
def carre(n) :
    c=n**2
    return c
```
Dans ce cas la fonction `carre` renvoie le carré du nombre dont on a passé en paramètre `n`.

Alors pour utiliser la valeur renvoyée par cette fonction on doit l’assigner à une variable.

Exemple d’exécution :
```Python
a=carre(3)
print(a)
```
Output :
```Python
9
```
Remarque :

* L’instruction `return` va terminer l’exécution d’une fonction, c’est pourquoi on place généralement cette instruction en fin de fonction puisque le code qui suit return dans une fonction ne sera jamais lu ni exécuté.
* On appel une fonction qui ne renvoie de valeur Procédure.

Exemple :
```Python
def carre(n) :
    return n**2
    return 2
```
***
# 3. Appel d’une Fonction dans un Programme

L’appel d’une fonction, c’est l’utiliser ce qui permet d’exécute ce qui est à son intérieur.

On peut appeler une fonction dans le programme principal tant de fois qu’on souhaite le faire.

Exemple :
```Python
def Double(n) :
    return n*2
```
Appel à la fonction `Double` :
```Python
x=Double(10)
print("Le double de 10 est :",x)
```
Output :
```Python
Le double de 10 est : 20
```
***
# 4. Appel d’une Fonction dans une Autre Fonction
Une fonction peut appeler une autre fonction, cette dernière peut appeler une autre fonction et ainsi de suite ( et autant de fois qu'on le veut ).

Exemple :

Le produit de deux entiers :
```Python
def somme(n,m):
    return n+m

def produit(n,m):
    p=0
    for i in range(m):
        p=somme(p,n)
    return p
```
La fonction `somme` renvoie la somme de deux entiers et la fonction `produit` utilise la fonction `somme` pour qu’en fin faire envoyer le produit de deux entiers (en basant sur des sommes).

Exemple d’exécution :
```Python
print(produit(3,7))
```
output :
```Python
21
```
***
# 5. Variables Locales/Globales
Une variable est dite **locale** lorsqu'elle est créée dans une fonction. Elle n'existera et ne sera visible que lors de l'exécution de cette fonction.

Exemple :
```Python
def factorielle(n) :  # La fonction factorielle permet de calculer le factoriel d'un entier
    if n==0 :
        return 1
    f=1
    for i in range(1,n+1) :
        f*=i
    return f
```
Dans ce cas les variables `f` et `i` sont des variables locales.

Une variable est dite **globale** lorsqu'elle est créée dans le programme principal. Elle sera visible partout dans le programme.

Exemple :
```Python
date_naissance = 1991

def age(date) :
    return 2023 – date
```
`date_naissance` est une variable **globale**, elle est visible partout, en particulier par la fonction `age`.

Remarque :

On ne peut pas modifier la valeur d’une variable globale directement à l’intérieur d’une fonction.

Exemple :
```Python
n=3
def modifier() :
    n=0
    return n

print(modifier())
print(n)
```
Output :
```Python
0
3
```
On remarque que la fonction `modifier` renvoie la valeur `0` (valeur de n), mais print(n) affiche `3` ce qui veux dire que la valeur de la variable globale `n` n’est pas modifiée par cette fonction mais `n` qui est à l’intérieur de la fonction est une nouvelle variable locale à la fonction.

Afin de modifier la valeur de `n` (globale), on utilise l’instruction `global`.

Exemple :
```Python
n=3
def modifier() :
    global n
    n=0
    return n

print(modifier())
print(n)
```
Output :
```Python
0
0
```
Dans ce cas nous avons pu modifier la valeur de la variable global `n`.
***
# 6. Fonctions Récursives
Une fonction **récursive** est une fonction qui s'appelle elle-même.

Exemple :

Version Itérative :
```Python
def factorielle(n) :
    if n==0 :
        return 1
    f=1
    for i in range(1,n+1) :
        f*=i
    return f
```
Version Récursive :
```Python
def rec_factorielle(n) :
    if n==0 or n==1 :
        return 1
    return n*rec_factorielle(n-1)
```