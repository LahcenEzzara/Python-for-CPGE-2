# 1. Notion de chaînes de caractères
Une **chaîne de caractères** est une structure de donnée en particulier, c’est une séquence de caractères qui est utilisée pour représenter du texte.

Exemple :
```Python
information = "Python est un langage de programmation de haut niveau"
```
# 2. Création de chaîne de caractères
Pour créer une chaîne de caractères, on peut assigner une série de caractères à une variable en utilisant des guillemets simples `'...'` ou des guillemets doubles `"..."`.

Exemple :
```Python
Remarque1 = 'Python est un langage de programmation'

Remarque2 = "Python est un langage de programmation"
```
# 3. Parcours d’une chaîne de caractères
## 3.1. Principe d’indexage
Comme les listes, les chaînes de caractères sont **indexées** par indices positifs et aussi négatifs.

Exemple :
```Python
Hello  = "Bonjour Python!"
```
Le premier `n` est d'indice 2 et dernier d’indice -1.
## 3.2. Accès aux éléments d’une chaîne de caractères
On peut accéder à un élément (caractère) en se basant sur son indice.

Syntaxe :
```Python
chaine[indice]
```
Exemple :
```Python
Hello = "Bonjour Python!"

# Accéder au caractère 'j'
print(Hello[3])
```
Output :
```Python
j
```
Remarque :

Les chaînes de caractères sont des structures de donnes **immutables** cad on ne peut pas les modifier après leur création.

Exemple :
```Python
Hello  = "Bonjour Python!"

Hello[0] = 'A'
```
Output :
```Python
TypeError: 'str' object does not support item assignment
```
## 3.3. Parcours d’une chaîne de caractères par indice
Exemple :
```python
Hello = "Bonjour Python!"

# On remarque que cette chaîne est de longueur : 15

for i in range(15):
    print(Hello[i])
```
Output:
```Python
B
o
n
j
o
u
r

P
y
t
h
o
n
!
```
## 3.4. Parcours d’une chaîne de caractères par élément
Exemple :
```Python
Hello = "Bonjour Python!"

# On remarque que cette chaîne est de longueur : 15

for x in Hello :
    print(x)
```
Output:
```Python
B
o
n
j
o
u
r

P
y
t
h
o
n
!
```
# 4. Concaténation de chaînes de caractères

Syntaxe :
```Python
nouvelle_chaine = chaine1 + chaine2
```
Exemple :
```Python
Hel = "Bonjour"
lo = "Python"
Hello = Hel + lo
print(Hello)
```
output :
```
BonjourPython
```
# 5. Duplication d’une chaîne de caractère

Exemple :
```Python
Hello = 'Hello'
Hello3 = Hello*3
print(Hello3)
```
Output :
```Python
HelloHelloHello
```
# 6. Longueur d’une chaîne de caractère
La longueur d’une chaîne de caractères est son nombre d’éléments.

La fonction len() renvoie la longueur de la chaîne de caractères qu’on lui passe en paramètre.

Syntaxe :
```Python
len(chaine)
```
Exemple :
```Python
Hello = 'Bonjour'

print(len(Hello))
```
Output :
```Python
7
```
# 7. Recherche d’éléments dans une chaîne de caractères
## 7.1. Recherche d’indice d’un caractère dans une chaîne de caractères
Syntaxe :
```Python
chaine.index(caractere)
```
Exemple :
```Python
Hello = 'Bonjour'

i=Hello.index('B')
print(i)
```
Output :
```Python
0
```
## 7.2. Recherche d’une chaîne dans une chaîne de caractères
La méthode `find()` retourne l'indice de la première occurrence d'une sous-chaîne dans une chaîne donnée et si la sous-chaîne n'est pas trouvée dans la chaîne, la méthode renvoie -1.

Syntaxe :
```Python
chaine.find(chaîne2)
```
Exemple 1 :
```Python
Hello = 'Bonjour'

print(Hello.find("jour"))
```
Output :
```Python
3
```
Exemple 2 :
```Python
Hello = 'Bonjour'

print(Hello.find("soir"))
```
Output :
```Python
-1
```
# 8. Nombre d’occurrences d’une sous-chaîne dans d’une chaîne de caractères
La méthode `count()` permet de retourner le nombre d’occurrences d’une sous-chaîne dans d’une chaîne de caractères.

Syntaxe :
```Python
nombre = chaine.count(sous_chaîne)
```
Exemple :
```Python
Hello = "Bonjour Python"
n = Hello.count("on")
print(n)
```
output :
```Python
2
```
# 9. Changement de casse de chaîne de caractèrere
## 9.1. Minuscule
La méthode `lower()` est permet de convertir une chaîne de caractères en minuscules en retournant une nouvelle chaîne de caractères qui est une copie de la chaîne d'origine, mais avec toutes les lettres en minuscules.

Syntaxe :
```Python
nouvelle_chaine = chaine.lower()
```
Exemple :
```Python
Hello = 'Bonjour PYTHON'
Hello_Min = Hello.lower()
print(Hello_Min)
```
Output :
```Python
bonjour python
```
## 9.2. Majuscule
La méthode `upper()` permet de convertir une chaîne de caractères en majuscule en retournant une nouvelle chaîne de caractères qui est une copie de la chaîne d'origine, mais avec toutes les lettres en majuscules.

Syntaxe :
```Python
nouvelle_chaine = chaine.upper()
```
Exemple :
```Python
Hello = 'Bonjour python'
Hello_Maj = Hello.upper()
print(Hello_Maj)
```
Output :
```Python
BONJOUR PYTHON
```
## 9.3. Capitalisation

La méthode `capitalize()` permet convertir la première lettre d'une chaîne de caractères en majuscule et toutes les autres lettres en minuscules en retournant une nouvelle chaîne de caractères qui est une copie de la chaîne d'origine mais avec les modifications citées.

Syntaxe :
```Python
nouvelle_chaine = chaine.capitalize()
```
Exemple :
```Python
Hello = 'bonJoUr PyThon'
newhello = Hello.capitalize()
print(newhello)
```
Output :
```Python
Bonjour python
```
# 10. Conversion d'un nombre en chaîne de caractères
On peut utiliser la fonction ``str()`` pour convertir un nombre en une chaîne de caractères.

Syntaxe :
```Python
chaine = str(nombre)
```
Exemple :
```Python
age = 32
age_chaine = str(age)
print(type(age_chaine))
```
Output :
```Python
<class 'str'>
```
# 11. Conversion d'une chaîne de caractères en une liste
La méthode `split()` retourne une liste de sous-chaînes d’une chaîne de caractères, elle découpe la chaîne en plusieurs éléments, en basant sur séparateur par défaut n'importe quelle combinaison d'espace blanc.

Syntaxe :
```Python
liste = chaine.split()
```
Exemple 1 :
```Python
information = "Python est un langage de programmation de haut niveau"
Mots = information.split()
print(Mots)
```
Output :
```Python
['Python', 'est', 'un', 'langage', 'de', 'programmation', 'de', 'haut', 'niveau']
```
Exemple 2 :
```Python
information = "Python,est un langage de programmation,de haut niveau"
Mots = information.split(',')
print(Mots)
```
Output :
```Python
['Python', 'est un langage de programmation', 'de haut niveau']
```
# 12. Conversion d'une liste de caractères en chaîne de caractères
La méthode `join()` permet de joindre une liste de chaînes de caractères en une seule chaîne de caractères, en spécifiant un séparateur entre les éléments de la liste.

Syntaxe :
```Python
chaine = "separateur".join(liste)
```
Exemple 1 :
```Python
Mots = ['Python', 'est', 'un', 'langage', 'de', 'programmation', 'de', 'haut', 'niveau']
information = ' '.join(Mots)
print(information)
```
Output :
```Python
Python est un langage de programmation de haut niveau
```
Exemple 2 :
```Python
Mots = ['Python', 'est', 'un', 'langage', 'de', 'programmation', 'de', 'haut', 'niveau']
information = ','.join(Mots)
print(information)
```
Output :
```Python
Python,est,un,langage,de,programmation,de,haut,niveau
```
# 13. Remplacement d’une sous-chaîne par une autre
La méthode `replace()` permet de remplacer toutes les occurrences d'une sous-chaîne donnée dans une chaîne de caractères par une autre sous-chaîne donnée en retournant une nouvelle chaîne de caractères qui est une copie de la chaîne d'origine avec les modifications citées.

Syntaxe :
```Python
nouvelle_chaine = chaîne.replace(sous_chaine1,sous_chaine2)
```
Exemple :
```Python
information = "PHP est un langage de programmation, PHP est de haut niveau"
remarque = information.replace('PHP','Python')
print(remarque)
```
Output :
```Python
Python est un langage de programmation, Python est de haut niveau
```
# 14. Suppression des espaces et des caractères de saut de ligne des bords d’une chaîne de caractères
La méthode `strip()` permet de supprimer les espaces et les caractères de saut de ligne en début et en fin de chaîne de caractères.

Syntaxe :
```Python
nouvelle_chaine = chaine.strip()
```
Exemple :
```Python
Hello = " Bonjour Python\n"
New_Hello = Hello.strip()
print(Hello)
print(New_Hello)
```
Output :
```Python
 Bonjour Python

Bonjour Python
```
# 15. Tranchage
Le **Tranchage** d’une chaîne de caractères permet de sélectionner une partie d'une liste en utilisant des indices, en faisant extraire une partie de la liste originale.

Syntaxe :
```Python
nouvelle_chaine = chaine[indice_debut:indice_fin:pas]
```
Exemple :
```Python
Hello = "Bonjour Python"

Nom = Hello[8:]
print(Nom)
```
Output :
```Python
Python
```

Résumé :

|Instruction|Description|
|:---|:---|
|ch1 + ch2|Concaténation des deux chaines ch1 et ch2|
|ch * n|Duplication de la chaine ch n fois|
|ch[i]|Accéder à l’élément d’indice i dans la chaine ch|
|len(ch)|Renvoi de la langueur de la chaine ch|
|ch.index(x)|Renvoi de l’indice de l’élément x dans la chaine ch|
|ch.find(sch)|Recherche de la sous-chaine sch dans la chaine ch|
|ch.count(sch)|Renvoi du nombre d’occurrences de sch dans la chaine ch|
|ch.lower()|Renvoi de ch en minuscule|
|ch.upper()|Renvoi de ch en majuscule|
|ch. capitalize()|Capitalisation de la chaine ch|
|str(n)|Conversion du nombre n en chaine|
|ch.splite()|Conversion de la chaine ch en liste|
|ch.join(l)|Conversion de la liste L en chaine|
|ch.replace(ch1,ch2)|Renvoi d’une chaine dont on a remplacé la sous-chaine ch1 en ch2 dans la chaine ch|
|ch.strip()|Suppression d’espaces et caractères de saut de ligne de la chaine ch|
|ch[i :j :pas]|Tranche de ch|