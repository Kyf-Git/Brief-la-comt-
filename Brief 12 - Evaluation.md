## L'évaluation 

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
