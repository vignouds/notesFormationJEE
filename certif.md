## Certification 3 - 26/04

tri des lettres se fait selon la table ASCII. Les majuscules sont donc avant les minuscules

`char c = 65; ` fonctionne grâce à table ASCII

Valeur par défaut d'un objet = null

Classe Java exécutable :
````
public static void main(String... args)
//ou
public static void main(String[] args)
````

switch/case : interdit d'utiliser  des variables dans les cases

Opérateur ^ retourne true si un des deux membres est true et l'autre false

Opérateur ^ retourne false si les deux membres sont true ou les deux membres sont false

On peut utiliser == pour comparer des primitives, ça marche toujours

Syntaxe de boucle pour parcourir un tableau :
````
for(User user:users)
// préférable à
for(int i=0;i<users.lenght;i++)
````

An abstract class must use the abstract keyword when declared

capacity par défaut d'un StringBuilder vide = 16

Dimension maximale d'un tableau : 255

`System.out.print()` provoque une erreur car le paramètre est obligataire

`int x, y = 100` interdit en java (possible en javascript)

>"Le couplage est une métrique indiquant le niveau d'interaction entre deux ou plusieurs composants logiciels (fonctions, modules, objets ou applications). Deux composants sont dits couplés s'ils échangent de l'information. On parle de couplage fort ou couplage serré si les composants échangent beaucoup d'information. On parle de couplage faible, couplage léger ou couplage lâche si les composants échangent peu d'information."

Static = lu à la compilation

LocalDate est immutable
String est immutable
(immutable = quand on fait des modifications dessus ça renvoie un nouvel objet)
### Les imports
Pas de notion de sous-package en Java

````
import java.*
// importe seulement les classes qui sont au même niveau et pas tout l'arborescence
````

java.lang importé de base dans tout projet java

Interdit d'écrire du code avant un import

### Les exceptions

Seules les errors sont jetées par la JVM (ex : ExceptionInInitializeError)

si on essaie d'accéder à un indice de tableau qui n'existe pas = runtime exception
```
int array[] = new int[2];
array[2]=10;
```
Division par 0 = runtime exception
NumberFormatException = runtime
NumberFormatException hérite de IllegalArgumentException

IOException = erreur liée aux entrées/sorties

FileNotFOundException hérite de IOException
