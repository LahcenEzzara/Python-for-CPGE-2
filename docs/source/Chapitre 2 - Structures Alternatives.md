# 1. Opérateurs Relationnels
Se sont aussi des **opérateurs de comparaisons**.

Ces opérateurs peuvent s’appliquer sur les `nombres`, les `chaînes de caractères` et les `booléens`.

Ces opérateurs renvoient une valeur **booléenne** (True ou False).

* **Strictement Inférieur** `<` :

Exemple :

```Python
a=23 < 55
print(a)
```
Output :
```Python
True
```
* **Strictement Supérieur** `>` :

Exemple :
```Python
B=7>12
print(B)
```
output :
```Python
False
```
* **Inférieur ou égal** `<=` :

Exemple :
```Python
print(3<=3)
```
Output :
```Python
True
```
* **Supérieur ou égal** >= :

Exemple :
```Python
print(4>=7)
```
Output :
```Python
False
```
* **Egal** `==` :

Exemple :
```Python
print('p'=='p')
```
Output :
```Python
True
```
* **Différent** `!=` :

Exemple :
```Python
print(3!=3.0)
```
Output :
```Python
True
```
Résumé :
|Symbole|Opération|Exemple|
|:---:| :---: | :---: |
|<|Strictement Inférieur|4 < 8|
|>|Strictement Supérieur|4 > 8|
|<=|Inférieur ou égal|1 <= 0.1|
|>=|Supérieur ou égal|8 >= 8|
|==|Egal|5 == 7|
|!=|Différent|6 ! = 1|
***
# 2. Opérateurs Logiques
Ces opérateurs ne peuvent s’appliquer que sur les **booléens**.

Ces opérateurs renvoient une valeur **booléenne** (True ou False).

* **Disjonction** `or` :

Exemple :

```Python
a=1==2
b=5>2
print(a or b)
```
Output :
```Python
True
```
* **Conjonction** `and` :

Exemple :
```Python
print(3>6 and 1==1)
```
Output :
```Python
False
```
* **Négation** `not` :

Exemple :
```Python
print(not 1>6)
```
Output :
```Python
True
```
Résumé :
|Symbole|Opération|Exemple|
|:---:| :---: | :---: |
|or|Disjonction|A or B|
|and|Conjonction|A and B|

**Table de vérité de `or`** :
|A|B|A or B|
|:---:| :---: | :---: |
|True|True|True|
|True|False|True|
|False|True|True|
|False|False|False|

**Table de vérité de `and`** :
|A|B|A and B|
|:---:| :---: | :---: |
|True|True|True|
|True|False|False|
|False|True|False|
|False|False|False|

**Table de vérité de `not`** :
|A|not A|
|:---:| :---: |
|True|False|
|False|True|
***
# 3. Instruction Conditionnelle
La structure conditionnelle permet de **prendre des décisions**.

## 3.1. L’Instruction if
Syntaxe :

```Python
if Condition :
    Bloc d’Instructions
```
**Condition** est une expression booléenne, cad une expression qui prend pour valeur True ou False.

Si la **condition** est Vrai le bloc d’instruction s’**exécute**, sinon le bloc ne n’exécute pas.

Exemple 1 :
```Python
age=32
if age >= 18 :
    print("Vous êtes accepté")
```
Output :
```Python
Vous êtes accepté
```
Exemple 2 :
```Python
filiere="MP"
if filiere=="PSI":
    print("Vous êtes un PSI")
if filiere=="ECT":
    print("Vous êtes un ECT")
```
Output :

Rien !

## 3.2. L’Instruction if - else
Syntaxe :
```Python
if Condition :
	Bloc d’Instructions A
else :
	Bloc d’Instructions B
```
Si la condition est vrai le bloc A s’exécute et B non, sinon le bloc B s’exécute au contraire du bloc A.

Exemple 1 :
```Python
age=20
if age >= 18 :
    print("Majeur")
else :
    print("Mineur")
```
Output :
```Python
Majeur
```
Exemple 2 :
```Python
age=12
if age >= 18 :
    print("Majeur")
else :
    print("Mineur")
```
Output :
```Python
Mineur
```
## 3.3. L’Instruction if - elif - else
Syntaxe :
```Python
if Condition A :
	Bloc d’Instructions A
elif Condition B :
	Bloc d’Instructions B
elif Condition C :
	Bloc d’Instructions C
…
else :
	Bloc d’Instructions N
```
Si la condition A est Vraie le bloc A s’exécute, sinon on examine la condition B… et si aucune de ses conditions n’est Vraie le bloc N s’exécute.

Exemple :
```Python
n=4
if n > 0 :
    print(n,"est positif")
elif n < 0 :
    print(n,"est négatif")
else :
    print(n,"est neutre")
```
Output :
```Python
4 est positif
```
# 4. Principe d’Indentation
Une **indentation** représente un ou plusieurs espaces au début d'une ligne de code.

Il est recommandé en Python d'indenter son code avec 4 espaces (équivalent à 1 tabulation).

L'indentation est **primordiale** en Python car elle sert à déterminer les blocs qui constituent votre code.

Exemple :
```Python
age=10
if age >= 18 :
    print("Majeur")
else :
    print("Mineur")
```
Dans ce cas le bloc contenant `print("Majeur")` est indenté, pour le séparer du bloc principal, car il ne s’exécute que si la condition `age>=18` est Vraie (True).