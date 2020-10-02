
Les boucles permettent de **répéter une ou plusieurs instructions**, selon les conditions désirées.

On en compte plusieurs types:
<br>

# La boucle FOR

Elle permet de contrôler exactement le nombre de répétitions (d'*itérations*) de la boucle.
C'est la plus compliquée à appréhender de toutes parce qu'elle demande plusieurs paramètres.
Sa structure est composée de telle manière:

```java
for( <initialisation> ; <condition> ;  <incrémentation>) {
    <actions>
}
```

Souvent, on utilise une variable temporaire qui garde le compte du nombre d'itérations. Elle est souvent appelée `i` comme *index*, et est un point de repère pour la boucle et le développeur ; mais elle peut s'appeler n'importe comment.

- Dans l'**initialisation** de la boucle, on définit quel est l'état de la boucle avant sa première répétition ; par exemple
`int i = 0`.
Dans cet exemple, on définit une variable i étant égale à 0.

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

On peut utiliser For pour faire une action pour chaque variable d'une array, par exemple :

```java
for (int i=0; i<myArray.length; i++) {
    System.out.println(myArray[i]);
}
```

Cet exemple enverra chaque objet de l'array dans la console tour à tour.
<br>

# La boucle WHILE

La boucle while permet de créer une boucle avec pour seule instruction sa condition de répétition (s'imaginer while comme "*tant que* \<condition>, faire \<actions>".
Elle s'écrit comme dans cet exemple:

```java
while(i<20){
    i++;
}
```

<br>

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

<br>

# Pour aller plus loin

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

Les boucles permettent de **répéter une ou plusieurs instructions**, selon les conditions désirées.

On en compte plusieurs types:
<br>

# La boucle FOR

Elle permet de contrôler exactement le nombre de répétitions (d'*itérations*) de la boucle.
C'est la plus compliquée à appréhender de toutes parce qu'elle demande plusieurs paramètres.
Sa structure est composée de telle manière:

```java
for( <initialisation> ; <condition> ;  <incrémentation>) {
    <actions>
}
```

Souvent, on utilise une variable temporaire qui garde le compte du nombre d'itérations. Elle est souvent appelée `i` comme *index*, et est un point de repère pour la boucle et le développeur ; mais elle peut s'appeler n'importe comment.

- Dans l'**initialisation** de la boucle, on définit quel est l'état de la boucle avant sa première répétition ; par exemple
`int i = 0`.
Dans cet exemple, on définit une variable i étant égale à 0.

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

On peut utiliser For pour faire une action pour chaque variable d'une array, par exemple :

```java
for (int i=0; i<myArray.length; i++) {
    System.out.println(myArray[i]);
}
```

Cet exemple enverra chaque objet de l'array dans la console tour à tour.
<br>

# La boucle WHILE

La boucle while permet de créer une boucle avec pour seule instruction sa condition de répétition (s'imaginer while comme "*tant que* \<condition>, faire \<actions>".
Elle s'écrit comme dans cet exemple:

```java
while(i<20){
    i++;
}
```

<br>

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

<br>

# Pour aller plus loin

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
