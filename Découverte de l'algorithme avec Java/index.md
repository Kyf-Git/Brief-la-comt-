# <p style="text-align:center;"> Découverte de l'algorithme avec <img src="https://upload.wikimedia.org/wikipedia/fr/thumb/2/2e/Java_Logo.svg/483px-Java_Logo.svg.png" widht="100px" height="100px"></p>

<p style="text-align:right;"> Par Frank, Gino, Hamza, Vivien.</p>

1. [La notion de variable](#variable-notion)
2. [Les types de variable](#variable-type)
3. [Les mots clés](#mot-cle)
4. [Les opérateurs](#operateurs)
5. [L'évaluation](#evaluation)
6. [L'assignation](#assignation)
7. [L'instruction](#instruction)
8. [Le bloc d'instructions](#bloc-instruction)
9. [Le commentaire](#commentaire)
10. [La condition](#condition)
11. [La boucle](#boucle)
12. [La fonction](#fonction)
13. [Les paramètres](#parametre)

# <a id="variable-notion">La notion de variable</a>

## Définition

Une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)"><a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a></a> est un symbole qui associe un nom à une valeur.

En informatique, cette valeur est stockée en mémoire dans l'attente d'un résultat.

En <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>, les <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> sont typées. Elles peuvent être déclarée comme étant un chiffre, un caractère, un chaîne de caractères etc. La façon dont elle seront traitées découlera de ce type.

La longueur d'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> est illimitée mais le compilateur ne prendra en compte que les 247 premiers caractères.

Elle doit aussi respecter certaines règles: 

- Elle ne peut comporter que des lettres, des chiffres. `_` et `$` sont autorisés mais déconseillés
- Elle ne doit pas commencer par un chiffre
- Elle ne doit pas comporter d'espace

Les noms de <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> sont sensibles à la casse (majusculte/minuscule). la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> `bonjour` ne sera  pas traitée comme `BonJouR`.

Les <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a> s'écrivent en <a href="https://fr.wikipedia.org/wiki/Camel_case">CamelCase</a> : `maVariable`, `DireBonjour` ...


## La déclaration des <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a>:

Pour pouvoir utiliser une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>, il faut la définir, c'est-à-dire lui donner un nom, mais surtout un type de donnée à stocker afin qu'un espace mémoire conforme au type de donnée qu'elle contient lui soit réservé.
Une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> se déclare de la façon suivante :   type nomDeVariable ;

Ou bien s'il y a plusieurs <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> du même type :  type nomDeVariables ; ou nom_De_Variables2 ;

-   <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a> impose que les <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> soient impérativement déclarées avant d'être utilisée.
-   <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a> permet de définir une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> à n'importe quel endroit du code.                 

## Affectation d'une donnée à une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>:
La déclaration d'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> réserve un emplacement mémoire où stocker la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>, et une valeur par défaut (généralement 0, null ou false), pour modifier cette valeur par défaut, il faut faire une affectation, c'est-à-dire préciser la donnée qui va être stockée à l'emplacement mémoire qui a été réservé.  

Pour cela on utilise l'opérateur d'affectation "`.`" :
nomDeVariable = valeur;
Il est aussi possible d'initialiser les valeurs lors de leurs déclarations.
type nomDeVariable = valeur;

Exemple : Pour stocker le caractère B dans une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> que l'on appellera  _caractere_, il faudrait écrire :  

char caractere = 'B';
Ce qui signifie _"stocker la valeur Unicode de la lettre B dans la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> nommée 'caractere'_.

## Portée (visibilité) des <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> :

Selon l'endroit où on déclare une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>, celle-ci pourra être accessible (visible) de partout dans le code ou bien que dans une portion confinée de celui-ci (à l'intérieur d'une méthode par exemple), on parle de  _portée_  d'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>.  

Lorsqu'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> est déclarée directement dans la classe, c'est-à-dire à l'extérieur de toute méthode, elle sera accessible dans toute la classe. On parle alors de  _champ_  de la classe (fields, en anglais). Elle représente l'état de l'objet courant (ou avec le mot clé static, l'état de la classe elle même).  

Lorsque l'on déclare une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> à l'intérieur d'un bloc d'instructions (entre des accolades), sa portée se restreint à l'intérieur de ce bloc (dans les lignes qui suit sa déclaration), on parle alors de <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> locale.  

Il est interdit d'avoir deux <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> de même nom si elles ont une portée commune. Il serait alors impossible de les distinguer...

## Définitions de constantes:

Une constante est une donnée dont la valeur est inchangeable lors de l'exécution d'un programme. Le mot clé _final_ permet de faire cela. Toutefois on ne peut véritablement parler de constantes en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a> que pour les **types** primitifs, car pour un objet le mot clé final impose seulement que la référence de l'objet n'est pas modifiable, mais les champs de l'objets peuvent être modifiés malgré tout.  
  
Par convention, et pour les distinguer des <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a>, les constantes sont écrites entièrement en majuscules, et le caractère _ peut être utilisé pour séparer deux mots.

final int MA_CONSTANTE =12

aura pour effet de définir une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> de type _int_ possèdant la valeur 12 et ne pouvant pas être modifiée dans la suite du code, auquel cas le compilateur générera une erreur...

# <a id="variable-type"></a>Les **types** de variables</a> :

**Les <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a>** se divisent en plusieurs **types**, permettant ainsi de stocker des données différentes selon le besoin.
Lors de la **déclaration** d'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>, il faut spécifier son type. Toute <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>, en plus de son nom, se doit d'avoir un type. 

## Les **types** primitifs :

Il existe 8 **types** primitifs en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>

`boolean` : ne prend en compte que 2 valeurs, **true** et **false**.

`char` : chractère au format unincode (compris entre `\u0000` et `\uffff`).

## Les entiers :

`byte` : nombre entier relatif très court (entre `-128` et `127`).

`short` : nombre entier relatif court (entre `-32 768` et `32 767`).

`int` : nombre entier relatif (entre `-2 147 483 648` et `2 147 483 647`).

`long` : nombre entier relatif court (entre `-32 768` et `32 767`).

## Les **types** flottants :
`float` et `double` se distinguent par la taille de leur représentation, et par conséquent par la précision et l'étendue des valeurs.

`float` : nombre décimal, permettant la virgule (entre − 3 , 4.10^38 et 3 , 4.10^38).

`double` : nombre décimal, permettant la virgule (entre − 1 , 7.10^308 et 1 , 7.10^308).

## Affectation :

Une **affectation** équivaut à mettre une valeur dans une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>.
Comment affecter la valeur d'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>?

* taper une valeur littéral après le signe égal : x = 12; test = true;
* affecter la valeur d'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> à une autre : y = x;
* employer une expression combinant les deux : x = y + 3;

### Exemples : 
```java
int taille = 32;
char initiale = 'j'; // ne pas oublier les ' '
double d = 431.123; // le point joue le rôle de la virgule.
boolean test; 
test = true; // les booléens et les entiers sont différents.
float = 32.4f; // le f différencie les floats des doubles.
```

# <a id="mot-cle"></a> Les mots-clés:

Les <a href="https://thierry-leriche-dessirier.developpez.com/tutoriels/java/mots-cles-java/">mots-clés</a> sont des termes spécifiques au langage de programmation, certains sont utilisables par plusieurs langages et d'autres spécifiques à un langage.

On trouve plus de 50 mots clés qui ont les usages propres en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>.

On ne peut les utiliser que dans un contexte précis et il est impossible de les déclarer en comme noms de classes ou <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a>. 

On retrouve différents **types** de <a href="https://thierry-leriche-dessirier.developpez.com/tutoriels/java/mots-cles-java/">mots-clés</a> pour déclarer des objets, des <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a>, des états, des branchements et encore des exceptions.

Déclarer des objets:

 `class`, `interface`, `implements`, `enum`, `import`, `this`, `abstract`, `extends`, `package`, `super`, `native`.

Déclarer des **types**:

`boolean`, `char`, `int`, `float`, `long`, `short`, `double`, `byte` & `void`.

Déclarer des états:

 `const` , `false`, `true`, `static`, `null`, `volatile`, `new`, `transient`, `strictfp`.

Déclarer des boucles:

`do`, `for`, `goto`, `while`, `continue`.

Déclarer des branchements:

 `if`, `else`, `return`, `break`, `assert`, `switch`, `synchronized`, `default`, `case`, `instanceof`.

Déclarer des exceptions:

 `throw`, `throws`, `try`, `catch`, `finally`


# <a id="operateurs"></a> Les opérateurs

Les opérateurs sont des symboles permettant de manipuler et d’effectuer des operations mathématiques sur des <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a>.


## Les opérateurs de calcul  

Permettent d'effectuer des opérations mathématiques simples sur/entre des <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a>

| Opérateur | Effet                                                                      |
| --------- | -------------------------------------------------------------------------- |
| **+**     | addition                                                                   |
| **-**     | soustraction                                                               |
| *         | multiplication                                                             |
| **/**     | division                                                                   |
| **%**     | modulo (rends le reste de la division)                                     |
| **=**     | affectation  (à ne pas confondre avec **==**, l'opérateur de vérification) |

## Les opérateurs d'assignation

Permet d'effectuer une opération de calcule à une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> et d'affecter son resultat à cette même <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> 
(exemple: 
```java
 x = x+1
 ```
  pourra s'écrire 
  ```java
  x += 1
  ```

| Opérateur | Effet                                                                                                                              |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **+=**    | additionne deux valeurs et stocke le résultat dans la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> |
| **-=**    | soustrait deux valeurs et stocke le résultat dans la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>  |
| ***=**    | multiplie deux valeurs et stocke le résultat dans la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>  |
| **/=**    | divise deux valeurs et stocke le résultat dans la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>     |
| **%=**    | module deux valeurs et stocke le résultat dans la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>     |

## Les opérateurs d'incrémentation

Permet d'augmenter ou diminuer d'une unité une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> (utile pour les boucles par exemple)

| Opérateur | Effet                                                                                                |
| --------- | ---------------------------------------------------------------------------------------------------- |
| **++**    | augmente d'une unité la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> |
| **--**    | diminue d'une unité la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>  |

## Les opérateurs de comparaison

Permettent d'effectuer des opérations de comparaison entre des <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a>, retournent  TRUE or FALSE

| Opérateur | Effet               |
| --------- | ------------------- |
| **==**    | égalité             |
| **<**     | inferiorité stricte |
| **<=**    | inferiorité         |
| **>**     | superiorité stricte |
| **>=**    | superiorité         |
| **!=**    | différence          |

## Les opérateurs logiques

Permet de vérifier si des conditions sont vraies

| Opérateur | Dénomination | Effet                                                                                                                                    |
| --------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------- |
| **ll**    | OU logique   | Retourne true si au moins une des deux conditions vaut true (ou false sinon)                                                             |
| **&&**    | ET logique   | Retourne true si les deux conditions valent true (ou false sinon)                                                                        |
| **!**     | NON logique  | Retourne true si la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> vaut false, et false si elle vaut true) |

# <a id="evaluation"></a>L'évaluation 

Lorsque une opération doit avoir lieux, la priorité opératoire s'applique. Par exemple, comme vu précédemment, les <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> de type *double* contiennent plus d'informations de type *int*.

Lors d'une opération, <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a> va donc retourner un résultat de l'opération qui sera **"caster"** selon les type de <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>.

> int nbre1 = 3  
int nbre2= 2  
double resultat = nbre1 / nbre2  
// le résultat sera 1  

Le résultat de cet exemple sera un entier. En effet la priorité opératoire est en faveur du type int. Si l'on veut obtenir 1,5, il nous faudra faire un *cast* sur le résultat, en apposant le type désiré entre parenthèse devant chaque membre de l'opération.

> int nbre1 = 3  
int nbre2= 2  
double resultat = double(nbre1) / double(nbre2)  
// le résultat sera 1.5

Ainsi en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>, chaque membre d'une opération passe automatiquement et implicitement par une évaluation de son type et par un cast si besoin.

Lorsque l’opérande de gauche n’est pas un tableau, il s'éxecute dans cet ordre:

1. Vérifier que l’opérande est une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> déclarée
2. Sauvegarder la valeur de l’opérande gauche

3. Évaluer l’opérande de droite

4. Effectuer l’opération binaire indiquée par l’opérateur composé

5. Convertir le résultat de l’opération binaire en type de <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> de gauche **(casting implicite)** . Affecter le résultat converti à la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> de gauche

# <a id="assignation"></a>L'assignation

En programmation informatique, une affectation, ou assignation, est une structure qui permet d'attribuer une valeur à une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>.


En <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>, **il faut déclarer toute les <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> en précisant leur type** . On peut éventuellement ajouter des modificateurs. Ainsi déclarer une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> « final » revient à créer une constante car le compilateur refusera toutes les instructions modifiant la valeur de cette <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>.  
On peut effectuer une affectation ou assignation (donner une valeur) en déclarant une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a>.  
**Lors de sa création une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> reçoit toujours une valeur par défaut** . (0 pour les entiers, 0.0 pour les flottants, false pour les booléens, null pour les objets).

**Le signe égal ( = ) est le symbole basique d'assignation.**

```
// déclaration de a comme entier
int a ;
//affectation de a avec la valeur 3
a = 3;
```

Cette instruction déclare une nouvelle <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> x , attribue à x la valeur de 3 et renvoie 3 .

Il existe d'autre opérateur d'assignation :

    = Affecte une valeur à une variable
    += Addition
    -= Soustraction
    *= Multiplication
    /= Division
    %= Modulo
    &= ET logique et binaire
    |= OU logique et binaire

*Exemple* : Si l’on a x=4 et que l’on fait x+=3, alors x vaudra 7.   

Ceci est la même chose avec tous ces opérateurs d'assignation.


# <a id="instruction"></a> Les Instructions

Une instruction informatique désigne une étape dans un programme informatique.

Une instruction dicte à l'ordinateur l'action nécessaire qu'il doit effectuer avant de passer à l'instruction suivante.

Un programme informatique est constitué d'une suite d'instructions.

En <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>, une instruction se termine par un point virgule `;`

```exemples

System.out.println("Hello World"); // ceci est une instruction

int resultat = 1 + 1; // ceci est une autre instruction

String resultat2 = "Je suis un texte" // une troisième instruction

```

Les instructions se lisent de haut en bas.

```java

int nombre1 = 1; // première instruction

int nombre2 = 1 + 1; //deuxième instruction

int nombre3 = nombre2 + nombre1; // troisième instruction

```

Dans le code précédent, les instructions sont soit indépendantes, soit dépendantes.

`nombre1` et `nombre2` se voient assignés une valeur par assignation directe ou via une opération mathématique `(1 + 1)`

`nombre3` se voit assigné une valeur via l'addition de `nombre1` et `nombre2`.

Il ne serait pas possible d'assigner de à `nombre3` si `nombre1` et `nombre2` avaient été déclarés après.

```javaint nombre3 = nombre2 + nombre1; // Erreur, nombre1 et nombre2 n'existent pas encore

int nombre1 = 1; 

int nombre2 = 1 + 1; 

```

# <a id="bloc-instruction"></a> Le bloc d'instructions

Avant de définir ce qu'est un bloc d'instruction, il faut définir ce qu'est une instruction.

Une instruction informatique désigne une étape dans un programme informatique. 

Une instruction dicte à l'ordinateur l'action nécessaire qu'il doit effectuer avant de passer à l'instruction suivante. 

En <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>, une instruction se termine par un point virgule `;`

```java

System.out.println("Hello World"); // ceci est une instruction

int resultat = 1 + 1; // ceci est une autre instruction

String resultat2 = "Je suis un texte" // une troisième instruction

```

Les instructions se lisent de haut en bas.

```java

int nombre1 = 1; // première instruction

int nombre2 = 1 + 1; //deuxième instruction

int nombre3 = nombre2 + nombre1; // troisième instruction

```

Dans le code précédent, les instructions sont soit indépendantes, soit dépendantes.

`nombre1` et `nombre2` se voient assignés une valeur par assignation directe ou via une opération mathématique `(1 + 1)`

`nombre3` se voit assigné une valeur via l'addition de `nombre1` et `nombre2`.

Il ne serait pas possible d'assigner `nombre1` et `nombre2` à `nombre3` si `nombre1` et `nombre2` avaient été déclarés après.

```java
int nombre3 = nombre2 + nombre1; // Erreur, nombre1 et nombre2 n'existent pas encore

int nombre1 = 1; 

int nombre2 = 1 + 1; 

```

Un programme informatique est constitué d'une suite d'instructions qui s'exécutent dans un `bloc d'instructions`.

## Déclaration d'un bloc d'instructions

En <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>, un bloc d'instructions se déclare entre crochets `{}`

Les conditions `if/else/else if` sont des blocs d'instructions.

```java

if(true){
    /*
    instruction 1;
    instruction2;
    ...
    */
}else{
    /*
    instruction 1;
    instruction2;
    ...
    */
}else{
    /*
    instruction 1;
    instruction2;
    ...
    */
}
```

Les boucles `for/while/do while` sont des blocs d'instructions.

```java
    for(int i=0;i<100;i++){
        /*
    instruction 1;
    instruction2;
    ...
    */
    }

    while(true){
        /*
    instruction 1;
    instruction2;
    ...
    */
    }

    do{
/*
    instruction 1;
    instruction2;
    ...
    */
    }while(true);
```

Les méthodes de classe sont des blocs d'instruction.

```java
public void function bonjour(){
    /*
    instruction 1;
    instruction2;
    ...
    */
}
```
Les classes sont des blocs d'instruction.

```java

public class MaClasse{
    
    public void method1(){}

    public void method2(){}

    //...
}
```

Chaque bloc d'instruction définit la durée de vie des instructions qui sont déclarées à l'intérieur.

Ainsi dans une fonction, les instructions à l'intérieur ne sont pas accessibles à l'extérieur. Les <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> déclarées à l'intérieur n'existent plus une fois le bloc d'instruction terminé

```java

public function MaMethode(int nombre, int nombre2){
    int addition =  nombre1 + nombre2;

    return addition;
}

int resultat = MaMethode(10,10);

System.out.println(addition) // Erreur, addition n'existe pas en dehors de la méthode MaMethode

```

Si une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> est déclarée dans un bloc d'instruction, elle n'existe plus en dehors de ce bloc.

```java

if(true){
    int nombre = 10;
}else{
    nombre = 20; //Erreur, nombre n'existe que dans if, pas dans else
}
```

Par contre

```java

public void function maMethode(){
    int nombre = 0;

    if(true){
        nombre = 10; //ok
    }else{
        nombre = 20; //ok
    }
}


```

`nombre` est défini en amont des blocs d'instruction `if` et `else` dans la méthode `maMethode`, les blocs d'instruction enfants peuvent donc récupérer la <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> `nombre`.

Un bloc d'instruction enfant peut lire les <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> de son parent mais pas l'inverse, la fin d'une instruction signifiant la fin de vie de toutes les instructions à l'intérieur. 

Comme le bloc d'instruction parent n'est pas fini, ses <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> sont encore accessibles.

# <a id="commentaire"></a>Les commentaires


Les commentaires permettent de rendre votre code lisible et surtout d'en faciliter ultérieurement la maintenance.

En général, l'insertion de commentaire se fait soit en fin de ligne, soit sur une nouvelle ligne mais en aucun cas au sein d'une ligne de commande.

- Ils ne sont pas pris en compte par le compilateur donc 
- ils ne sont pas inclus dans le pseudo code
- ils ne terminent pas par un ;
- Il existe trois **types** de commentaires en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>.
- **types** de commentaires en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a> :

**1-Commentaire sur une seule ligne**

La première consiste à placer un double slash `//` 

```java
public class Main {
  public static void main(String[] args) {
    //Afficher le message Hello World en console!
    System.out.println("Hello World!");
  }
}
```


**2-Commentaire sur plusieurs lignes**

La seconde solution est d'encadrer le texte par un slash suivi d'une étoile (/*) et la même séquence inversée (*/)

```java

/*
  Ceci est un commentaire 
  sur plusieurs 
  lignes
*/`

//Example:
`public class Main {
  public static void main(String[] args) {
    /*
        Déclarer et afficher
        le message Hello World!
    */
    String str = "Hello World!";
    System.out.println(str);
  }
}
//Sortie: Hello World!
```

**3-Commentaire de documentation**
Ce type de commentaires est généralement utilisé lors de l’écriture du code pour un projet, car il permet de générer une page de documentation de référence, qui peut être utilisée pour obtenir des informations sur les méthodes, ses paramètres, etc.

```java

`**
*
*-Ceci est un Commentaire 
*- de documentation
*/
 
 /**
 *Programme Java pour déclarer et afficher
 *le message Hello World!
 *-
 *- @author  Thomas babtise
 *-@version 2.5 
 *-@since   2021-12-10
 *-@link    www.waytolearnx.com
 *-
 **/
public class Main {
  public static void main(String[] args) {
    String str = "Hello World!";
    System.out.println(str);
  }
}`

//sortie: Hello World!

```

# <a id="condition"></a>Les conditions

Une condition va vous permettre d'exécuter une portion de code ou non en fonction du résultat de <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variables</a> booléennes, c'est à dire que vous pourrez dire "si X est faux alors je fais ça, sinon ceci et si aucune des conditions précédentes n'est remplie, je ferais plutôt cela".

## Exemple d'une condition

```java
public boolean variable = true;

if(variable == true)
{
     //Si variable = a vrai(true) alors on execute ce code
     System.out.println("La variable est vrai");
}
```

## Les opérateurs de comparaison

Permet de comparer des valeurs ou de savoir si la condition est vrai ou fausse 

```java
public int var = 5;
```

| Opérateur | Dénomination                    | Effet                                                                                                                            | Exemple  | Résultat                                     |
| --------- | ------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------- | -------------------------------------------- |
| ==        | opérateur d'égalité             | Compare deux valeurs et vérifie leur égalité                                                                                     | var == 5 | Retourne vrai si var égale 5                 |
| <         | opérateur d'infériorité stricte | Verifie qu'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> est strictement inférieure           | var < 4  | Retourne faux car 5 et pas plus petit que 4  |
| <=        | Opérateur d'inféririoté         | Vérifie qu'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> inférieure ou egale                  | var <= 5 | Retourne vrai car 5 et egale a 5             |
| >=        | Opérateur de superiorité        | Vérifie qu'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> est supérieure ou égale à une valeur | var >= 2 | Retourne vrai car 5 et superieur a 2         |
| !=        | Operateur de différence         | Vérifie qu'une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> est supérieure ou égale à une valeur | var != 5 | Retourne faux car 5 n'est pas different de 5 |

## Autres exemples

```java
public int variable = 5;

if(variable == 5)
{
     //Si variable == 5 on execute ce code
     System.out.println("La variable est a 5 donc le code s'execute");
}
```

```java
public int variable = 10;

if(variable <= 5)
{
     //Si variable est inférieure ou egale 5 on execute ce code
     System.out.println("Ce code ne s'execute pas");
}
```

## Sinon (else)
Il existe une autre facon d'écrire des conditions que seulement avec des si (if) on peut ecrire une condition avec un sinon(else) à la suite d'un if(si), else signifie que si une condition et pas vrai alors on execute un autre bout de code 

## Exemple avec Else

```java
public int variable = 10;

if(variable <= 5)
{
     //Si variable est inférieure ou egale 5 on execute ce code
     System.out.println("Ce code ne s'execute pas");
} else
{
    //Sinon on execute ce code
    System.out.println("Ce code s'execute");
}
```

On peut aussi combiné un else avec un if

## Exemple avec Else If

```java
public int variable = 10;

if(variable <= 5)
{
     //Si variable est inférieure ou egale 5 on execute ce code
     System.out.println("Ce code ne s'execute pas");
} else if (variable == 10)
{
    //Sinon si variable == 10 on execute ce code
    System.out.println("Ce code s'execute");
}
```

# <a id="boucle"></a>Les boucles

Les boucles permettent de **répéter une ou plusieurs instructions**, selon les conditions désirées.

On en compte plusieurs **types**:

# La boucle FOR

Elle permet de contrôler exactement le nombre de répétitions (d'*itérations*) de la boucle.
C'est la plus compliquée à appréhender de toutes parce qu'elle demande plusieurs paramètres.
Sa structure est composée de telle manière:

```java
for( <initialisation> ; <condition> ;  <incrémentation>) {
    <actions>
}
```

Souvent, on utilise une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> temporaire qui garde le compte du nombre d'itérations. Elle est souvent appelée `i` comme *index*, et est un point de repère pour la boucle et le développeur ; mais elle peut s'appeler n'importe comment.

- Dans l'**initialisation** de la boucle, on définit quel est l'état de la boucle avant sa première répétition ; par exemple
`int i = 0`.
Dans cet exemple, on définit une <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> i étant égale à 0.

- Dans la **condition** de la boucle, on définit quel est la condition d'arrêt de la boucle ; par exemple
`i <= 20`.
Dans cet exemple, la boucle se répétera tant que la valeur de notre *i* sera inférieure ou égale à 20.

- Dans le paramètre d'**incrémentation** de la boucle, on définit ce qui change à chaque répétition, et qui va permettre à la boucle de se finir à un moment donné. Par exemple:
`i++`.
Dans cet exemple, à chaque répétition de la boucle, la valeur de `i` s'augmente de 1.

## Résultat

Voilà ce que donne nos exemples appliqués ensemble:

```java
for( int i=0 ; i <= 20 ; i++){
    System.out.println(i);
}
```

Cet exemple dans la console nous renverra à chaque répétition la valeur de `i`, jusqu'à 20.

## FOR avec une array

On peut utiliser For pour faire une action pour chaque <a href="https://fr.wikipedia.org/wiki/Variable_(informatique)">variable</a> d'une array, par exemple :

```java
for (int i=0; i<myArray.length; i++) {
    System.out.println(myArray[i]);
}
```

Cet exemple enverra chaque objet de l'array dans la console tour à tour.


# La boucle WHILE

La boucle while permet de créer une boucle avec pour seule instruction sa condition de répétition (s'imaginer while comme "*tant que* \<condition>, faire \<actions>".
Elle s'écrit comme dans cet exemple:

```java
while(i<20){
    i++;
}
```

# La boucle DO... WHILE

Cette boucle ressemble beaucoup à la précédente, à l'exception que sa condition est écrite après son action, garantissant que la boucle s'éxécute au moins une fois.
Exemple:

```java
int i = 0;

do{
    System.out.println("coucou");
} while(i ==1);
```

Affichera une fois *"coucou"*, même si la condition n'est jamais respectée.

## L'instruction *continue*

Dans une boucle, on peut utiliser `continue` pour dire qu'une partie du code ne doit pas s’exécuter selon certaines conditions:

```java
while(i<20){
    i++;
        if(i ==5){
            continue;
        }
    System.out.println("coucou");
    }
```

La suite du code ne s'exécute pas lorsque `i` est égal à 5, et donc n'affichera pas *"coucou"* à ce moment là.

## L'instruction *break*

On peut utiliser `break` pour arrêter une boucle à un moment voulu, même si la condition de la boucle n'est pas encore respectée:

```java
while(i<20){
    i++;
    if(i ==5){
        break;
    }
}
````

Au moment où `i` sera égal à 5, la boucle s'arrêtera complêtement, alors même que `i` n'est pas encore supérieur ou égal à 20.

## <a id="fonction"></a> La fonction (appelée méthode de classe en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>)

La fonction ou méthode de classe est un bloc d'instruction réutilisable permettant de recevoir des arguments.

Plutôt que de répéter plusieurs opérations identiques, il suffit de créer une fonction et de mettre ces opérations à l'intérieur.

Aisin si l'on voulait effectuer une opération mathématiques sur deux valeurs on pourrait le faire de cette façon:

```java

int addition = 2+2;

int soustration = 5 - 3;

float division = 10 / 2;

int multiplication = 4 * 7;

```

Grâce aux fonctions, il est possible d'encapsuler ces opérations:

```java
public int function Addition(int nombre1, int nombre2){
    return nombre1 + nombre2;
}

public int function Soustraction(int nombre1, int nombre2){
    return nombre1 - nombre2;
}

public float function Division(float nombre1, float nombre2){
    return nombre1 / nombre2;
}

public int function Multiplication(int nombre1, int nombre2){
    return nombre1 * nombre2;
}
```

## <a id=""></a>Déclaration d'une méthode de classe

La déclarion d'une méthode de classe/fonction s'éffectue d'abord par la déclaration de sa portée.

- `public` : accès publique. La méthode est disponible depuis partout, par toutes les classes.
- `protected` : accès protégé. La méthode n'est disponible qu'à l'intérieur d'une classe. Elle peut être donc visible pour les classes héritantes. Elle est aussi visible pour des classes non héritantes mais étant du même package.
- `private` : accès privé. La méthode n'est disponible qu'à l'intérieur d'une classe. Héritée, elle n'est pas visible.
 
Puisqu'en <a href="https://fr.wikipedia.org/wiki/Java_(technique)">Java</a>, tout est objet, une méthode appartient obligatoirement à une classe.

une méthode de classe peut être déclarée `static`. Quand une méthode est déclarée `static`, elle ne peut être appelée que par la classe elle-même et non par une instance de classe. 

```java 
class MaClass{
    public static void MaMethodeStatique(){
        System.out.println("Je suis appelée par une classe");
    }

    public void MaMethode(){
        System.out.println("Je suis appelée par une instance de classe");
    }
}
```

`MaMethodeStatique` ne peut être appelée que par `MaClass` quand `MaMethode` ne pourra être appelée que par une instance de `MaClass`

Il faut ensuite définir le type de retour de la fonction.
Une fonction peut ou non retourner un résultat.

Sans retour de résultat, il faudra déclarer la méthode par le mot clé `void`.

Selon la valeur de retour, il faudra déclarer le retour comme étant un `int`,`float`,`char`,`String`...

La fonction se déclare avec le mot clé `function` puis par le nom qu'on veut lui donner. Ce sera ensuite son identifiant pour l'appeller (`Addition`, `Soustraction`...).

Les arguments qu'on veut injecter dans cette fonction se déclarent entre parenthèses `()`.

Le traitement des arguments et autres opérations propres à la fonction se déclarent entre crochets  `{ }`. 

Si la méthode renvoit un résultat, le bloc d'instruction se terminera par l'instruction `return` puis le résultat à retourner.

Une fois la fonction déclarée, il est ensuite possible de l'utiliser à l'infini en l'appelant dans notre code:

```java

int resultatAddition = Addition(5,10);
int resultatAddition2 = Addition(6,9);

int resultatSoustraction = Soustraction(100,50);
int resultatSoustraction2 = Soustraction(4,1);

float resultatDivision = Division(10.0,4.0);
float resultatDivision2 = Division(300.0,8.0);

int resultatMultiplication = Multiplication(2,2);
int resultatMultiplication2 = Multiplication(5,9);

```

# <a id="parametre"></a> Les paramètres

En programmation informatique, un paramètre est une donnée manipulée par une section de code et connue du code appelant cette section. 

Par exemple, une fonction définit les paramètres qu'elle recevra pour traiter une succession d'intructions.


```java
fonction direBonjour(String message){
    System.out.println(message);
}
```
`message` est ici le paramètre de `direBonjour`

Lors de l'utilisation de la fonction, on renseignera les arguments que l'on veut passer en paramètres.

```java
direBonjour("Salut ça va bien?");
direBonjour("Hey bonjour vous!");
```

Les paramètres sont aussi utilisé dans le cadre des conditions et des boucles

```java 
boolean jeSuisVrai = false;

if(jeSuisVrai){
    System.out.println("C'est bien vrai!");
}else{
    System.out.println("Ah ba non, pas d'accord!");
}

//ou bien

while(jeSuisVrai){
    //instructions
}
```