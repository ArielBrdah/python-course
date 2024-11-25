# 🚀 Introduction à Python – Guide Ludique et Pratique

## 🌟 1. Les Bases des Fonctions Python

### 📌 Affichage et interactions utilisateur
```python
print("Hello, Python!")  # Afficher un message
```

- **`print()`** : Sert à afficher des informations dans la console.

```python
nom = input("Quel est ton nom ? ")  # Récupérer des données de l'utilisateur
print("Bonjour, " + nom + " !")
```

- **`input()`** : Permet à l'utilisateur de saisir des données (toujours retournées sous forme de chaîne).

### 📌 Vérification du type d'une donnée
```python
age = 25
print(type(age))  # <class 'int'>
```

- **`type()`** : Indique le type d'une variable (int, str, float, etc.).

---

## 🌟 2. Conversion des types (Casting)
Python permet de convertir les types grâce à des fonctions appelées *casting* :
- **`int()`** : Convertir en entier.  
- **`float()`** : Convertir en décimal.  
- **`str()`** : Convertir en chaîne de caractères.

### Exemples :
```python
# Conversion de types
nombre = "42"
print(int(nombre))  # Convertir une chaîne en entier
print(float(nombre))  # Convertir une chaîne en nombre décimal

# Combinaison
age = 25
print("J'ai " + str(age) + " ans.")  # Conversion pour concaténation
```

---

## 🌟 3. Variables

### 📌 Règles pour nommer une variable :
1. Doit commencer par une lettre ou un underscore (`_`).  
2. Peut contenir des chiffres, mais ne doit **pas** commencer par un chiffre.  
3. Doit être unique dans un programme.

### Exemples :
```python
# Déclaration de variables
nom = "Alice"
age = 30
pi = 3.14

print(nom, age, pi)
```

---

## 🌟 4. Commentaires
Les commentaires sont ignorés par Python mais utiles pour documenter ton code :
```python
# Ceci est un commentaire sur une seule ligne.

"""
Ceci est un commentaire
multiligne.
"""
```

---

## 🌟 5. Conditions (IF/ELSE)

### 📌 Structure :
```python
if condition:
    # Bloc de code si la condition est vraie
elif autre_condition:
    # Bloc si l'autre condition est vraie
else:
    # Bloc si aucune condition n'est vraie
```

### Exemple :
```python
age = 20

if age >= 60:
    print("Vous êtes senior.")
elif age >= 18:
    print("Vous êtes adulte.")
else:
    print("Vous êtes mineur.")
```

---

## 🌟 6. Exercices pratiques

### 🔹 **Exercice 1 : Présentation**
Écrivez un programme qui demande à l'utilisateur :
- Son nom
- Son âge

Puis affiche : `Bonjour <nom>, vous avez <âge> ans.`

<details>
<summary>Solution</summary>

```python
nom = input("Quel est votre nom ? ")
age = input("Quel est votre âge ? ")
print("Bonjour " + nom + ", vous avez " + age + " ans.")
```
</details>

---

### 🔹 **Exercice 2 : Accès au cinéma**
Demandez à l'utilisateur son âge et dites-lui s'il peut regarder un film d'horreur (âge minimum : 13 ans). Si non, précisez combien d'années il doit attendre.

**Solution**

```python
age = int(input("Quel est votre âge ? "))

if age >= 13:
    print("Autorisé à voir le film.")
else:
    print("Accès interdit, il vous manque " + str(13 - age) + " ans.")
```

---

## 🌟 7. Tableaux (listes)

Les tableaux permettent de stocker plusieurs valeurs dans une seule variable.  
**Exemple :**
```python
fruits = ["pomme", "banane", "cerise"]

print(fruits[0])  # pomme
print(len(fruits))  # Nombre d'éléments : 3
```

### 📌 Obtenir le nombre d'éléments dans une liste
```python
nombres = [10, 20, 30]
print(len(nombres))  # 3
```

### 📌 Changer d'élément dans une liste existante:

```python
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
fruits[0] = "strawberry"
```

### 📌 Remplacer une sous liste d'élément par une autre list:

```python
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
fruits[0:2] = ["strawberry","grappe"]
```

### 📌 Insérer un élément dans une liste a l'index-K:

```python
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
fruits.insert(0,"watermelon")
print(fruits)

# ["watermelon", "apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
```


### 📌 Ajouter un élément a la fin d'une liste:

```python
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
fruits.append("peach")
print(fruits)

# ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango","peach"]
```

### 📌 Ajouter et concatener une liste, Ajouter une autre liste dans la liste actuelle:
```python
fruits = ['watermelon', 'strawberry', 'grappe', 'watermelon', 'cherry', 'orange', 'kiwi', 'melon', 'mango', 'peach']
fruits.extend( ["tomato","avocado"] )
print(fruits)
# ['watermelon', 'strawberry', 'grappe', 'watermelon', 'cherry', 'orange', 'kiwi', 'melon', 'mango', 'peach', 'tomato', 'avocado']
```

### 📌 Supprimer un element de la liste actuelle avec sa valeur:
```python
fruits = ['watermelon', 'strawberry', 'grappe']
fruits.remove("strawberry")
print(fruits)
# ['watermelon', 'grappe']
```


### 📌 Supprimer un element de la liste actuelle avec sa cle:
```python
fruits = ['watermelon', 'strawberry', 'grappe']
fruits.pop(1)
print(fruits)
# ['watermelon', 'grappe']
```

alternative

```python
fruits = ['watermelon', 'strawberry', 'grappe']
del fruits[1]
print(fruits)
# ['watermelon', 'grappe']
```

### 📌 Supprimer le derniere element de la liste actuelle:
```python
fruits = ['watermelon', 'strawberry', 'grappe']
fruits.pop()
print(fruits)
# ['watermelon', 'strawberry']
```

### 📌 Supprimer une liste:
```python
fruits = ['watermelon', 'strawberry', 'grappe']
del fruits
print(fruits)
# Not Defined
```

### 📌 Vide une liste:
```python
fruits = ['watermelon', 'strawberry', 'grappe']
fruits.clear()
print(fruits)
# result: []
```


### 📌 Boucler sur un tableau sur chaque valeur:
```python
fruits = ['watermelon', 'strawberry', 'grappe']
# foreach
for fruit in fruits:
    print("Le fruit actuelle est le: "+fruit)
# result: []
```


### 📌 Boucler sur un tableau a partir de l'index:
```python
fruits = ['watermelon', 'strawberry', 'grappe']
# for
for index in range(0,len(fruits)):
    print("Le fruit actuelle est le: "+fruits[index])
# result: []
```


"salut" = ["s","a","l","u","t"]

### 📌 Trier un tableau numeric:
```python
nums = [9,6,3,6,7]
nums.sort()
print(nums)
# result: [3,6,6,7,9]
```

### 📌 Recuperer l'index d'un élément dans une liste
```python
nombres = [10, 20, 30]
print(nombres.index(20))  # 1
```

### 📌 Copy d'une liste en profondeur
ERREUR A NE PAS FAIRE
```python
# un tableau qui pointe sur le meme tableau manipule les memes donnees
# manipuler (modifier un element, supprimer un element)
nombres = [10, 20, 30]
nombres_2 = nombres
nombres_2[0] = 1000
print(nombres) # [1000, 20, 30]
print(nombres_2) # [1000, 20, 30]
```
Voici comment faire une copie de tableau pour le manipuler sous une autre forme.

```python
nombres = [10, 20, 30]
nombres_2 = nombres.copy()
nombres_2[0] = 1000
print(nombres)  # [10, 20, 30]
print(nombres_2)  # [1000, 20, 30]
```

### 📌 Extraire une liste d'élément a partir d'une autre liste
```python
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]

nouvelle_list_1 = fruits[2:5] # ["cherry", "orange", "kiwi"]
nouvelle_list_2 = fruits[2:] # ["cherry", "orange", "kiwi", "melon", "mango"]
nouvelle_list_3 = fruits[:2] # ["apple", "banana"]
```

### 📌 Verifier si un élément existe dans la liste:
```python
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]

if "apple" in fruits:
    print("Ce fruit existe dans notre liste")
else:
    print("Ce fruit n'existe pas dans notre liste")
```


```python
fruits = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]

user_input = input("Which fruits is in the list? ")
if user_input.lower() in fruits:
    print("Ce fruit existe dans notre liste")
else:
    print("Ce fruit n'existe pas dans notre liste")
```

### 📌 Itération dans une liste :
```python
for fruit in fruits:
    print(fruit)
```
### 📌 Recap: toutes les fonctions possible sur une liste:
```python
**Method**	**Description**
append()	# Ajout element a la fin de la liste
clear()	    # Vide la liste
copy()	    # Retourne une copy de la liste
count()	    # Recupere le nombre de fois ou un element est present dans le tableau
extend()	# Combine deux liste
index()	    # Retourne l'index d'une valeur
insert()	# Ajoute un element a la position souhaite
pop()	    # Supprime un element a une position
remove()	# Supprime un element qui matche la valeur
reverse()	# Renverse l'ordre de la liste
sort()	    # Trie une liste, et la garde trier
```
---

## 🌟 8. Fonctions

### 📌 Définir une fonction :
```python
def saluer(nom):
    print("Bonjour, " + nom + " !")
```

### 📌 Appeler une fonction :
```python
saluer("Alice")  # Bonjour, Alice !
```

---

## 🌟 9. Bibliothèques
Une bibliothèque est un ensemble de fonctions prédéfinies que vous pouvez importer dans votre code.

### 📌 Exemple avec `random` :
```python
import random

nombre_aleatoire = random.randint(1, 10)  # Générer un nombre entre 1 et 10
print(nombre_aleatoire)
```

---

## 🌟 10. Tuples (listes constantes)

### 📌 Simple declaration
```python
fruits = ['banana','melon','watermelon']
fruits_permanents = tuple(fruits[0:2])
# fruits_permanents est une variable de type list et constant => tuple (inalterable)
```

### 📌 Destructuring - Destructuration
```python
fruits = ['banana','melon','watermelon']
fruits_permanents = tuple(fruits[0:2])
(banana, melon) = fruits_permanents
print(banana) # banana

(x, y) = fruits_permanents
print(x) # banana
```

## 🌟 10. Sets (listes sans doublon)
Cette structure de donnee ne permet pas les doublons.

### 📌 Simple declaration
```python
fruits = ['banana','peach','mango','banana']
fruits_once = set(fruits)
print(fruits_once) # ('banana','peach','mango')
```
### 📌 Ajout
```python
mon_set = {1, 2, 3}
mon_set.add(4)  # Ajoute 4 au set
print(mon_set)  # {1, 2, 3, 4}
```
### 📌 Suppression
```python
mon_set = {1, 2, 3}
mon_set.remove(2)  # Supprime 2
print(mon_set)  # {1, 3}
```

## 🌟 11. Dictionary (liste cle : valeur)

### 📌 Simple declaration
```python
# un tableau avec cle et valeur
car = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
car = {year: 1969}
car = dict(year:1969
)
```

### 📌 Acces a une valeur (dictionnaire)
```python
print(car['brand']) # Ford
print(car.get('brand')) # Ford
```

### 📌 Recuperer la liste des cles (dictionnaire)
```python
car = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
k = car.keys()
print(k) # ['brand','model','year']
```

### 📌 Recuperer la liste des valeurs (dictionnaire)
```python
v = car.values()
print(v) # ["Ford","Mustang","1969"]
```

### 📌 Modifier une valeur (dictionnaire)
```python
car = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
car["brand"] = "Mitsubichi"
print(car.values()) # ["Mitsubichi","Mustang","1969"]
```

### 📌 Modifier plusieurs valeurs en une fois (dictionnaire)
```python
car = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
modif = {"brand":"Mitsubichi","year": 2020}
car.update(modif)
# car.update({"brand":"Mitsubichi","year": 2020})
print(car.values()) # ["Mitsubichi","Mustang","2020"]
```

### 📌 Supprimer un element a partir d'une cle (dictionnaire)
```python
car.pop('model')
# { "year": 2020, "brand": "Mitsubichi"}
```

### 📌 Supprimer le derniere element (dictionnaire)
```python
car = {
    "brand": "Ford",
    "model": "Mustang",
    "year": 1964
}
car.popitem()
# { "brand": "Ford", "model": "Mustang" }
```



# Pendu
# pre-requis
# a. banque de mot, selectionner un mot au hasard
# b. l'utilisateur a 5 essaies

# 1. utilisateur propose une lettre
# 2. verifier si cette lettre existe dans le mot
# 3. S'il a trouve alors placer les lettres dans le mot
# 4. Sinon enlever une vie
# 5. verifier s'il a trouver tout les lettres du mot

import random

banque_de_mots = [
    "amour", "bonheur", "château", "danse", "étoile",
    "fleur", "guitare", "histoire", "imaginaire", "joie",
    "lumière", "montagne", "nature", "océan", "papillon",
    "quartz", "rêve", "soleil", "trésor", "univers",
    "vent", "wagon", "xylophone", "yacht", "zèbre"
]

guess_word = random.choice(banque_de_mots)