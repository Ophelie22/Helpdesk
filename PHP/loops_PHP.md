## Les différentes boucles de PHP

### Boucle `while`

La boucle `while` va être utilisé dans les cas où l'on "__ne sais pas__" le nombre de boucles à effectuer. (__de préférence__)

```php
while (/* Conditions */) {
/* Actions de la boucle */ 
}
```
- __Conditions__ - Les conditions (tant que c'est vrai je continue la boucle, sinon je stop la boucle).
- __Actions de la boucles__ - Les action à appliquer à chaque boucle.

### Boucle `for`

La boucle `for` va être utilisé dans les cas où l'on "__sais__" le nombre de boucles à effectuer. (__de préférence__)

```php
for (/* Initialisation */;/* Conditions */;/* Actions */) {
// Actions de la boucle 
}
```
- __Initialisation__ - Action appliqué au départ de la boucle (__Pas à chaque boucle__).
- __Conditions__ - Les conditions (tant que c'est vrai je continue la boucle, sinon je stop la boucle).
- __Actions__ - Les action à appliquer à chaque boucle.
- __Actions de la boucles__ - Les action à appliquer à chaque boucle.

### Boucle `foreach`

La boucle `foreach` sert à faire une boucle sans indiquer le moment où celle-ci doit s'arréter, car elle va boucler en fonction du nombre de donné dans le tableau.
Exemple avec cette liste `$maListe = ['1','2','3','4']`, il y aura 4 boucle, car il y a 4 données dans cette liste.

#### Méthode n°1
```php
foreach (/* Tableau */ as /* Ligne */) {
// Actions par tour de boucle 
}
```
- __Actions__ - Les action à appliquer à chaque boucle.
- __Tableau__ - Le tableau que vous avez créer au préalable ; Exemple `$listeDesFilms`.
- __Ligne__ - La ligne du tableau, une nouvelle variable (nommée comme tu le souhaité) qui ne sortira pas de la boucle `foreach`


#### Méthode n°2
```php
foreach (/* Tableau */ as /* Ligne */ => /* Valeur */) {
// Actions par tour de boucle 
}
```
- __Actions__ - Les action à appliquer à chaque boucle.
- __Tableau__ - Le tableau que vous avez créer au préalable ; Exemple `$listeDesFilms`.
- __Ligne__ - La ligne du tableau, une nouvelle variable (nommée comme tu le souhaité) qui ne sortira pas de la boucle `foreach`
- __Valeur__ - La valeur de la ligne, une nouvelle variable (nommée comme tu le souhaité) qui ne sortira pas de la boucle `foreach`

### Méthode n°3
Identique à la `méthode n°2` à la différence qu'à la place des `{ /* Interieur de la boucle */ }` on vien remplacer par `: /* Interieur de la boucle */ endforeach;`.
C'est utilisé pour éviter de confondre la fermeture des accolades (`}`) du `foreach` avec la fermeture des accolades des `if() {}`, `esle if() {}` et `else {}`.
```php
foreach (/* Tableau */ as /* Ligne */ => /* Valeur */):
// Actions par tour de boucle 
endforeach;
```
- __Actions__ - Les action à appliquer à chaque boucle.
- __Tableau__ - Le tableau que vous avez créer au préalable ; Exemple `$listeDesFilms`.
- __Ligne__ - La ligne du tableau, une nouvelle variable (nommée comme tu le souhaité) qui ne sortira pas de la boucle `foreach`
- __Valeur__ - La valeur de la ligne, une nouvelle variable (nommée comme tu le souhaité) qui ne sortira pas de la boucle `foreach`