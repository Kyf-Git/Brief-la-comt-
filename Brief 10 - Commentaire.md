
Les commentaires permettent de rendre votre code lisible et surtout d'en faciliter ultérieurement la maintenance.

En général, l'insertion de commentaire se fait soit en fin de ligne, soit sur une nouvelle ligne mais en aucun cas au sein d'une ligne de commande.

> ♦Ils ne sont pas pris en compte par le compilateur donc ils ne sont pas inclus dans le pseudo code
♦ils ne terminent pas par un ;
♦Il existe trois types de commentaires en Java.
♦Types de commentaires en Java :

**1-Commentaire sur une seule ligne**
La première consiste à placer un double slash (//) 
♦Syntaxe:
`public class Main {
  public static void main(String[] args) {
    //Afficher le message Hello World!
    System.out.println("Hello World!");
  }
}`
♦Sortie: Hello World!

**2-Commentaire sur plusieurs lignes**
La seconde solution est d'encadrer le texte par un slash suivi d'une étoile (/*) et la même séquence inversée (*/)
♦Syntaxe:
`/*
  Ceci est un commentaire 
  sur plusieurs 
  lignes
*/`

♦Example:
`public class Main {
  public static void main(String[] args) {
    /*
        Déclarer et afficher
        le message Hello World!
    */
    String str = "Hello World!";
    System.out.println(str);
  }
}`
♦Sortie: Hello World!

**3-Commentaire de documentation**
Ce type de commentaires est généralement utilisé lors de l’écriture du code pour un projet, car il permet de générer une page de documentation de référence, qui peut être utilisée pour obtenir des informations sur les méthodes, ses paramètres, etc.
♦Syntaxe:
`**
*
*-Ceci est un Commentaire 
*- de documentation
*
**/`
♦Example:
` /**
 *
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

♦Sortie: Hello World!