# Devinette


Comme vous allez le voir, il peut être très facile de créer une devinette en python en quelques lignes de code.

Nous allons décortiquer l'exemple que je vous fournis ci dessous :

**1.1 Import de la librairie Random**

```
import random
```

**1.2 On imprime les instructions pour le joueur**

``` 
print("Bienvenue dans le jeu de devinette. Vous allez jouer deux parties de 5 fois")
```

**1.3 Création de la class devinette**

```
class devinette:

    def jouer(self, max_num):

        self.points = 0

        for jeu in range(0,5):

            chiffre = random.randint(1, max_num)
            dev = int(input("Veuillez choisir un chiffre entre 1 et {} ".format(max_num)))

            if chiffre == dev:
                self.points += 1
                print("bien joué!")

            else:
                print("L'ordinateur a choisi {}".format(chiffre))

        return self.points 
```

**1.4 Création des instances et commencement du jeu**

```
partie_1 = devinette()

partie_1.jouer(int(input('veuillez choisir le nombre maximal ')))

partie_2 = devinette()

partie_2.jouer(int(input('veuillez choisir le nombre maximal ')))

```


**1.4 # Résultat de la partie**

```
print("Voici le résultat: partie 1: {}, partie 2: {}".format(partie_1.points, partie_2.points))

if partie_1.points < partie_2.points:
    print("vous avez mieux joué lors du premier jeu")

elif partie_1.points == partie_2.points:

    print("vous avez les mêmes nombres de points")

else: print("vous avez mieux joué lors du second jeu")
```

