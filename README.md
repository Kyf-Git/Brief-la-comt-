# les types de variables :

<br/>

**Les variables** se divisent en plusieurs **types**, permettant ainsi de stocker des données différentes selon le besoin.
Lors de la **déclaration** d'une variable, il faut spécifier son type. Toute variable, en plus de son nom, se doit d'avoir un type. 

<br/>

## Les types primitifs :


#### boolean : 
ne prend en compte que 2 valeurs, **true** et **false**.
#### char (character) : 
permet de stocker la valeur Unicode d'un caractère (entre '\u0000' et '\uffff').

<br/>

### Les types entier :

#### byte : 
nombre entier relatif très court (entre -128 et 127).
#### short : 
nombre entier relatif court (entre -32 768 et 32 767).
#### int (integrer) : 
nombre entier relatif (entre -2 147 483 648 et 2 147 483 647).
#### long : 
nombre entier relatif court (entre -32 768 et 32 767).

<br/>

### Les types flottants :
**float** et **double** se distinguent par la taille de leur représentation, et par conséquent par la précision et l'étendue des valeurs.

#### float : 
nombre décimal, permettant la virgule (entre − 3 , 4.10^38 et 3 , 4.10^38).
#### double : 
nombre décimal, permettant la virgule (entre − 1 , 7.10^308 et 1 , 7.10^308).

<br/>

## Affectation :

Une **affectation** équivaut à mettre une valeur dans une variable.
Comment affecter la valeur d'une variable?

* taper une valeur littéral après le signe égal : x = 12; test = true;
* affecter la valeur d'une variable à une autre : y = x;
* employer une expression combinant les deux : x = y + 3;


#### Exemples : 
```java
int taille = 32;
char initiale = 'j'; // ne pas oublier les ' '
double d = 431.123; // le point joue le rôle de la virgule.
boolean test; 
test = true; // les booléens et les entiers sont différents.
float = 32.4f; // le f différencie les floats des doubles.
```






