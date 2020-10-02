
## Table des matières

1. [Introduction](#introduction)
2. [La notion de variable](#lanotiondevariable)
3. [Les mots clefs](#lesmotsclefs)
4. [Les opérateurs](#lesoperateurs)
5. [L'évaluation](#levaluation)
6. [L'assignation](#lassignation)
7. [L'instruction](#linstruction)
8. [Le bloc d'instructions](#leblocdinstruction)
9. [Le commentaire](#lecommentaire)
10. [La condition](#lacondition)
11. [La boucle](#laboucle)
12. [La fonction (ou méthode de classe)](#lafonction)
13. [Les paramètres](#lesparametres)

# <a href ="lanotiondevariable"></a>la Notion de variable

## Le concept de variables

Une variable est une donnée (un objet ou un type primitif) repérée par son nom, et qui pourra être lu, ou modifiée lors de l'exécution du programme.
 Les variables en langage Java sont typées, c'est-à-dire que les données contenues dans celles-ci possèdent un type, ainsi elles sont donc stockées à une adresse mémoire et occupent un nombre d'octets dépendant du type de donnée stockée.

En Java, les noms de variables peuvent être aussi long que l'on désire, toutefois le compilateur(programme qui traite les instructions écrites dans un langage de programmation donné pour les traduire en langage machine, ou « code », utilisé par le processeur d'un ordinateur) ne tiendra compte "que" des 247 premiers caractères. De plus, elles doivent répondre à certains critères :

-   un nom de variable ne peut comporter que des lettres, des chiffres (les caractères _ et $ peuvent être utilisés mais ne devrait pas l'être pour des variables)
-   un nom de variable ne peut pas commencer par un chiffre et ne doit pas comporter d'espace

Les noms de variables sont sensibles à la casse (Java fait la différence entre les lettres minuscules et majuscules, avec ou sans accent), il faut donc veiller à respecter la casse des noms !  
Par convention, un nom de variable est écrit en minuscules, sans accent, ni _ ou $. En revanche lorsqu'il est composé de plusieurs mots, on peut utiliser une majuscule pour l'initiale de chaque nouveau mot.

**Exemples de variables correctes**:
      nomDeVariable ; nomDeVariables123


## La déclaration des variables:

Pour pouvoir utiliser une variable, il faut la définir, c'est-à-dire lui donner un nom, mais surtout un type de donnée à stocker afin qu'un espace mémoire conforme au type de donnée qu'elle contient lui soit réservé.
Une variable se déclare de la façon suivante :   type nomDeVariable ;

Ou bien s'il y a plusieurs variables du même type :  type nomDeVariables ; ou nom_De_Variables2 ;

-   Java impose que les variables soient impérativement déclarées avant d'être utilisée.
-   Java permet de définir une variable à n'importe quel endroit du code.                 

## Affectation d'une donnée à une variable:
La déclaration d'une variable réserve un emplacement mémoire où stocker la variable, et une valeur par défaut (généralement 0, null ou false), pour modifier cette valeur par défaut, il faut faire une affectation, c'est-à-dire préciser la donnée qui va être stockée à l'emplacement mémoire qui a été réservé.  

Pour cela on utilise l'opérateur d'affectation "_=_" :
nomDeVariable = valeur;
Il est aussi possible d'initialiser les valeurs lors de leurs déclarations.
type nomDeVariable = valeur;

Exemple : Pour stocker le caractère B dans une variable que l'on appellera  _caractere_, il faudrait écrire :  

char caractere = 'B';
Ce qui signifie _"stocker la valeur Unicode de la lettre B dans la variable nommée 'caractere'_.

## Portée (visibilité) des variables :

Selon l'endroit où on déclare une variable, celle-ci pourra être accessible (visible) de partout dans le code ou bien que dans une portion confinée de celui-ci (à l'intérieur d'une méthode par exemple), on parle de  _portée_  d'une variable.  

Lorsqu'une variable est déclarée directement dans la classe, c'est-à-dire à l'extérieur de toute méthode, elle sera accessible dans toute la classe. On parle alors de  _champ_  de la classe (fields, en anglais). Elle représente l'état de l'objet courant (ou avec le mot clé static, l'état de la classe elle même).  

Lorsque l'on déclare une variable à l'intérieur d'un bloc d'instructions (entre des accolades), sa portée se restreint à l'intérieur de ce bloc (dans les lignes qui suit sa déclaration), on parle alors de variable locale.  

Il est interdit d'avoir deux variables de même nom si elles ont une portée commune. Il serait alors impossible de les distinguer...

## Définitions de constantes:

Une constante est une donnée dont la valeur est inchangeable lors de l'exécution d'un programme. Le mot clé _final_ permet de faire cela. Toutefois on ne peut véritablement parler de constantes en Java que pour les types primitifs, car pour un objet le mot clé final impose seulement que la référence de l'objet n'est pas modifiable, mais les champs de l'objets peuvent être modifiés malgré tout.  
  
Par convention, et pour les distinguer des variables, les constantes sont écrites entièrement en majuscules, et le caractère _ peut être utilisé pour séparer deux mots.

final int MA_CONSTANTE =12

aura pour effet de définir une variable de type _int_ possèdant la valeur 12 et ne pouvant pas être modifiée dans la suite du code, auquel cas le compilateur générera une erreur...


### <a href="lesmotsclefs"></a> Les mots clés

Les mots-clés sont des termes spécifiques au langage de programmation, certains sont utilisables par plusieurs langages et d'autres spécifiques à un langage.
On trouve plus de 50 mots clés qui ont les usages propres en java.
On ne peut les utiliser que dans un contexte précis et il est impossible de les déclarer en comme noms de classes ou variables. 
On retrouve différents types de mots-clés; des mots-clés pour déclarer des objets, variables, des états, des branchements et encore des exceptions.

Les mots pour les objets; "class", "interface", "implements", "enum", "import", "this", "abstract", "extends", "package", "super" &"native".

Les mots pour les types; "boolean", "char", "int", "float", "long", "short", "double", "byte" & "void".

Pour les états; "const" , "false", "true", "static", "null", "volatile", "new", "transient", "strictfp".

pour les boucles: "do", "for", "goto", "while", "continue".

pours les branchements; "if", "else", "return", "break", "assert", "switch", "synchronized", "default", "case" & "instanceof".

Et voici les mots-clés pour gérer des exceptions; "throw", "throws", "try", "catch" & "finally"


### <a href="lesoperateurs"></a> Les opérateurs

Les opérateurs sont des symboles permettant de manipuler et d’effectuer des operations mathématiques sur des variables, il en existe plusieurs types:


##Les opérateurs de calcul  

Permettent d'effectuer des opérations mathématiques simples sur/entre des variables

| Opérateur | Effet                                                                      |
| --------- | -------------------------------------------------------------------------- |
| **+**     | addition                                                                   |
| **-**     | soustraction                                                               |
| *         | multiplication                                                             |
| **/**     | division                                                                   |
| **%**     | modulo (rends le reste de la division)                                     |
| **=**     | affectation  (à ne pas confondre avec **==**, l'opérateur de vérification) |



##Les opérateurs d'assignation

Permet d'effectuer une opération de calcule à une variable et d'affecter son resultat à cette même variable 
(exemple: 
```java
 x = x+1
 ```
  pourra s'écrire 
  ```java
  x += 1
  ```

| Opérateur | Effet                                                          |
| --------- | -------------------------------------------------------------- |
| **+=**    | additionne deux valeurs et stocke le résultat dans la variable |
| **-=**    | soustrait deux valeurs et stocke le résultat dans la variable  |
| ***=**    | multiplie deux valeurs et stocke le résultat dans la variable  |
| **/=**    | divise deux valeurs et stocke le résultat dans la variable     |
| **%=**    | module deux valeurs et stocke le résultat dans la variable     |


##Les opérateurs d'incrémentation

Permet d'augmenter ou diminuer d'une unité une variable (utile pour les boucles par exemple)

| Opérateur | Effet                            |
| --------- | -------------------------------- |
| **++**    | augmente d'une unité la variable |
| **--**    | diminue d'une unité la variable  |

##Les opérateurs de comparaison

Permettent d'effectuer des opérations de comparaison entre des variables, retournent  TRUE or FALSE

| Opérateur | Effet               |
| --------- | ------------------- |
| **==**    | égalité             |
| **<**     | inferiorité stricte |
| **<=**    | inferiorité         |
| **>**     | superiorité stricte |
| **>=**    | superiorité         |
| **!=**    | différence          |

##Les opérateurs logiques

Permet de vérifier si des conditions sont vraies

| Opérateur | Dénomination | Effet                                                                        |
| --------- | ------------ | ---------------------------------------------------------------------------- |
| **ll**    | OU logique   | Retourne true si au moins une des deux conditions vaut true (ou false sinon) |
| **&&**    | ET logique   | Retourne true si les deux conditions valent true (ou false sinon)            |
| **!**     | NON logique  | Retourne true si la variable vaut false, et false si elle vaut true)         |

## <a href="levaluation"></a>L'évaluation 

Lorsque une opération doit avoir lieux, la priorité opératoire s'applique. Par exemple, comme vu précédemment, les variables de type *double* contiennent plus d'informations de type *int*.

Lors d'une opération, Java va donc retourner un résultat de l'opération qui sera **"caster"** selon les type de variable.

> int nbre1 = 3  
int nbre2= 2  
double resultat = nbre1 / nbre2  
// le résultat sera 1  

Le résultat de cet exemple sera un entier. En effet la priorité opératoire est en faveur du type int. Si l'on veut obtenir 1,5, il nous faudra faire un *cast* sur le résultat, en apposant le type désiré entre parenthèse devant chaque membre de l'opération.

> int nbre1 = 3  
int nbre2= 2  
double resultat = double(nbre1) / double(nbre2)  
// le résultat sera 1.5

Ainsi en Java, chaque membre d'une opération passe automatiquement et implicitement par une évaluation de son type et par un cast si besoin.

Lorsque l’opérande de gauche n’est pas un tableau, il s'éxecute dans cet ordre:

1. Vérifier que l’opérande est une variable déclarée
2. Sauvegarder la valeur de l’opérande gauche

3. Évaluer l’opérande de droite

4. Effectuer l’opération binaire indiquée par l’opérateur composé

5. Convertir le résultat de l’opération binaire en type de variable de gauche **(casting implicite)** . Affecter le résultat converti à la variable de gauche
