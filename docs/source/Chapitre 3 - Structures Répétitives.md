Une **structure répétitive** ou **boucle** permet de répéter une portion de code.
***
# 1. La Boucle while
Syntaxe :
```Python
while Condition :
    Bloc d'Instructions
```
Tant que la **Condition** est vraie le bloc d'instructions s'exécute.

La boucle se **répète** jusqu'à ce que la Condition soit fausse.

Exemple :
```Python
i=1
while i<=10 :
    print("5 x",i,"=",5*i)
    i=i+1
```
Output :
```Python
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```
***
# 2. La Boucle for
Syntaxe :
```Python
for élément in séquence :
    Bloc d'Instructions
```
La séquence est **parcourue** élément par élément, par élément.

On utilise la boucle for lorsqu'on connaît le nombre d'itérations.

Exemple :
```Python
for i in range(1,11):
    print("5 x",i,"=",5*i)
```
Output :
```Python
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```
La fonction `range()` permet de générer une séquence de nombre selon `début`, `fin` et `pas` :

`range(début, fin, pas)`, le `début` est par défaut 0, `pas` est par défaut 1.
***
# 3. Les Instructions break, continue
## 3.1. L’Instruction break
L'instruction `break` permet de stopper l’exécution d’une boucle (while ou for), sous une certaine condition.

Exemple :
```Python
for i in range(1,100):
    print(i)
    if i==5:
        break
```
Output :
```Python
1
2
3
4
5
```
## 3.2. L’Instruction continue
L'instruction `continue` permet de sauter à l'itération suivante, sans exécuter la suite du bloc d'instructions de la boucle courante.

Exemple :
```Python
for i in range(6):
    if i==3 :
        continue
    print(i)
```
Output :
```Python
0
1
2
4
5
```
***
# 4. Boucles Conditionnées
Les `boucles conditionnées` permettent de répéter un bloc d'instructions jusqu'à ce qu'une condition spécifique soit satisfaite.

Exemple :
```Python
i=1
while True :
    if i>10 :
        break
    print(i)
    i+=2
```
Output :
```Python
1
3
5
7
9
```
***
# 5. Boucles Imbriquées
Une `boucle imbriquée` est le fait d’avoir une boucle à l’intérieur d’une autre.

Exemple :
```Python
for i in range(1,11):
    print("Table de multiplication de",i,":")
    for j in range(1,11):
        print(i,"x",j,"=",i*j)
```
Output :
```Python
Table de multiplication de 1 :
1 x 1 = 1  
1 x 2 = 2  
1 x 3 = 3  
1 x 4 = 4  
1 x 5 = 5  
1 x 6 = 6  
1 x 7 = 7  
1 x 8 = 8  
1 x 9 = 9  
1 x 10 = 10
Table de multiplication de 2 :
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20
Table de multiplication de 3 :
3 x 1 = 3
3 x 2 = 6
3 x 3 = 9
3 x 4 = 12
3 x 5 = 15
3 x 6 = 18
3 x 7 = 21
3 x 8 = 24
3 x 9 = 27
3 x 10 = 30
Table de multiplication de 4 :
4 x 1 = 4
4 x 2 = 8
4 x 3 = 12
4 x 4 = 16
4 x 5 = 20
4 x 6 = 24
4 x 7 = 28
4 x 8 = 32
4 x 9 = 36
4 x 10 = 40
Table de multiplication de 5 :
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
Table de multiplication de 6 :
6 x 1 = 6
6 x 2 = 12
6 x 3 = 18
6 x 4 = 24
6 x 5 = 30
6 x 6 = 36
6 x 7 = 42
6 x 8 = 48
6 x 9 = 54
6 x 10 = 60
Table de multiplication de 7 :
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
7 x 4 = 28
7 x 5 = 35
7 x 6 = 42
7 x 7 = 49
7 x 8 = 56
7 x 9 = 63
7 x 10 = 70
Table de multiplication de 8 :
8 x 1 = 8
8 x 2 = 16
8 x 3 = 24
8 x 4 = 32
8 x 5 = 40
8 x 6 = 48
8 x 7 = 56
8 x 8 = 64
8 x 9 = 72
8 x 10 = 80
Table de multiplication de 9 :
9 x 1 = 9
9 x 2 = 18
9 x 3 = 27
9 x 4 = 36
9 x 5 = 45
9 x 6 = 54
9 x 7 = 63
9 x 8 = 72
9 x 9 = 81
9 x 10 = 90
Table de multiplication de 10 :
10 x 1 = 10
10 x 2 = 20
10 x 3 = 30
10 x 4 = 40
10 x 5 = 50
10 x 6 = 60
10 x 7 = 70
10 x 8 = 80
10 x 9 = 90
10 x 10 = 100
```
Remarque :
|Affectation|Équivalent|
|:---:| :---: |
|i += 1|i=i+1|
|i -= 1|i=i-1|
|i *= 1|i=i*1|
|i /= 1|i=i/1|
|i //= 1|i=i//1|
|i %= 1|i=i%1|
|i **= 1|i=i**1|
|ect...|ect...|