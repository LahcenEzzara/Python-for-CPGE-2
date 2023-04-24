# 1. Notion de Programme Informatique
**Un programme informatique** est un ensemble d'instructions et d’opérations destinées à être exécutées par un ordinateur.
***
# 2. Les Variables
## 2.1. Notion de Variable
**Une variable** est une zone de la mémoire dans laquelle une valeur est stockée.

Pour nous (programmeurs) : cette variable est définie par un nom.

Pour l'ordinateur il s'agit en fait d'une adresse.

Une variable se caractérise par :
* Un Nom ;
* Un Type ;
* Une valeur.

**La déclaration d’une variable** : c'est indiquer à l’ordinateur qu'il doit réserver un emplacement mémoire pour que le programmeur puisse y stocker une donnée.

Exemple en langage C :
```C
int n;
```

**L’initialisation d’une variable** : c’est donner la valeur de la variable au moment de sa déclaration.

Exemple en langage C :

```C
int n=2;
```

**L'affectation** : c’est attribuer à une variable une valeur au cours de l'exécution du programme à l'aide de l'opérateur d'affectation `=` (Reçoit).

Exemple en langage C :
```C
int n=2;
n=4;
```
On peut distinguer deux types d’affectation : 
* Affectation Simple.

Exemple :
```python
var = 4
```
* Affectation Parallèle.

Exemple :
```python
a, b = 1, 5
```
Dans cet exemple `a` reçoit 1 et `b` reçoit 5.

En Python, la **déclaration** et l’**initialisation** d'une variable se font **en même temps**.

Exemples :
```python
n=2
Age=32
```
## 2.2. Types des Variables
**Le type d'une variable** correspond à sa nature.

On rencontre généralement quatre types principaux :

* Les **Entiers** symbolisés en Python par `int` (integers).

Exemples :
```python
a=4
b=-7
c=0
```
* Les **Réels** symbolisés en Python par `float` (floating point numbers).

Exemples :
```Python
d=12.5
e=pi
f=2.0
```
* Les **Chaînes de Caractères** symbolisées par `str` (strings).

Exemples :
```Python
cours='Python'
information=''Python est un langage de programmation''
lettre='p'
```
Les **Booléens** symbolisés en Python par `bool` (Booleans).

Exemples :
```python
compris=True
compris=False
```
On peut savoir le **type** d’une variable en utilisant l’instruction `type()` , par exemple :
```Python
n=2
type(n)
```
Output :
```Python
<class 'int'>
```
Cad `n` est une variable de type entier (`int`).

Python est un langage au **typage dynamique**.

Cad vous n'avez pas besoin de **déclarer** le type d'une variable avant de l'utiliser. Le type de variable est **déterminé automatiquement** à l'exécution en fonction de la valeur que vous lui attribuez.

Exemple 1 :
```Python
Nom='Python'
type(Nom)
```
Output :
```Python
<class 'str'>
```
Exemple 2 :
```Python
age=32
type(age)
```
Output :
```Python
<class 'int'>
```
## 2.3. Nommage des Variables
Les noms des variables subissent à des règles, ils peuvent être constitués de :
* **Lettres Minuscules** : `a,b,c,...,z`.

Exemples :
```Python
nom="Python"
age=32
happy=True
```

* **Lettres Majuscules** : `A,B,C,...,Z`.

Exemples :
```Python
Nom="Python"
AgE=32
HAPPY=True
```
* **Nombres** : `0,1,...,9`.

Exemples :
```Python
Nom1="Python"
AgE23=32
HA09PPY=True
```
* **Caractère souligné** : `_`.

Exemples :
```Python
Le_nom="Python"
mon_Age=32
I_am_happy=True
```
**Remarques :**

* Il n'est pas recommandé de le faire **débuter** par le caractère `_`.

Exemples :
```Python
_nom="Python"
_Age=32
_happy=True
```

* Il est **interdit** d’utiliser d'espace dans un nom de variable.

Exemples :
```Python
Le nom="Python"
mon Age=32
I am happy=True
```

* Il faut **éviter** d'utiliser un mot réservé par Python comme nom de variable (`print`, `range`, `for`, `from`,..).

Exemple :
```Python
from="Morocco"
```

* Python est **sensible à la casse** cad les variables `Python` , `PYTHON` , `python` , `pyThon` sont `différentes`.
***
# 3. Les Opérateurs
## 3.1. Notion d’Opérateur
Les **Opérateurs** sont des symboles qui permettent de manipuler des variables, c'est-à-dire effectuer des opérations, les évaluer,...

Exemples : `+,-,>,...`

Une **expression** : c'est une combinaison de variables, d'opérateurs, en suivant les règles de priorité du langage de programmation pour produire une nouvelle valeur.

Exemples :
```Python
n=5
somme=12+7+n
expression=6>4
```
## 3.2. Opérations Arithmétiques sur Les Nombres
Ces opérateurs renvoient un nombre.

* L’**Addition** `+` :
```Python
Somme=3+6
Somme
```
Output :
```Python
9
```

* La **Soustraction** `-` :
```Python
age=2023-1991
age
```
Output :
```Python
32
```
* La **Multiplication** `*` :
```Python
duree=2*60
duree
```
Output :
```Python
120
```

* La **Division Réelle** `/` :
```Python
nombre=5/2
nombre
```
Output :
```Python
2.5
```
* La **Puissance** `**` :
```Python
p=3**2
p
```
Output :
```Python
9
```
* La **Division Entière** `//` :
```Python
Quotient=5//2
Quotient
```
Output :
```Python
2
```

* Le **Reste de la Division Entière** `%` :
```Python
reste=5%2
reste
```
Output
```Python
1
```
**Résumé :**

|Symbole| Opération | Exemple |
|:---:| :---: | :---: |
|   +   |   Addition    | 2 + 12 |
|   -   |   Soustraction| 1.5 - 7 |
|   *   |   Multiplication| 5 * 3 |
|   /   |   Division Réelle| 13 / 2 |
|   **  |   Puissance| 3 ** 2 |
|  //   |   Division Entière| 13 // 2 |
|   %   |Reste de la Division Entière| 13 % 2 |

## 3.3. Les Commentaires
Les **commentaires** sont des portions du code que l’ordinateur n'exécute pas.

Les commentaires sont le plus souvent utilisés pour **expliquer** le code.

En Python, on insère un commentaire avec le caractère `#` (un dièse).

Exemples :
```Python
var='Python' # Le nom
Age=32
a=1991 # Année de naissance
age=2023-a
```
Si on désire insérer des commentaires sur plusieurs lignes on utilise trois guillemets `'''` ou `"""`.

Exemple :
```Python
"""
Ce programme informatique sert à : 
1. Stocker deux valeurs dans deux variables
2. Calculer la somme de ces deux variables et la stocker dans une nouvelle variable
"""
a = 2
b = 6
Somme = a + b
```
***
# 4. Gestion d’entrée/sortie
## 4.1. L’Instruction d’Écriture
La fonction `print` nous permet d’**afficher sur l'écran** les valeurs qu’on lui **met entre parenthèses**.

Exemple:
```Python
print('Hello World!')
```
Output :
```Python
Hello World!
```
On peut afficher **plusieurs valeurs** :

Exemple :
```Python
nom='Python'
age=32
print('Je suis',nom,"j'ai",age,'ans!')
```
Output :
```Python
Je suis Python j'ai 32 ans!
```
**Écriture formatée f-strings**

Programme **Version 1** :
```Python
nom='Python'
age=32
print('Je suis',nom,"j'ai",age,'ans!')
```
**Version f-strings :**
```Python
nom='Python'
age=32
print(f"Je suis {nom} j'ai {age} ans!")
```
## 4.2. L’Instruction de Lecture
La fonction `input()` nous permet de saisir des données au programme à l’aide du clavier.

Exemple:
```Python
age = input()
```

**Remarque :**

La fonction **input()** renvoie **toujours une chaîne de caractères**.

Alors si on veut avoir un autre **type**, on doit **convertir** les données saisies vers le type voulu.
```Python
age=int(input())
print(type(age))
```
Output :
```Python
32
<class 'int'>
```
On peut afficher un message d’information avec la fonction `input()`

Exemple :
```Python
nom=input('Saisissez votre nom SVP!:')
```
Output :
```Python
Saisissez votre nom SVP!:
```