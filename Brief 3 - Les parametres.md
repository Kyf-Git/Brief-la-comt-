Les paramètres sont utilisées **par les fonctions** pour leur **donner du matériel avec lequel travailler**.

# Théorie

Lors de la déclaration d'une fonction, on lui indique à l'avance les outils dont elle aura besoin, entre parenthèses, juste après le nom de la fonction.
On sépare plusieurs paramètres par des virgules.
Exemple:

```java

fonction maFonction(int monParametre){
    <actions>
}

```

# Utilisation

Lors de **l'appel** d'une fonction, on donne entre parenthèses les valeurs que la fonction utilisera comme paramètres.
Exemple:


```java

fonction monProfil(String monAge, String monPrenom){
    return monPrenom + " a " + monAge + "ans."
}

String prenom = "Jean-Bob";

monProfil("12", prenom);

```

Notre fonction renverra ainsi *"Jean-Bob a 12 ans"*

# Cas d'exemple: pour conditionner

On peut aussi utiliser des paramètres pour donner des **conditions** pour l’exécution du code au sein d'une fonction
Exemple: 

```java

bool buMonCafé = true;
bool prisMonPC = true;

bool jeSuisPrêt = (buMonCafé && prisMonPC);

fonction commencerJournee(bool ready){
    if(ready){
        aller_a_simplon();
    }
}

commencerJournee(jeSuisPrêt);

```