# Instructions

C'est quoi?
<p><br>Une instruction informatique désigne une étape dans un programme informatique.</br>
<p>Une instruction dicte à l'ordinateur l'action nécessaire qu'il doit effectuer avant de passer à l'instruction suivante. </p>
<p>Un programme informatique est constitué d'une suite d'instructions.</p>

En java, une instruction se termine par un point virgule `;`

```exemples

System.out.println("Hello World"); // ceci est une instruction

int resultat = 1 + 1; // ceci est une autre instruction

String resultat2 = "Je suis un texte" // une troisième instruction

```

Les instructions se lisent de haut en bas.

```en java

int nombre1 = 1; // première instruction

int nombre2 = 1 + 1; //deuxième instruction

int nombre3 = nombre2 + nombre1; // troisième instruction

```

Dans le code précédent, les instructions sont soit indépendantes, soit dépendantes.

`nombre1` et `nombre2` se voient assignés une valeur par assignation directe ou via une opération mathématique `(1 + 1)`

`nombre3` se voit assigné une valeur via l'addition de `nombre1` et `nombre2`.

Il ne serait pas possible d'assigner de à `nombre3` si `nombre1` et `nombre2` avaient été déclarés après.

```en java

int nombre3 = nombre2 + nombre1; // Erreur, nombre1 et nombre2 n'existent pas encore

int nombre1 = 1; 

int nombre2 = 1 + 1; 

```
