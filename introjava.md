# Rappel des bases de Java

## 1. Définition et caractéristiques

Java est un langage de programmation polyvalent et orienté objet, développé pour répondre aux besoins de la programmation multiplateforme. Il s'agit de l'un des langages les plus populaires et les plus largement utilisés dans le monde, principalement en raison de sa robustesse, de sa sécurité, et de sa capacité à fonctionner sur divers systèmes d'exploitation sans nécessiter de modifications du code source.

### Qu’est-ce que Java ?

```{admonition} Définition
Java est un langage de programmation **orienté objet** qui a été initialement développé par Sun Microsystems (désormais sous la propriété d'Oracle) en **1995**. Il est conçu pour être simple, sécurisé et compatible avec de multiples plateformes, rendant son utilisation idéale pour les applications web, mobiles, et les systèmes embarqués.
```

Java est souvent décrit comme un langage de niveau intermédiaire, car il est à la fois proche du matériel, par sa syntaxe simple et optimisée, et indépendant des systèmes d'exploitation, grâce à la **Java Virtual Machine (JVM)**.

### Les Principes Fondateurs de Java

Java repose sur plusieurs principes clés qui ont influencé sa conception et son développement, permettant aux développeurs de bénéficier de sa portabilité et de sa flexibilité.

#### 1.1 Write Once, Run Anywhere (WORA)

L’un des principes fondamentaux de Java est le concept **WORA (Write Once, Run Anywhere)**, qui signifie "écrire une fois, exécuter partout". Ce principe indique qu'un programme Java, une fois écrit et compilé, peut s'exécuter sur n'importe quel système d'exploitation équipé de la **JVM (Java Virtual Machine)**, sans nécessiter de modification du code source.

```{admonition} Avantage de WORA
Le principe WORA fait de Java un langage indépendant des plateformes, permettant aux développeurs de déployer leurs applications sur différentes machines sans avoir à adapter le code à chaque système d'exploitation.
```

#### 1.2 Java Virtual Machine (JVM)

La **JVM** est un élément essentiel de la plateforme Java, jouant un rôle fondamental dans l'indépendance de Java par rapport aux plateformes matérielles et logicielles.

```{admonition} Définition
La **Java Virtual Machine (JVM)** est une machine virtuelle qui permet d’exécuter le code Java. Elle interprète le bytecode (code intermédiaire de Java) et l'exécute sur le système d'exploitation hôte.
```

Le bytecode Java est un code intermédiaire généré par le compilateur Java. Contrairement aux autres langages qui se compilent directement en langage machine spécifique à un système d'exploitation, Java est compilé en bytecode, lequel est ensuite interprété par la JVM. Ce bytecode garantit que le même code source Java fonctionnera sur différents systèmes d'exploitation (Windows, macOS, Linux, etc.) tant que la JVM est présente.

#### 1.3 Compilation et Bytecode

L’un des aspects uniques de Java est son processus de compilation en **bytecode**. Ce processus permet de s'assurer que le programme Java est indépendant de la plateforme.

1. **Écriture du Code Source** : Le code source Java est écrit dans des fichiers `.java`.
2. **Compilation** : Le compilateur Java (`javac`) convertit le code source en bytecode, un langage intermédiaire indépendant de la plateforme, stocké dans des fichiers `.class`.
3. **Interprétation par la JVM** : Lors de l'exécution, la JVM interprète le bytecode et le convertit en instructions machine pour le système d'exploitation hôte.

```{admonition} Bytecode : Avantages et Sécurité
Le bytecode offre plusieurs avantages :
- **Portabilité** : Grâce à la JVM, le même bytecode peut être exécuté sur différentes plateformes.
- **Sécurité** : Le bytecode est vérifié par la JVM avant d'être exécuté, limitant les risques de comportements indésirables et renforçant la sécurité.
```

### Caractéristiques de Java

Java se distingue par plusieurs caractéristiques qui le rendent adapté pour des projets variés, de la simple application de bureau aux systèmes distribués complexes.

#### 1.4 Langage Orienté Objet

Java est intrinsèquement un langage de programmation **orienté objet (POO)**, ce qui signifie que tout est structuré autour des objets et des classes. La POO facilite la modélisation de concepts réels en code et permet une organisation modulaire, facilitant la maintenance et la réutilisabilité.

Les principes fondamentaux de la POO en Java incluent :
- **Encapsulation** : Regroupe les données et les méthodes dans des classes, et contrôle l'accès à ces données.
- **Héritage** : Permet de créer des classes dérivées qui héritent des propriétés et comportements d’une classe existante.
- **Polymorphisme** : Permet aux objets de prendre plusieurs formes, ce qui favorise la flexibilité et l'extensibilité du code.
- **Abstraction** : Simplifie la complexité en ne montrant que les détails essentiels et en cachant l'implémentation interne.

#### 1.5 Sécurité et Robustesse

Java est conçu pour être un langage sécurisé et robuste. La JVM offre une couche de sécurité supplémentaire en vérifiant le bytecode avant l'exécution, et en limitant l’accès à certaines ressources du système pour éviter les erreurs et les comportements dangereux.

#### 1.6 Gestion Automatique de la Mémoire

Java intègre un **ramasse-miettes** (garbage collector), un processus qui gère automatiquement la libération de la mémoire inutilisée. Cela signifie que Java surveille et récupère la mémoire occupée par des objets qui ne sont plus utilisés, ce qui réduit les risques de fuite de mémoire et améliore la gestion des ressources.

#### 1.7 Multithreading et Concurrence

Java prend en charge le **multithreading**, permettant d’exécuter plusieurs tâches simultanément dans un seul programme. Cela est particulièrement utile pour les applications complexes nécessitant une exécution parallèle, comme les serveurs web ou les jeux.

## 2. Structure de base d'un programme

Un programme Java est structuré autour de classes et de méthodes. La structure de base est assez simple et suit des conventions strictes, notamment concernant le nommage des fichiers et l'utilisation de la méthode `main()` comme point d'entrée.

### Exemple de Structure de Base

Voici un exemple minimal de la structure d’un programme Java :

```java
public class MonProgramme {
    public static void main(String[] args) {
        // Code principal ici
    }
}
```

### Éléments de la Structure

Ce programme simple contient les éléments essentiels de tout programme Java : une classe publique et une méthode `main()`.

#### 2.1 Classe Publique

```{admonition} Définition : Classe Publique
En Java, chaque fichier `.java` doit contenir **au maximum une classe publique**. Une classe publique est accessible depuis d'autres classes et constitue un modèle pour créer des objets en définissant leurs caractéristiques (attributs) et leurs comportements (méthodes).
```

- **Nom de la Classe** : Le nom de la classe doit commencer par une majuscule par convention (par exemple, `MonProgramme`).
- **Nommage du Fichier** : Le fichier `.java` doit porter le même nom que la classe publique qu’il contient. Dans cet exemple, la classe publique est `MonProgramme`, donc le fichier devra être nommé `MonProgramme.java`. Toute divergence entre le nom du fichier et celui de la classe publique entraînera une erreur lors de la compilation.

#### 2.2 La Méthode `main()`

:::{admonition} Définition : Point d'Entrée du Programme
La méthode **`main()`** est le point d'entrée de tout programme Java. C’est la première méthode qui est exécutée lorsqu'un programme Java démarre. Elle suit la signature suivante :
```java
public static void main(String[] args)
```
:::

- **Signature** : La signature exacte de la méthode `main()` est obligatoire pour que la JVM identifie le point de départ du programme.
    - `public` : Cette méthode est accessible publiquement, permettant à la JVM de l'invoquer.
    - `static` : La méthode `main()` est statique, ce qui signifie qu'elle peut être appelée sans créer une instance de la classe.
    - `void` : La méthode `main()` ne renvoie aucune valeur.
    - `String[] args` : Elle prend un tableau de chaînes de caractères comme argument, permettant de passer des paramètres en ligne de commande au programme.
- **Bloc de Code** : C'est à l’intérieur de la méthode `main()` que le code principal de l'application est exécuté. Les instructions écrites ici seront exécutées lorsque le programme sera lancé.

#### 2.3 Les Commentaires

Java permet l'utilisation de commentaires pour rendre le code plus compréhensible sans affecter son exécution. Il existe trois types de commentaires en Java :
  
- **Commentaire sur une ligne** : Utilisez `//` pour ajouter un commentaire sur une seule ligne.
  ```java
  // Ceci est un commentaire sur une ligne
  ```
  
- **Commentaire sur plusieurs lignes** : Utilisez `/* ... */` pour des commentaires sur plusieurs lignes.
  ```java
  /*
   Ceci est un commentaire
   sur plusieurs lignes
  */
  ```
  
- **Commentaire de documentation** : Utilisez `/** ... */` pour générer automatiquement de la documentation.
  ```java
  /**
   * Ceci est un commentaire de documentation
   */
  ```

### Résumé de la Structure de Base

Un programme Java de base doit respecter les règles suivantes :

1. **Classe Publique** : Un fichier `.java` contient une classe publique, dont le nom correspond à celui du fichier.
2. **Méthode `main()`** : La méthode `main()` est le point d'entrée du programme et contient le code principal.
3. **Commentaires** : Ils sont utilisés pour documenter le code et faciliter la compréhension.


## 3. Types de données

En Java, les données sont classées en deux grandes catégories : les types primitifs et les types référence. Les types primitifs stockent des valeurs simples, tandis que les types référence permettent de manipuler des objets complexes.

### Types Primitifs

Les types primitifs sont les types de base de Java. Ils sont prédéfinis par le langage et représentent des valeurs simples comme des entiers, des décimaux, des caractères, et des valeurs booléennes. Les types primitifs sont directement stockés en mémoire et sont souvent utilisés pour leurs performances optimales.

| Type    | Taille  | Plage de valeurs                               | Exemple             |
|---------|---------|-----------------------------------------------|---------------------|
| byte    | 8 bits  | -128 à 127                                     | byte a = 100;       |
| short   | 16 bits | -32,768 à 32,767                               | short b = 1000;     |
| int     | 32 bits | -2^31 à 2^31-1                                | int c = 10000;      |
| long    | 64 bits | -2^63 à 2^63-1                                | long d = 100000L;   |
| float   | 32 bits | ±3.4e−038 à ±3.4e+038                          | float e = 3.14f;    |
| double  | 64 bits | ±1.7e−308 à ±1.7e+308                          | double f = 3.14;    |
| boolean | 1 bit   | true/false                                     | boolean g = true;   |
| char    | 16 bits | caractère Unicode                              | char h = 'A';       |

```{admonition} Remarque
Les types primitifs ont des tailles et des plages de valeurs spécifiques, ce qui est important pour gérer la mémoire de manière efficace et éviter des erreurs de dépassement de capacité.
```

#### Explications des Types Primitifs

- **byte** : Utilisé pour représenter de petits entiers. Ce type est généralement utilisé dans les applications où la mémoire est une contrainte majeure, comme les systèmes embarqués.
- **short** : Entier de taille moyenne, moins utilisé que `int` mais utile dans certaines applications spécifiques.
- **int** : Type le plus courant pour les entiers. Utilisé pour la plupart des calculs numériques.
- **long** : Utilisé lorsque la plage d'un `int` est insuffisante, notamment dans les calculs financiers.
- **float** : Type pour les nombres décimaux, précis jusqu'à 6 à 7 chiffres après la virgule. Le suffixe `f` indique un `float`.
- **double** : Utilisé pour des nombres décimaux de plus grande précision (jusqu'à 15 chiffres après la virgule).
- **boolean** : Type logique pour stocker les valeurs `true` ou `false`. Souvent utilisé dans les conditions.
- **char** : Représente un seul caractère Unicode, ce qui permet de manipuler n’importe quel symbole (lettres, chiffres, symboles spéciaux).

### Types Référence

Les types référence permettent de manipuler des objets et des structures de données plus complexes que les types primitifs. Ils ne stockent pas directement la valeur, mais une référence vers l’emplacement mémoire où l’objet est stocké.

Les types référence incluent :

- **String** : Représente une chaîne de caractères. Les objets `String` sont immuables, ce qui signifie qu'une fois créés, leur contenu ne peut pas être modifié.
- **Arrays (Tableaux)** : Structures de données permettant de stocker plusieurs éléments du même type.
- **Classes** : Les classes sont des modèles pour créer des objets. Elles définissent les attributs et les comportements des objets.
- **Interfaces** : Définissent un ensemble de méthodes que les classes peuvent implémenter. Elles permettent de réaliser une abstraction et de définir des comportements que différentes classes peuvent partager.

```{admonition} Note sur les Types Référence
Contrairement aux types primitifs, les types référence sont stockés en mémoire comme des objets. Leur manipulation est plus flexible mais peut nécessiter plus de mémoire.
```

### Exemple d'utilisation

Pour illustrer, voici un exemple de déclaration de différents types de données en Java :

```java
public class TypesDonnees {
    public static void main(String[] args) {
        byte a = 100;
        short b = 1000;
        int c = 10000;
        long d = 100000L;
        float e = 3.14f;
        double f = 3.14;
        boolean g = true;
        char h = 'A';
        String chaine = "Bonjour Java";
        
        System.out.println("Byte : " + a);
        System.out.println("Short : " + b);
        System.out.println("Int : " + c);
        System.out.println("Long : " + d);
        System.out.println("Float : " + e);
        System.out.println("Double : " + f);
        System.out.println("Boolean : " + g);
        System.out.println("Char : " + h);
        System.out.println("String : " + chaine);
    }
}
```











## 4. Variables et constantes

En Java, les variables et les constantes sont des éléments essentiels pour stocker et manipuler des données dans un programme. Les variables sont des conteneurs de valeurs qui peuvent être modifiées au cours de l'exécution, tandis que les constantes sont des valeurs fixes, définies une fois et non modifiables.

### Déclaration de Variables

Une variable est un espace mémoire réservé pour stocker une valeur d'un type spécifique. La déclaration d'une variable en Java suit généralement la syntaxe suivante :

```java
type nomVariable = valeur;
```

#### Exemple de Variables

```java
// Déclaration et initialisation de variables
int nombre = 10;
String texte = "Hello";
```

Dans cet exemple :
- `int nombre = 10;` : déclare une variable de type `int` (entier) nommée `nombre` et lui assigne la valeur `10`.
- `String texte = "Hello";` : déclare une variable de type `String` (chaîne de caractères) nommée `texte` et lui assigne la valeur `"Hello"`.

### Règles de Nommage des Variables

Les noms des variables en Java doivent respecter certaines règles et conventions :
- Ils doivent commencer par une lettre (a-z ou A-Z), un dollar `$`, ou un tiret bas `_`. Les caractères suivants peuvent être des lettres, des chiffres (0-9), des dollars `$`, ou des tirets bas `_`.
- Ils ne peuvent pas contenir d'espaces ni de caractères spéciaux (à l'exception de `$` et `_`).
- Les noms des variables sont sensibles à la casse (`nombre` et `Nombre` sont différents).
  
**Conventions** :
- Utiliser le style camelCase pour les noms de variables (ex. `monNombre`, `texteUtilisateur`).
- Les noms de variables doivent être significatifs pour faciliter la compréhension du code.

### Déclaration de Constantes

Une constante est une valeur fixe qui ne peut pas être modifiée une fois définie. En Java, on utilise le mot-clé `final` pour déclarer une constante. Par convention, les noms des constantes sont écrits en majuscules.

```{admonition} Définition : Constante
Une constante en Java est une variable qui, une fois initialisée, ne peut plus être modifiée. On la déclare avec le mot-clé `final` et un nom en majuscules pour indiquer qu'elle est immuable.
```

#### Exemple de Constantes

```java
// Déclaration d'une constante
final double PI = 3.14159;
```

Dans cet exemple :
- `final double PI = 3.14159;` : déclare une constante de type `double` nommée `PI` et lui assigne la valeur `3.14159`. Le mot-clé `final` empêche toute modification de `PI` après son initialisation.

### Exemple Complet : Variables et Constantes

Voici un exemple illustrant l'utilisation de variables et de constantes dans un programme Java :

```java
public class ExempleVariablesConstantes {
    public static void main(String[] args) {
        // Variables
        int nombre = 10;
        String texte = "Hello";
        
        // Constante
        final double PI = 3.14159;
        
        // Affichage des valeurs
        System.out.println("Variable nombre : " + nombre);
        System.out.println("Variable texte : " + texte);
        System.out.println("Constante PI : " + PI);
    }
}
```

Dans ce programme :
- `nombre` et `texte` sont des variables dont les valeurs peuvent être modifiées.
- `PI` est une constante définie avec `final`, et sa valeur reste la même tout au long de l'exécution du programme.

### Résumé

- **Variables** : Conteneurs de valeurs qui peuvent être modifiées. Utilisez un nom significatif en camelCase.
- **Constantes** : Valeurs fixes définies avec `final` et nommées en majuscules. Elles ne peuvent pas être modifiées après l'initialisation.


