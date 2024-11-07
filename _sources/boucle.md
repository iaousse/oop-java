# Structures de Contrôle, Tableaux, Méthodes et Gestion des Exceptions

## 1. Structures de contrôle

Les structures de contrôle en Java permettent de diriger le flux d’exécution d’un programme en fonction de conditions et de répétitions. Elles se divisent en deux grandes catégories : les structures conditionnelles (`if-else`, `switch`) et les structures de boucle (`for`, `while`, `do-while`, `for-each`).

### If-Else

La structure `if-else` permet d’exécuter des blocs de code spécifiques en fonction de conditions.

:::{admonition} Définition : If-Else
La structure `if-else` est utilisée pour évaluer une ou plusieurs conditions. Si la condition `if` est vraie, le bloc de code associé est exécuté. Si elle est fausse et qu'il y a une condition `else if`, celle-ci est testée. Enfin, si toutes les conditions sont fausses, le bloc `else` est exécuté.
:::

:::{admonition} Syntaxe
```java
if (condition) {
    // code exécuté si la condition est vraie
} else if (autreCondition) {
    // code exécuté si l’autre condition est vraie
} else {
    // code exécuté si toutes les conditions sont fausses
}
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 1 : Vérification d'une note**
```java
int note = 85;
if (note >= 90) {
    System.out.println("Excellence");
} else if (note >= 75) {
    System.out.println("Très bien");
} else {
    System.out.println("Peut mieux faire");
}
```

**Exemple 2 : Vérification de la parité d’un nombre**
```java
int nombre = 4;
if (nombre % 2 == 0) {
    System.out.println(nombre + " est pair");
} else {
    System.out.println(nombre + " est impair");
}
```
:::

### Switch

La structure `switch` est utilisée pour tester une seule variable contre plusieurs valeurs possibles et exécuter un bloc de code spécifique en fonction de la correspondance trouvée.

:::{admonition} Définition : Switch
La structure `switch` compare la valeur d’une variable avec plusieurs cas (`case`). Lorsqu'une correspondance est trouvée, le code associé est exécuté. L'instruction `break` permet de quitter le bloc `switch` une fois un cas traité, et `default` est exécuté si aucune correspondance n’est trouvée.
:::

:::{admonition} Syntaxe
```java
switch (variable) {
    case valeur1:
        // code exécuté si variable == valeur1
        break;
    case valeur2:
        // code exécuté si variable == valeur2
        break;
    default:
        // code exécuté si aucune correspondance trouvée
}
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 3 : Affichage du jour de la semaine**
```java
int jour = 3;
switch (jour) {
    case 1:
        System.out.println("Lundi");
        break;
    case 2:
        System.out.println("Mardi");
        break;
    case 3:
        System.out.println("Mercredi");
        break;
    default:
        System.out.println("Jour non valide");
}
```

**Exemple 4 : Sélection d'un niveau de priorité**
```java
int priorite = 1;
switch (priorite) {
    case 1:
        System.out.println("Priorité haute");
        break;
    case 2:
        System.out.println("Priorité moyenne");
        break;
    case 3:
        System.out.println("Priorité basse");
        break;
    default:
        System.out.println("Priorité non définie");
}
```
:::

### Boucles

Les boucles permettent de répéter un bloc de code tant qu'une condition est vraie ou pour un nombre déterminé de répétitions. Les boucles les plus courantes en Java sont `for`, `while`, `do-while`, et `for-each`.

#### Boucle For

La boucle `for` est idéale pour exécuter une action un nombre défini de fois.

:::{admonition} Définition : Boucle For
La boucle `for` utilise trois éléments : une initialisation, une condition, et une incrémentation. Elle répète le bloc de code tant que la condition reste vraie.
:::

:::{admonition} Syntaxe
```java
for (initialisation; condition; incrémentation) {
    // code répété
}
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 5 : Affichage de nombres de 1 à 5**
```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Nombre : " + i);
}
```

**Exemple 6 : Affichage des nombres pairs de 2 à 10**
```java
for (int i = 2; i <= 10; i += 2) {
    System.out.println("Nombre pair : " + i);
}
```
:::

#### Boucle While

La boucle `while` exécute un bloc de code tant qu’une condition est vraie. Elle est souvent utilisée lorsque le nombre de répétitions n'est pas connu à l'avance.

:::{admonition} Définition : Boucle While
La boucle `while` répète un bloc de code tant qu'une condition est vraie. Elle vérifie la condition avant d'exécuter le bloc de code.
:::

:::{admonition} Syntaxe
```java
while (condition) {
    // code répété tant que la condition est vraie
}
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 7 : Compteur décroissant de 5 à 1**
```java
int compteur = 5;
while (compteur > 0) {
    System.out.println("Compte à rebours : " + compteur);
    compteur--;
}
```

**Exemple 8 : Affichage d'une série jusqu'à un maximum donné**
```java
int valeur = 1;
int max = 5;
while (valeur <= max) {
    System.out.println("Valeur actuelle : " + valeur);
    valeur++;
}
```
:::

#### Boucle Do-While

La boucle `do-while` est similaire à `while`, mais elle garantit que le bloc de code est exécuté au moins une fois, car la condition est vérifiée après l'exécution.

:::{admonition} Définition : Boucle Do-While
La boucle `do-while` exécute le bloc de code, puis vérifie la condition pour déterminer si elle doit se répéter. Le code est toujours exécuté au moins une fois.
:::

:::{admonition} Syntaxe
```java
do {
    // code exécuté au moins une fois
} while (condition);
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 9 : Exécution d'une tâche jusqu'à ce qu'une condition soit atteinte**
```java
int essai = 0;
do {
    System.out.println("Essai numéro : " + essai);
    essai++;
} while (essai < 3);
```

**Exemple 10 : Vérification répétée jusqu’à une valeur cible**
```java
int compteur = 1;
do {
    System.out.println("Compteur actuel : " + compteur);
    compteur++;
} while (compteur <= 5);
```
:::

#### Boucle For-Each

La boucle `for-each` est utilisée pour parcourir des éléments lorsque la taille ou le nombre d'éléments est connu. Cette structure est simple et lisible, adaptée aux éléments individuels lorsque l'index n'est pas nécessaire.

:::{admonition} Définition : Boucle For-Each
La boucle `for-each` permet de parcourir chaque élément d’une collection d’éléments ou d’un ensemble de valeurs définies.
:::

:::{admonition} Syntaxe
```java
for (Type element : ensemble) {
    // code pour chaque élément
}
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 11 : Affichage de notes individuelles**
```java
int[] notes = {90, 85, 75, 60};
for (int note : notes) {
    System.out.println("Note : " + note);
}
```

**Exemple 12 : Affichage de valeurs prédéfinies**
```java
int[] valeurs = {1, 3, 5, 7};
for (int valeur : valeurs) {
    System.out.println("Valeur : " + valeur);
}
```
:::


## 2. Tableaux

En Java, les tableaux sont des structures de données qui permettent de stocker plusieurs éléments du même type dans une seule variable. Ils sont très utiles pour gérer des groupes de valeurs.

:::{admonition} Déclaration et Initialisation d'un Tableau
Pour déclarer un tableau en Java, vous devez spécifier le type d’éléments qu’il contiendra, suivi de `[]`. La taille du tableau doit être définie à la création ou vous pouvez directement l’initialiser avec des valeurs spécifiques.
:::

:::{admonition} Syntaxe
```java
// Déclaration d'un tableau avec une taille définie
int[] tableau = new int[5]; // tableau vide de 5 éléments

// Déclaration et initialisation d'un tableau avec des valeurs
int[] nombres = {1, 2, 3, 4, 5}; // tableau initialisé avec 5 éléments
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 13 : Initialisation et remplissage d'un tableau**
```java
int[] tableau = new int[3];
tableau[0] = 10; // assignation de la première valeur
tableau[1] = 20; // assignation de la deuxième valeur
tableau[2] = 30; // assignation de la troisième valeur

System.out.println("Exemple 13 - Valeurs du tableau : " + tableau[0] + ", " + tableau[1] + ", " + tableau[2]);
```

**Exemple 14 : Déclaration avec valeurs prédéfinies**
```java
int[] notes = {90, 85, 75, 60, 95}; // tableau de notes

System.out.println("Exemple 14 - Première note : " + notes[0]);
System.out.println("Exemple 14 - Dernière note : " + notes[4]);
```
:::

### Accès aux éléments d'un Tableau

Une fois un tableau créé, vous pouvez accéder à chaque élément en utilisant son index. Les index commencent à 0 pour le premier élément.

:::{admonition} Exemples d'Accès et de Modification
**Exemple 15 : Modification et lecture des éléments**
```java
int[] valeurs = {5, 10, 15};
valeurs[1] = 20; // modification du deuxième élément
int valeur = valeurs[1]; // lecture de la nouvelle valeur

System.out.println("Exemple 15 - Nouvelle valeur au second index : " + valeur);
```

**Exemple 16 : Parcours d'un tableau**
```java
int[] nombres = {2, 4, 6, 8};
for (int i = 0; i < nombres.length; i++) {
    System.out.println("Exemple 16 - Valeur à l'index " + i + " : " + nombres[i]);
}
```
:::

---

## 3. Méthodes (Fonctions)

Les méthodes en Java sont des blocs de code qui réalisent une tâche spécifique et qui peuvent être appelés depuis d'autres parties du programme. Les méthodes permettent de structurer le code, d'améliorer la réutilisabilité et de réduire la redondance.

### Définition d'une Méthode

Une méthode est définie par un type de retour, un nom, et éventuellement des paramètres. 

:::{admonition} Structure d'une Méthode
- **Type de retour** : indique le type de données que la méthode retourne (`void` si elle ne retourne rien).
- **Nom de la méthode** : nom choisi pour la méthode, en camelCase par convention.
- **Paramètres** : liste d'arguments entre parenthèses, qui peuvent être utilisés à l'intérieur de la méthode.
:::

### Méthodes sans Retour

Une méthode sans retour exécute une action mais ne renvoie aucune valeur. Son type de retour est `void`.

:::{admonition} Syntaxe
```java
public void afficher(String message) {
    System.out.println(message);
}
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 17 : Afficher un message**
```java
public void afficherMessage() {
    System.out.println("Exemple 17 - Bienvenue dans le cours de Java !");
}
```
:::
### Méthodes avec Retour

Les méthodes avec retour effectuent une opération et renvoient un résultat. Le type de retour est spécifié dans la définition de la méthode.

:::{admonition} Syntaxe
```java
public int additionner(int a, int b) {
    return a + b;
}
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 18 : Calcul d'une somme**
```java
public int calculerSomme() {
    int x = 5;
    int y = 10;
    int somme = additionner(x, y); // appelle la méthode additionner
    return somme;
}

public int additionner(int a, int b) {
    return a + b;
}
```

**Exemple 19 : Calcul d’une différence**
```java
public int soustraction(int a, int b) {
    return a - b;
}

int resultat = soustraction(15, 5);
System.out.println("Exemple 19 - Résultat de la soustraction : " + resultat);
```
:::

### Méthodes Statique

Les méthodes statiques appartiennent à la classe elle-même plutôt qu’à une instance de la classe. Elles peuvent être appelées sans créer d’objet de la classe.

:::{admonition} Syntaxe
```java
public static double multiplier(double a, double b) {
    return a * b;
}
```
:::

:::{admonition} Exemples d'Utilisation
**Exemple 20 : Calculer un produit avec une méthode statique**
```java
public static double calculerProduit(double x, double y) {
    return x * y;
}

public static void main(String[] args) {
    double produit = calculerProduit(5.5, 3.2);
    System.out.println("Exemple 20 - Produit : " + produit);
}
```

**Exemple 21 : Calcul d'un quotient avec une méthode statique**
```java
public static double diviser(double a, double b) {
    if (b != 0) {
        return a / b;
    } else {
        System.out.println("Division par zéro impossible.");
        return 0;
    }
}

double resultatDivision = diviser(10.0, 2.0);
System.out.println("Exemple 21 - Résultat de la division : " + resultatDivision);
```
:::









## 4. Gestion des Exceptions

En Java, les exceptions sont des événements qui surviennent lors de l'exécution d'un programme et qui perturbent le flux normal des instructions. La gestion des exceptions permet de traiter ces situations sans interrompre brutalement le programme. Le bloc `try-catch-finally` est l’un des mécanismes les plus courants pour gérer les exceptions en Java.

### Structure de Base de la Gestion des Exceptions

:::{admonition} Définition : Bloc try-catch-finally
Le bloc `try` contient le code susceptible de générer une exception. Si une exception se produit, le contrôle passe au bloc `catch` associé, où l’on peut traiter l’erreur. Le bloc `finally` est optionnel et s'exécute dans tous les cas, que l'exception ait été levée ou non.
:::

:::{admonition} Syntaxe
```java
try {
    // code susceptible de générer une exception
} catch (Exception e) {
    // traitement de l'exception
} finally {
    // code exécuté dans tous les cas
}
```
:::

### Exemples d'Utilisation

**Exemple 22 : Gestion de la division par zéro**
Dans cet exemple, nous utilisons `try-catch` pour gérer une éventuelle division par zéro.

```java
public class DivisionParZero {
    public static void main(String[] args) {
        try {
            int resultat = 10 / 0;
            System.out.println("Résultat : " + resultat);
        } catch (ArithmeticException e) {
            System.out.println("Exemple 22 - Erreur : Division par zéro");
        }
    }
}
```

**Exemple 23 : Accès à un élément hors limites dans un tableau**
Lorsqu’on accède à un index qui n’existe pas dans un tableau, une `ArrayIndexOutOfBoundsException` est levée.

```java
public class AccesHorsLimites {
    public static void main(String[] args) {
        int[] tableau = {1, 2, 3};
        try {
            int valeur = tableau[5]; // accès hors limites
            System.out.println("Valeur : " + valeur);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Exemple 23 - Erreur : Index hors limites dans le tableau");
        }
    }
}
```

**Exemple 24 : Gestion de plusieurs exceptions**
Il est possible de gérer plusieurs types d’exceptions en utilisant plusieurs blocs `catch`.

```java
public class MultipleExceptions {
    public static void main(String[] args) {
        try {
            int[] tableau = new int[3];
            tableau[3] = 10; // génère ArrayIndexOutOfBoundsException
            int resultat = 10 / 0; // génère ArithmeticException
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Exemple 24 - Erreur : Index hors limites");
        } catch (ArithmeticException e) {
            System.out.println("Exemple 24 - Erreur : Division par zéro");
        }
    }
}
```

**Exemple 25 : Utilisation du bloc finally**
Le bloc `finally` s'exécute toujours, que l’exception soit levée ou non. Il est souvent utilisé pour libérer des ressources comme des fichiers ou des connexions.

```java
public class BlocFinally {
    public static void main(String[] args) {
        try {
            int resultat = 10 / 2;
            System.out.println("Résultat : " + resultat);
        } catch (ArithmeticException e) {
            System.out.println("Erreur : Division par zéro");
        } finally {
            System.out.println("Exemple 25 - Bloc finally exécuté, libération des ressources.");
        }
    }
}
```

### Lancer une Exception

Parfois, il est nécessaire de lever manuellement une exception. Cela se fait avec l’instruction `throw`, suivie d’une instance de l'exception.

:::{admonition} Syntaxe
```java
throw new ExceptionType("Message d'erreur");
```
:::

**Exemple 26 : Lever une exception personnalisée**
Dans cet exemple, une exception est levée manuellement si une valeur négative est passée comme paramètre.

```java
public class ExceptionPersonnalisee {
    public static void main(String[] args) {
        try {
            verifierValeur(-5);
        } catch (IllegalArgumentException e) {
            System.out.println("Exemple 26 - Erreur : " + e.getMessage());
        }
    }

    public static void verifierValeur(int valeur) {
        if (valeur < 0) {
            throw new IllegalArgumentException("La valeur ne peut pas être négative");
        }
    }
}
```

### Exemples avancés

**Exemple 27 : Gestion des exceptions dans une méthode avec `throws`**
Lorsqu'une méthode peut lever une exception, on peut l'indiquer avec le mot-clé `throws`. Cela signifie que la méthode appelante doit gérer l'exception ou la propager.

```java
public class MethodeAvecThrows {
    public static void main(String[] args) {
        try {
            diviser(10, 0);
        } catch (ArithmeticException e) {
            System.out.println("Exemple 27 - Erreur : " + e.getMessage());
        }
    }

    public static int diviser(int a, int b) throws ArithmeticException {
        if (b == 0) {
            throw new ArithmeticException("Division par zéro non autorisée");
        }
        return a / b;
    }
}
```

**Exemple 28 : Utilisation des exceptions pour valider des entrées**
Les exceptions peuvent aussi être utilisées pour valider des entrées et renvoyer des messages d'erreur appropriés.

```java
public class ValidationEntree {
    public static void main(String[] args) {
        try {
            verifierAge(15); // provoque une exception
        } catch (Exception e) {
            System.out.println("Exemple 28 - Erreur : " + e.getMessage());
        }
    }

    public static void verifierAge(int age) throws Exception {
        if (age < 18) {
            throw new Exception("L'âge doit être de 18 ans ou plus");
        }
    }
}
```



