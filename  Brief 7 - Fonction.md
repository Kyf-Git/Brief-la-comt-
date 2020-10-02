### La fonction (appelée méthode de classe en Java)

La fonction ou méthode de classe est un bloc d'instruction réutilisable permettant de recevoir des arguments en paramètres.

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

### Déclaration d'une méthode de classe

La déclarion d'une méthode de classe/fonction s'éffectue d'abord par la déclaration de sa portée.

- `public` : accès publique. La méthode est disponible depuis partout, par toutes les classes.
- `protected` : accès protégé. La méthode n'est disponible qu'à l'intérieur d'une classe. Elle peut être donc visible pour les classes héritantes. Elle est aussi visible pour des classes non héritantes mais étant du même package.
- `private` : accès privé. La méthode n'est disponible qu'à l'intérieur d'une classe. Héritée, elle n'est pas visible.
 
Puisqu'en java, tout est objet, une méthode appartient obligatoirement à une classe.

une méthode de classe peut être déclarée `static`. Quand une méthode est déclarée `static`, elle ne peut être appelée que par la classe elle-même et non par une instance de classe. 

```java

class MaClass{
    public static void MaMethodeStatique(){
        System.out.print.ln('Je suis appelée par une classe");
    }

    public void MaMethode(){
        System.out.print.ln('Je suis appelée par une instance de classe");
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