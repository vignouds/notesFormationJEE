Java compilé en Byte Code

Byte code interprété par la JVM (Java Virtual Machine)

Portabilité

Garbage collector de la JVM : réserve et libère la mémoire de manière automatique ; du coup les applications Java consomment beaucoup de mémoire à cause de cette surcouche

JDK : pour les développeurs (compiler)
JRE : pour les utilisateurs (executer)

Fichier .class = byte code

.jar = biliothèque

On peut rendre un .jar excecutable. Il faut une fonction main et un fichier metainf à la racine

/** génère une javadoc

## Les variables
Le type byte(1 octet) peut contenir les entiers entre -128 et +127.

Le type short(2 octets) contient les entiers compris entre -32768 et +32767

Le type int(4 octets) va de -2*109 à 2*109

Le type long (8 octets) peut aller de −9×10^18  à 9×10^18

Le type float(4 octets) est utilisé pour les nombres avec une virgule flottante.

Le type double(8 octets) est identique à float, si ce n'est qu'il contient plus de chiffres derrière la virgule et qu'il n'a pas de suffixe.

### String

!!! String est un objet
les String sont immuables

valeur par défaut : null

`string nom="toto";
nom = null;`

*nom pointe désormais vers null ce qui permet de supprimer toto de la mémoire (vide la mémoire)*



## Les conditions et les boucles
Comparaisons (==, !=...) ne marchent qu'avec les types primitifs (string, int...) et pas les objets

break = sortir de la boucle

continue = passer à l'interaction suivante

marche pour tous les blocs

## Les tableaux
On doit définir la taille du tableau quand on le crée.

## POO
public : visible partout

rien : visible dans le même package

protected : visible dans le même package

private : uniquement par la classe elle-même

transient interdit serialisation

serialisation : sauvegarde dans une base de données

final = constante (valeur non modifiable)

`pubic final int PAGE_SIZE=10;`

abstract = ne peut pas être instanciée

signature = couple nom-paramètres

cast = transtypage

methode statique = une seule instance par classe ; appellable sur la classe elle-même

Une classe anonyme n'a pas de nom

## Conventions de nommage

UpperCamelCase
LowerCamelCase

## maven
Modifier le fichier pom.xml du projet pour indiquer que l’on compile des sources avec la version Java 8

```
<project>
//....
<properties>
  <maven.compiler.target>1.8</maven.compiler.target>
  <maven.compiler.source>1.8</maven.compiler.source>
</properties>
</project>
```

## Tests
JUnit = framework de test en Java
PIC = Plateforme d'Integration Continue
