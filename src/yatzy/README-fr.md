# Yatzy

## Présentation

Le jeu de yatzy est un jeu de dés simple.

Chaque joueur lance cinq dés à six faces.

Le joueur place le lancer dans une `category`, telle que `ones`, `twos`, `fives`, `pair`, `two pairs`, etc. (voir ci-dessous).

- Si le lancer est compatible avec la catégorie, le joueur obtient un score pour le lancer selon les règles.
- Si le lancer n'est pas compatible avec la catégorie, le joueur marque 0 pour le lancer.

Par exemple, si un joueur lance `5,6,5,5,2` et marque les dés dans la catégorie `fives`, il marquerait 15 (3 cinq).

Votre tâche consiste à marquer un `lancer` **DONNÉ** dans une `category` **DONNÉE**.
- Vous n'avez PAS à programmer le lancer de dés aléatoire.
- Vous n'avez PAS à programmer les relances (comme dans le vrai jeu).
- Vous ne jouez PAS en laissant l'ordinateur choisir la catégorie de score la plus élevée pour un lancer donné.

## Catégories de Yatzy et Règles de Score

### Catégorie `Chance` :
Le joueur marque la somme de tous les dés, peu importe ce qu'ils affichent.

Par exemple :
- `1,1,3,3,6` placés sur `chance` marquent 14 (1+1+3+3+6)
- `4,5,5,6,1` placés sur `chance` marquent 21 (4+5+5+6+1)

### Catégorie `Yatzy` :
Si tous les dés affichent le même nombre, le joueur marque 50 points.

Par exemple :
- `1,1,1,1,1` placés sur `yatzy` marquent 50
- `5,5,5,5,5` placés sur `yatzy` marquent 50
- `1,1,1,2,1` placés sur `yatzy` marquent 0

### Catégories `Ones`, `Twos`, `Threes`, `Fours`, `Fives`, `Sixes` :
Le joueur marque la somme des dés affichant un, deux, trois, quatre, cinq ou six, respectivement.

Par exemple :
- `1,1,2,4,4` placés sur `fours` marquent 8 (4+4)
- `2,3,2,5,1` placés sur `twos` marquent 4  (2+2)
- `3,3,3,4,5` placés sur `ones` marquent 0

### Catégorie `Pair` :
Si exactement deux dés affichent la même valeur, le joueur marque la somme des deux dés correspondants les plus élevés.

Par exemple, placés sur `pair` :
- `3,3,3,4,4` marquent 8 (4+4)
- `1,1,6,2,6` marquent 12 (6+6)
- `3,3,3,4,1` marquent 0
- `3,3,3,3,1` marquent 0

### Catégorie `Two pairs` :
Si exactement deux dés affichent la même valeur et exactement deux dés affichent une valeur différente, le joueur marque la somme de ces quatre dés.

Par exemple, placés sur `two pairs` :
- `1,1,2,3,3` marquent 8 (1+1+3+3)
- `1,1,2,3,4` marquent 0
- `1,1,2,2,2` marquent 0

### Catégorie `Three of a kind (Brelan)` :
S'il y a exactement trois dés avec le même numéro, le joueur marque la somme de ces dés.

Par exemple, placés sur `Three of a kind` :
- `3,3,3,4,5` marquent 9 (3+3+3)
- `3,3,4,5,6` marquent 0
- `3,3,3,3,1` marquent 0

### Catégorie `Four of a kind (Carré)` :
S'il y a exactement quatre dés avec le même numéro, le joueur marque la somme de ces dés.

Par exemple, placés sur `Four of a kind` :
- `2,2,2,2,5` marquent 8 (2+2+2+2)
- `2,2,2,5,5` marquent 0
- `2,2,2,2,2` marquent 0

### Catégorie `Small straight (Petite suite)` :
Placés sur `Small straight`, si les dés affichent :
- `1,2,3,4,5`, le joueur marque 15 (la somme de tous les dés).

### Catégorie `Large straight (Grande suite)` :
Placés sur `Large straight`, si les dés affichent :
- `2,3,4,5,6`, le joueur marque 20 (la somme de tous les dés).

### Catégorie `Full house (Full)` :
Si les dés sont deux d'un même nombre et trois d'un nombre différent, le joueur marque la somme des cinq dés.

Par exemple, placés sur `Full house` :
- `1,1,2,2,2` marquent 8 (1+1+2+2+2)
- `2,2,3,3,4` marquent 0
- `4,4,4,4,4` marquent 0
