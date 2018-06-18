webkit = moteur de rendu js
Package.json = équivalent du pom.xml
Port par défaut de node = 3000

``npm init -y`` pour initialiser le package.json
``npm search module`` pour rechercher un module
``npm install module`` pour installer un module
``npm install module --save`` paramètre save permet d'ajouter le module à package.json
``npm install module -dev`` pour installer en dépendance de développement
``npm install module -g`` pour installer de manière globale


``node index.js`` pour lancer le script

``npm start`` pour lancer le script si on spécifié le raccourcis dans package.json
idem pour ``npm test``

## Rappel JE ES5
undefined : valeur n'a jamais été affectée
null : affectée à  null

## ES6
possibilité de déclarer des constantes avec ``const``
``let`` variable avec scope au niveau block
arrow function = équivalent des lambdas en Java ; avec des parenthèses à gauche de la flèche le return est implicite

### functions parameters
````
function f(x, y=7, z=42) {
  return x+y+z
}
f(1)===50
f(1,2)===45
f(1,2,3)===6
````

### classes
mot-clef class
En JS, 1 seul constructeur par classes
Heritage avec extends et super(), comme en Java
