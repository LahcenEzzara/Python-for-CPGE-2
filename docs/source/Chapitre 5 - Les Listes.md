# 1. Notion de List
Les variables ne permettent de stocker qu'une seule donnée à la fois.

Alors afin de stocker plusieurs données en une même variable, on fait appel aux **structures de données**.

Une **liste** est une structure de données qui contient une **série de valeurs**.

En Python, une liste peut contenir des valeurs de types différents.

Exemple :
```Python
# Une liste Age qui contient l’âge de chacun des étudiants d'une classe

Age = [20, 19, 21, 20, 19, 20, 20, 20]
```
Remarque :

Le nombre d’élément d’une liste s’appelle la **longueur** de la liste.

Exemple :
```Python
Age = [20, 19, 21, 20, 19, 20, 20, 20]
# Age est une liste de longueur : 8.
```
***
# 2. Création d’une Liste
## 2.1. Syntaxe
En Python, la création d’une liste se fait simplement par insertion des différentes valeurs entre crochets en les séparées par virgules.

Syntaxe :
```Python
L = [val1, val2 , ..., ValN]
```
Exemples :
```Python
# Création d'une liste vide :
L=[]

# Création de liste d'entiers :
L=[3, 8, 5, 0]

# Création de liste de données de types différents
L=[5, 'Hello', 3.14, 'Python', True]
```
Pour **afficher** une liste on utilise l’instruction `print`.

Exemple :
```Python
L=[5, 'Hello', 3.14, 'Python', True]
print(L)
```
Output :
```Python
[5, 'Hello', 3.14, 'Python', True]
```
***
## 2.2. Les fonctions `range()` et `list()`
La combinaison des fonctions `list()` et `range()` donne une liste dont les éléments sont la séquence d’entiers définie par la fonction `range()`.

Exemple :
```Python
L=list(range(1,11))

print(L)
```
Output :
```Python
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
***
# 3. Parcours d’une Liste
## 3.1. Principe d’indexage

En Python, les éléments d’une liste sont indexés par des entiers (Positifs et Négatif).

Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
```
|Elément|'Youssef'|'Khadija'|'Soukaina'|'Ahmed'|
|:---:| :---: | :---: | :---: | :---: |
|Indice Positif|0|1|2|3|
|Indice Négatif|-4|-3|-2|-1|

L’élément `'Khadija'` est d’indice `1`, alors pour accéder à cet élément on écrit `L[1]`, et `-3` est aussi son indice alors on peut accéder au même élément `'Khadija'` avec `L[-3]`.

```Python
# Affichage de 'Khadija' :

L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

print(L[1])

# ou bien :

print(L[-3])
```
Output :
```Python
Khadija
Khadija
```
Remarques :
* L’un des avantages des indices négatifs est la possibilité d’accéder au dernier élément de la liste sans connaitre sa longueur ( L[-1] ).
* Les listes sont des structures de données mutables cad on peut les modifier après leur création.
Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

print("L avant modification :", L)

L[0] = 'Mohamed'

print("L après modification :", L)
```
Output :
```Python
L avant modification : ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
L après modification : ['Mohamed', 'Khadija', 'Soukaina', 'Ahmed']
```
On remarque que le premier élément de la liste L `'Youssef'` a été remplacé par `'Mohamed'`.
***
## 3.2. Parcours d’une liste par Indice
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
```
Dans ce cas on connait que la longueur de la liste L est : 4
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

for i in range(4) :
    print(L[i])
```
Output :
```Python
Youssef
Khadija 
Soukaina
Ahmed
```
A chaque fois i prend une valeur de 0 à 3 alors on affiche L[i] l’élément d’indice i.
***
## 3.3. Parcours d’une liste par Élément
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

for x in L :
    print(x)
```
Dans ce cas x prend les valeurs des éléments de L au lieu des valeurs des indices.
***
# 4. Concaténation de Listes
La **concaténation** de deux listes en Python est le fait de combiner les éléments ces deux listes pour en former une seule.

Pour concaténer deux listes en Python, on peut utiliser l'opérateur `+` ou la méthode `extend`.

Exemple 1 :
```Python
# Concaténation de deux listes d'étudiants
classe1 = ['Youssef', 'Khadija', 'Soukaina']
classe2 = ['Ahmed']
reunion= classe1 + classe2

print(reunion)
```
Output :
```Python
['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
```
Exemple 2 :
```Python
# Concaténation de deux listes d'étudiants
classe1 = ['Youssef', 'Khadija', 'Soukaina']
classe2 = ['Ahmed']

classe1.extend(classe2)

print(classe1)
```
Output :
```Python
['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
```
***
# 5. Duplication d'une Liste
La **duplication** d’une liste est une liste qui dont les éléments sont ceux de la liste d’origine répètes un certain nombre de fois.

Pour dupliquer une liste on utilise l’opérateur `*`.

Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
M = L*3
print(M)
```
Output :
```Python
['Youssef', 'Khadija', 'Soukaina', 'Ahmed', 'Youssef', 'Khadija', 'Soukaina', 'Ahmed', 'Youssef', 'Khadija', 'Soukaina', 'Ahmed']
```
***
# 6. Création d’une copie d’une Liste
La méthode `copy()` permet de créer une copie d'une liste.

Syntaxe :
```Python
nouvelle_liste = liste.copy()
```
Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

M=L.copy()

print("L :",L)
print("M :",M)
```
Output :
```Python
L : ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
M : ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
```
***
# 7. Longueur d’une Liste
La **longueur** d’une liste est son nombre d’éléments.

La fonction `len()` renvoie la longueur de la liste qu’on lui passe en paramètre.

Syntaxe :
```Python
len(liste)
```
Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

longueur=len(L)
print("La longueur de la liste L est",longueur)
```
Output :
```Python
La longueur de la liste L est 4
```
***
# 8. Recherche d’indice d’un élément dans une Liste
La méthode `index()` renvoie l’indice d’un élément dans une liste.

Syntaxe :
```Python
liste.index(element)
```
Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

print(L.index('Soukaina'))
```
Output :
```Python
2
```
Remarque :

Si l’élément passé en paramètre de `index()`, n’existe pas dans la liste, cela engendre une erreur.

Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

print(L.index('Mohamed'))
```
Output :
```Python
ValueError: 'Mohamed' is not in list
```
***
# 9. Test d’appartenance d’un élément à une Liste
C’est vérifier si un élément donné est présent dans la liste ou non.

Pour ce faire on peut utiliser l’opérateur `in`.

Syntaxe :
```Python
element in liste
```
Exemple 1 :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

membre = 'Youssef' in L
print(membre)

print('Mohamed' in L)
```
Output :
```Python
True
False
```
Exemple 2 :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

print('Ali' not in L)
```
Output :
```Python
True
```
***
# 10. Les fonctions min(), max(), sum() sur les Listes
Dans cette section, on doit vérifier que la fonction `min()`, `max()` ou `sum()` est définie pour les éléments de la liste passée en paramètre sinon cela va engendre une erreur.

* La fonction **`min()`** renvoie le **minimum** d’éléments d’une liste.

Syntaxe :
```Python
min(liste)
```
Exemple :
```Python
L = [34, 63, 22, 10,40]

print("Le plus petit nombre des éléments de la liste L est :",min(L))
```
Output :
```Python
Le plus petit nombre des éléments de la liste L est : 10
```
* La fonction **`max()`** renvoie le **maximum** d’éléments d’une liste.

Syntaxe :
```Python
max(liste)
```
Exemple :
```Python
L = [34, 63, 22, 10,40]

print("Le plus grand nombre des éléments de la liste L est :",max(L))
```
Output :
```Python
Le plus grand nombre des éléments de la liste L est : 63
```
* La fonction **`sum()`** renvoie la **somme** d’éléments d’une liste.

Syntaxe :
```Python
sum(liste)
```
Exemple :
```Python
L = [1,4,3]

print("La somme des éléments de la liste L est :",sum(L))
```
Output :
```Python
La somme des elements de la liste L est : 8
```
***
# 11. Ajout d’éléments à la fin d’une Liste
* La méthode `append()` permet d’ajouter un et un seul élément à la fin d’une liste.

Syntaxe :
```Python
liste.append(element)
```
Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

print(L)
L.append('Mohamed')
print(L)
```
Output :
```Python
['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
['Youssef', 'Khadija', 'Soukaina', 'Ahmed', 'Mohamed']
```
* La méthode `extend()` permet d'ajouter plusieurs éléments à la fin d'une liste.

Syntaxe :
```Python
liste.extend(liste)
```
Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

print(L)
L.extend(['Mohamed','Karima','Ali'])
print(L)
```
Output :
```Python
['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
['Youssef', 'Khadija', 'Soukaina', 'Ahmed', 'Mohamed', 'Karima', 'Ali']
```
***
# 12. Insertion d’éléments dans une Liste
La méthode `insert()` permet d’insérer un élément à une position spécifiée dans une liste, elle prend en argument : l’élément à insérer et la position ou l’insérer.

Syntaxe :
```Python
liste.insert(indice,element)
```
Exemple :
```Python
L = ['Youssef', 'Khadija', 'Soukaina', 'Ahmed']

print(L)
L.insert(1,'Ali')
print(L)
```
Output :
```Python
['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']
```
***
# 13. Suppression d’éléments d’une Liste
## 13.1. remove()
La méthode `remove()` permet de supprimer la première occurrence d'un élément spécifié dans une liste.

Syntaxe :
```Python
liste.remove(element)
```
Exemple :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']

print(L)
L.remove('Ali')
print(L)
```
Output :
```Python
['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']
['Youssef', 'Khadija', 'Soukaina', 'Ahmed']
```
***
## 13.2. del()
L’opérateur `del()` permet de supprimer un élément d’une liste dont on connait l’indice.

Syntaxe :
```Python
del(liste[indice])
```
Exemple :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']

print(L)
del(L[2])
print(L)
```
Output :
```Python
['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']
['Youssef', 'Ali', 'Soukaina', 'Ahmed']
```
***
## 13.3. pop()
La méthode `pop()` permet de supprimer un élément spécifié d'une liste et renvoyer cet élément.

La méthode `pop()` supprime l'élément ayant l'indice spécifié dans la liste et renvoie cet élément. Si aucun indice n'est spécifié, la méthode `pop()` supprime et renvoie le dernier élément de la liste.

Syntaxe :
```
liste.pop() # Dans ce cas le dernier élément qui sera supprimer
liste.pop(indice)
```
Exemple 1 :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']

print(L)
x=L.pop()
print(L)
print("l'élément supprimé est :",x)
```
Output :
```Python
['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']
['Youssef', 'Ali', 'Khadija', 'Soukaina']
l'élément supprimer est : Ahmed
```
Exemple 2 :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']

print(L)
L.pop(2)
print(L)
```
Output :
```Python
['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']
['Youssef', 'Ali', 'Soukaina', 'Ahmed']
```
***
## 13.4. clear()
La méthode `clear()` permet de supprimer tous les éléments d'une liste, laissant la liste vide.

Syntaxe :
```Python
liste.clear()
```
Exemple :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Youssef', 'Soukaina', 'Ahmed']

L.clear()

print(L)
```
Output :
```Python
[]
```
***
# 14. Inverser une Liste
La méthode `reverse()` permet d'inverser l'ordre des éléments d'une liste.

Syntaxe :
```Python
liste.reverse()
```
Exemple :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']

print(L)
L.reverse()
print(L)
```
Output :
```Python
['Youssef', 'Ali', 'Khadija', 'Soukaina', 'Ahmed']
['Ahmed', 'Soukaina', 'Khadija', 'Ali', 'Youssef']
```
***
# 15. Tri d’une Liste
La méthode `sort()` permet de trier une liste en place, c'est-à-dire de modifier la liste originale sans créer une nouvelle liste.

Syntaxe :
```Python
liste.sort()
```
Exemple 1 :
```Python
L=[5,2,4,1,3]

print(L)
L.sort()
print(L)
```
Output :
```Python
[5, 2, 4, 1, 3]
[1, 2, 3, 4, 5]
```
Exemple 2 :
```Python
L=[5,2,4,1,3]

print(L)
L.sort(reverse=True)
print(L)
```
Output :
```Python
[5, 2, 4, 1, 3]
[5, 4, 3, 2, 1]
```
***
# 16. Nombre d’occurrences d’un élément dans une Liste
La méthode `count()` permet de compter le nombre d'occurrences d'un élément donné dans une liste.

Syntaxe :
```Python
liste.count(element)
```
Exemple 1 :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Youssef', 'Soukaina', 'Ahmed']

n=L.count('Youssef')
print(n)
```
Output :
```Python
2
```
Exemple 2 :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Youssef', 'Soukaina', 'Ahmed']

print(L.count('Mohamed'))
```
Output :
```Python
0
```

***
# 17. Liste de Listes
## 17.1. Notion de Liste de Listes
Une **liste de listes** est une structure de données qui contient plusieurs listes imbriquées les unes dans les autres. Chaque liste interne peut contenir des éléments de différents types (nombres, chaînes de caractères, etc.), y compris d'autres listes.

Syntaxe :
```Python
liste=[[x1, x2, ...], [x3, x4, ...], [x5, x6, ...], ...]
```
Exemple :
```Python
# une liste qui contient les listes des groupes d'une classe

Groupes = [["Amina", "Fatima"], ["Mohammed", "Youssef"], ["Sara", "Naima"], ["Karim", "Ahmed"], ["Hajar", "Loubna"], ["Mounir", "Abdelatif"]]
```
***
## 17.2. Accès aux éléments d’une Liste de Listes
Il faut noter que les éléments de la liste Groupes sont des listes alors pour accéder la première liste on utilise Groupes[0] :
```Python
Groupes = [["Amina", "Fatima"], ["Mohammed", "Youssef"], ["Sara", "Naima"], ["Karim", "Ahmed"], ["Hajar", "Loubna"], ["Mounir", "Abdelatif"]]
print(Groupes[0])
```
Output :
```Python
['Amina', 'Fatima']
```
Pour accéder à un élément d’une liste interne en utilise `Groupes[i][j]`, par exemple accéder à `"Mohammed"` :
```Python
Groupes = [["Amina", "Fatima"], ["Mohammed", "Youssef"], ["Sara", "Naima"], ["Karim", "Ahmed"], ["Hajar", "Loubna"], ["Mounir", "Abdelatif"]]

print(Groupes[1][0])
```
Output :
```Python
Mohammed
```
***
# 18. Le Tranchage (Slicing)
Le **Tranchage** de liste permet de sélectionner une partie d'une liste en utilisant des indices, en extrayant une partie de la liste originale.

Syntaxe :
```Python
nouvelle_liste = liste[indice_debut:indice_fin:pas]
```
Remarque :

L’élément d’indice indice_debut est inclus et indice_fin est exclu.

Exemple 1 :
```Python
L = ['Youssef', 'Ali', 'Khadija', 'Youssef', 'Soukaina', 'Ahmed']

M = L[1:4]
print(M)
```
Output :
```Python
['Ali', 'Khadija', 'Youssef']
```
Exemple 2 :
```Python
L = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

print(L[1:7:2])
```
Output :
```Python
[1, 3, 5]
```
Résumé :
|Instruction|Description|
|:---|:---|
|L1 + L2|Concaténer les deux listes L1 et L1|
|L * n|Dupliquer la liste L n fois|
|L.copy()|Retourner une copie de la liste L|
|len(L)|Retourner la longueur de la liste L|
|L.index(x)|Retourner l’indice de l’élément x dans la liste L|
|x in L|Retourner True si x existe dans L et False sinon|
|min(L)|Retourner la plus petite valeur des éléments de la liste L|
|max(L)|Retourner la plus grande valeur des éléments de la liste L|
|sum(L)|Retourner la somme des éléments de la liste L|
|L.append(x)|Ajouter l’élément x à la fin de la liste L|
|L.extend(M)|Ajouter les éléments de la liste M à la fin de la liste L|
|L.insert(i,x)|Ajouter l’élément x à la position i dans la liste L|
|L.remove(x)|Supprimer l’élément x de la liste L|
|del(L[i])|Supprimer l’élément d’indice i de la liste L|
|L.pop()|Supprimer et Retourner le dernier élément de la liste L|
|L.pop(i)|Supprimer et Retourner l’élément d’indice i de la liste L|
|L.clear()|Supprimer tous les éléments de la liste L|
|L.reverse()|Inverser la liste L en place|
|L.sort()|Trier la liste L en place|
|L.count(x)|Retourner le nombre d’occurrences de l’élément x dans la liste L|
|L[i,j,n]|Retourner une tranche de la liste L selon i, j et n|