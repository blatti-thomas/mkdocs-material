# Affichage en python
Pour afficher une valeur, on utilise la fonction print(). Cette fonction peut prendre plusieurs
paramètres, séparés par des virgules. Elle affiche les valeurs séparées par un espace et ajoute un
retour à la ligne à la fin.
```
print("Hello", "World")
```
Pour afficher la valeur d’une variable, nous allons utiliser le formatage f-string. Il suffit de préfixer
la chaîne de caractères avec la lettre f et d’entourer le nom de la variable avec des accolades {}.
```
name = "World"
print(f"Hello {name}")
```
Pour afficher un nombre à virgule flottante avec un nombre de décimales limité, on peut utiliser la
notation suivante: {variable:.xf} où x est le nombre de décimales souhaité.
```
pi = 3.141592653589793
print(f"Pi: {pi:.2f}")
```
La fonction print permet également d’afficher des listes, des tuples, des ensembles et
des dictionnaires.

# Chaîne

Par rapport au C, les chaînes de caractères sont des objets à part entière en Python. Elles possèdent
de nombreuses méthodes qui permettent de les manipuler. link
```
s = "Hello World"
print(s)        #affiche la string (s)

print(len(s))   # Affiche la longueur de la chaîne de caractères
 
print(s.upper())  #affiche la longueur de la string(s) (nombre de caractere)

s1 = "Hello"
s2 = "World"

full = s1 + " " + s2    #ajout de deux string pour en donner une seule (Hello + World)
print(full)             #affiche la string full
```

# Dictionnaires
Un dictionnaire est une collection d’objets non ordonnés, modifiables et indexés. Les dictionnaires
sont déclarés en utilisant des accolades {} et les éléments sont séparés par des virgules ,. Chaque
élément est constitué d’une clé et d’une valeur séparées par deux points :. Les clés doivent être#uniques et immuables (chaînes, nombres ou tuples).

Les méthodes suivantes sont disponibles pour les dictionnaires: 
```
clear(): supprime tous les éléments du dictionnaire

copy(): renvoie une copie du dictionnaire

get(): renvoie la valeur de la clé spécifiée

items(): renvoie une liste contenant une paire de tuples pour chaque paire clé-valeur

keys(): renvoie une liste contenant les clés du dictionnaire

pop(): supprime l’élément avec la clé spécifiée

popitem(): supprime le dernier élément inséré

update(): met à jour le dictionnaire avec les paires clé-valeur spécifiées

values(): renvoie une liste de toutes les valeurs du dictionnaire

french = {"un": "one", "deux": "two", "trois": "three"}

key = {1: "one", 2: "two", 3: "three"}
```
# Ensembles
Un ensemble est une collection d’objets non ordonnés et non indexés. Les ensembles sont déclarés
en utilisant des accolades {} et les éléments sont séparés par des virgules ,.
Les ensembles sont utilisés lorsque l’ordre des éléments n’a pas d’importance et que chaque élément
doit être unique. Les ensembles sont plus performants que les listes pour tester l’appartenance d’un
élément.
Il n’est pas possible d’accéder à un élément d’un ensemble par son index.

Les méthodes suivantes sont disponibles pour les ensembles: link
```
add(): ajoute un élément à l’ensemble

clear(): supprime tous les éléments de l’ensemble

copy(): renvoie une copie de l’ensemble

update(): ajoute plusieurs éléments à l’ensemble

pop(): supprime un élément de l’ensemble

remove(): Supprime un élément spécifique de l’ensemble

numbers = {1, 2, 3, 4, 5}
```

# Listes
Une liste est une collection d’objets ordonnés et modifiables. Les listes sont déclarées en utilisant
des crochets [] et les éléments sont séparés par des virgules ,. Une liste en python est polymorphe,
c’est-à-dire qu’elle peut contenir des éléments de différents types.

Une liste de méthodes utiles :
```
append(): ajoute un élément à la fin de la liste

insert(): insère un élément à une position donnée

remove(): supprime un élément de la liste

pop(): supprime un élément à une position donnée

clear(): supprime tous les éléments de la liste

index(): renvoie la position d’un élément

count(): renvoie le nombre d’éléments ayant une valeur donnée

sort(): trie les éléments de la liste

reverse(): inverse l’ordre des éléments de la liste

copy(): renvoie une copie de la liste


numbers = [1, 2, 3, 4, 5]
val = numbers[0] # val = 1
## Attention, accès au dernier élément
last = numbers[-1] # last = 5
poly = [1, 2.5, "Hello", True]
numbers.append(6) # numbers = [1, 2, 3, 4, 5, 6]
print(numbers)
```

# Slices
Les slices permettent d’extraire une partie d’une liste, d’un tuple ou d’une chaîne de caractères.
La syntaxe est la suivante: [start:stop:step] où - start est l’indice de départ, - stop est l’indice
de fin (non inclus) - step est le pas.
```
numbers = [1, 2, 3, 4, 5]
print(numbers[1:3])
print(numbers[1:])
print(numbers[:3])
print(numbers[::2])
print(numbers[::-1])
print(numbers[4:1:-1]) 
s = "Hello World"
print(s[0:3]) # Hel
print(s[-1]) # d
```
Il est possible d’utiliser des valeurs négatives pour start et stop. Dans ce cas, l’indice est compté
à partir de la fin de la liste.
```
numbers = [1, 2, 3, 4, 5]
print(numbers[:-3])
print(numbers[-3:-1])
print(numbers[-4:])
print(numbers[-2:])
```
Il est aussi possible d’utiliser des valeurs négatives pour step. Dans ce cas, la liste est parcourue
en partant de la fin.
```
numbers = [1, 2, 3, 4, 5]
print(numbers[::-1])
print(numbers[4:1:-1])
print(numbers[-1:-4:-1])
```

# Tuples
Un tuple est une collection d’objets ordonnés et non modifiables. Les tuples sont déclarés en#utilisant des parenthèses () et les éléments sont séparés par des virgules ,. Un tuple en python est
polymorphe, c’est-à-dire qu’il peut contenir des éléments de différents types.
```
numbers = (1, 2, 3, 4, 5)
val = numbers[0] # val = 1
```
Comme un tuple est non modifiable, il n’y a pas de méthode pour ajouter ou supprimer
des éléments.
L’instruction numbers[0] = 10 va générer une erreur.

# Types
```
int
i = 12

float
f = 12.0

complex
c = 12 + 0j

bool
b = True

string
s1 = "Hello World"

list
l = [1,2,3,4,5]

tuple
t = (1,2,3,4,5)

set
s2 = {1,2,3,4,5}

dict
d = {"a": 13, "b": 2, "c" : 3}
```
