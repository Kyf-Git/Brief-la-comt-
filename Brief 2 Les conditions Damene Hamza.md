# Les conditions


Une condition va vous permettre d'exécuter une portion de code ou non en fonction du résultat de variables booléennes, c'est à dire que vous pourrez dire "si X est faux alors je fais ça, sinon ceci et si aucune des conditions précédentes n'est remplie, je ferais plutôt cela".

# Exemple d'une condition

```java
public boolean variable = true;

if(variable == true)
{
     //Si variable = a vrai(true) alors on execute ce code
     System.out.println("La variable est vrai");
}
```

### Les opérateurs de comparaison

Permet de comparer des valeurs ou de savoir si la condition est vrai ou fausse 

```java
public int var = 5;
```

| Opérateur | Dénomination | Effet | Exemple | Résultat |
| ------ | ------ | ------ | ------ | ------ |
| == | opérateur d'égalité | Compare deux valeurs et vérifie leur égalité | var == 5 | Retourne vrai si var égale 5
| < | opérateur d'infériorité stricte | Verifie qu'une variable est strictement inférieure | var < 4 | Retourne faux car 5 et pas plus petit que 4
| <= | Opérateur d'inféririoté | Vérifie qu'une variable inférieure ou egale | var <= 5 | Retourne vrai car 5 et egale a 5
| >= | Opérateur de superiorité | Vérifie qu'une variable est supérieure ou égale à une valeur | var >= 2 | Retourne vrai car 5 et superieur a 2
| != | Operateur de différence | Vérifie qu'une variable est supérieure ou égale à une valeur | var != 5 | Retourne faux car 5 n'est pas different de 5

### Autres exemples 

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

# Sinon (else)
Il existe une autre facon d'écrire des conditions que seulement avec des si (if) on peut ecrire une condition avec un sinon(else) à la suite d'un if(si), else signifie que si une condition et pas vrai alors on execute un autre bout de code 


### Exemple avec Else

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
### Exemple avec Else If
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

