# Notion de variable

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
                                                                         








