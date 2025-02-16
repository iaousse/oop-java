# Opérations et Comparaisons en Java 

Les opérateurs en Java permettent de réaliser des opérations sur des valeurs. Ils se divisent en plusieurs catégories : arithmétiques, de comparaison et logiques. Voici une description détaillée de chaque catégorie d’opérateurs avec des exemples progressifs pour une meilleure compréhension.

### Opérateurs arithmétiques

Les opérateurs arithmétiques permettent d’effectuer des calculs mathématiques de base sur des nombres.

```{admonition} Définition : Opérateurs Arithmétiques
Les opérateurs arithmétiques en Java incluent :
- `+` : addition
- `-` : soustraction
- `*` : multiplication
- `/` : division
- `%` : modulo (reste de la division)
```

:::{admonition} Exemples d'Utilisation
**Exemple 1 : Addition (`+`)**
```java
int a = 15;
int b = 7;
int somme = a + b; // somme vaut 22
System.out.println("Exemple 1 - La somme de " + a + " et " + b + " est : " + somme);
```

**Exemple 2 : Soustraction (`-`)**
```java
int resultat = a - b; // resultat vaut 8
System.out.println("Exemple 2 - La différence entre " + a + " et " + b + " est : " + resultat);

int c = 20;
int d = 25;
int difference = c - d; // difference vaut -5
System.out.println("Exemple 3 - La différence entre " + c + " et " + d + " est : " + difference);
```

**Exemple 3 : Multiplication (`*`)**
```java
int produit = a * b; // produit vaut 105
System.out.println("Exemple 4 - Le produit de " + a + " et " + b + " est : " + produit);

int e = 4;
int f = 5;
int produit2 = e * f; // produit2 vaut 20
System.out.println("Exemple 5 - Le produit de " + e + " et " + f + " est : " + produit2);
```

**Exemple 4 : Division (`/`)**
```java
int division = a / b; // division vaut 2, car c'est une division entière
System.out.println("Exemple 6 - La division entière de " + a + " par " + b + " est : " + division);

double x = 15.0;
double y = 4.0;
double resultatDivision = x / y; // résultat vaut 3.75
System.out.println("Exemple 7 - La division réelle de " + x + " par " + y + " est : " + resultatDivision);
```

**Exemple 5 : Modulo (`%`)**
```java
int reste = a % b; // reste vaut 1, car 15 mod 7 = 1
System.out.println("Exemple 8 - Le reste de la division de " + a + " par " + b + " est : " + reste);

int g = 9;
int reste2 = g % 2; // reste2 vaut 1, car 9 n'est pas divisible par 2
System.out.println("Exemple 9 - Le reste de la division de " + g + " par 2 est : " + reste2);
```
:::

---
### Les Opérations Postfix et Prefix (++)

**Définitions :**
- **Préfix (++a)** : L'opérateur incrémente la valeur de la variable avant que l'expression ne soit évaluée.
- **Postfix (a++)** : L'opérateur incrémente la valeur de la variable après que l'expression ne soit évaluée.

**Exemples en Java :**

**Préfix (++a)**
```java
int a = 5;
int b = ++a; // a devient 6, puis b reçoit la valeur de a, donc b vaut aussi 6
System.out.println("a : " + a + ", b : " + b); // Affiche a : 6, b : 6
```

**Postfix (a++)**
```java
int a = 5;
int b = a++; // b reçoit la valeur de a, donc b vaut 5, puis a est incrémenté à 6
System.out.println("a : " + a + ", b : " + b); // Affiche a : 6, b : 5
```


### Opérateurs de comparaison

Les opérateurs de comparaison permettent de comparer deux valeurs. Le résultat de ces comparaisons est toujours un type `boolean` (`true` ou `false`).

```{admonition} Définition : Opérateurs de Comparaison
Les opérateurs de comparaison en Java incluent :
- `==` : égal à
- `!=` : différent de
- `>` : supérieur à
- `<` : inférieur à
- `>=` : supérieur ou égal à
- `<=` : inférieur ou égal à
```

:::{admonition} Exemples d'Utilisation
**Exemple 6 : Égalité (`==`)**
```java
int a = 15;
int b = 7;
boolean egal = (a == b); // egal vaut false
System.out.println("Exemple 10 - Est-ce que " + a + " est égal à " + b + " ? : " + egal);

boolean egal2 = (a == 15); // egal2 vaut true
System.out.println("Exemple 11 - Est-ce que " + a + " est égal à 15 ? : " + egal2);
```

**Exemple 7 : Différence (`!=`)**
```java
boolean different = (a != b); // different vaut true
System.out.println("Exemple 12 - Est-ce que " + a + " est différent de " + b + " ? : " + different);

boolean different2 = (a != 15); // different2 vaut false
System.out.println("Exemple 13 - Est-ce que " + a + " est différent de 15 ? : " + different2);
```

**Exemple 8 : Supérieur (`>`)**
```java
boolean superieur = (a > b); // superieur vaut true
System.out.println("Exemple 14 - Est-ce que " + a + " est supérieur à " + b + " ? : " + superieur);

int c = 10;
boolean superieur2 = (b > c); // superieur2 vaut false
System.out.println("Exemple 15 - Est-ce que " + b + " est supérieur à " + c + " ? : " + superieur2);
```

**Exemple 9 : Inférieur (`<`)**
```java
boolean inferieur = (a < b); // inferieur vaut false
System.out.println("Exemple 16 - Est-ce que " + a + " est inférieur à " + b + " ? : " + inferieur);

boolean inferieur2 = (c < a); // inferieur2 vaut true
System.out.println("Exemple 17 - Est-ce que " + c + " est inférieur à " + a + " ? : " + inferieur2);
```

**Exemple 10 : Supérieur ou égal (`>=`)**
```java
boolean superieurOuEgal = (a >= b); // superieurOuEgal vaut true
System.out.println("Exemple 18 - Est-ce que " + a + " est supérieur ou égal à " + b + " ? : " + superieurOuEgal);

boolean superieurOuEgal2 = (a >= 15); // superieurOuEgal2 vaut true
System.out.println("Exemple 19 - Est-ce que " + a + " est supérieur ou égal à 15 ? : " + superieurOuEgal2);
```

**Exemple 11 : Inférieur ou égal (`<=`)**
```java
boolean inferieurOuEgal = (a <= b); // inferieurOuEgal vaut false
System.out.println("Exemple 20 - Est-ce que " + a + " est inférieur ou égal à " + b + " ? : " + inferieurOuEgal);

boolean inferieurOuEgal2 = (a <= 15); // inferieurOuEgal2 vaut true
System.out.println("Exemple 21 - Est-ce que " + a + " est inférieur ou égal à 15 ? : " + inferieurOuEgal2);
```
:::

---

### Opérateurs logiques

Les opérateurs logiques permettent de combiner plusieurs expressions booléennes. Ils sont souvent utilisés dans les conditions pour évaluer des expressions complexes.

```{admonition} Définition : Opérateurs Logiques
Les opérateurs logiques en Java incluent :
- `&&` : ET logique (retourne `true` si les deux conditions sont vraies)
- `||` : OU logique (retourne `true` si au moins une des deux conditions est vraie)
- `!` : NON logique (inverse la valeur booléenne)
```

:::{admonition} Exemples d'Utilisation
**Exemple 12 : ET logique (`&&`)**
```java
boolean condition1 = (5 > 3); // true
boolean condition2 = (10 > 5); // true
boolean etLogique = condition1 && condition2; // etLogique vaut true
System.out.println("Exemple 22 - Les deux conditions (5 > 3 et 10 > 5) sont-elles vraies ? : " + etLogique);

boolean condition3 = (5 > 10); // false
boolean etLogique2 = condition1 && condition3; // etLogique2 vaut false
System.out.println("Exemple 23 - Les deux conditions (5 > 3 et 5 > 10) sont-elles vraies ? : " + etLogique2);
```

**Exemple 13 : OU logique (`||`)**
```java
boolean ouLogique = condition1 || condition3; // ouLogique vaut true
System.out.println("Exemple 24 - Au moins une des conditions (5 > 3 ou 5 > 10) est-elle vraie ? : " + ouLogique);

boolean condition4 = (3 > 7); // false
boolean ouLogique2 = condition3 || condition4; // ouLogique2 vaut false
System.out.println("Exemple 25 - Au moins une des conditions (5 > 10 ou 3 > 7) est-elle vraie ? : " + ouLogique2);
```

**Exemple 14 : NON logique (`!`)**
```java
boolean nonLogique = !condition1; // nonLogique vaut false car condition1 est true
System.out.println("Exemple 26 - L'inverse de la condition (5 > 3) est : " + nonLogique);

boolean condition5 = (10 == 20); // false
boolean nonLogique2 = !condition5; // nonLogique2 vaut true
System.out.println("Exemple 27 - L'inverse de la condition (10 == 20) est : " + nonLogique2);
```

**Exemple 15 : Expression avec `&&` et `||`**
```java
int age = 25;
boolean majeur = (age >= 18); // true
boolean permisDeConduire = true; // possède un permis
boolean peutConduire = majeur && permisDeConduire; // peutConduire vaut true
System.out.println("Exemple 28 - Est-ce que l'individu est majeur et a un permis ? : " + peutConduire);

boolean jeuneAdulte = (age >= 18 && age <= 30);
System.out.println("Exemple 29 - L'individu est-il un jeune adulte (entre 18 et 30 ans) ? : " + jeuneAdulte);
```
:::

## Saisie des données utilisateur en Java

### Introduction

En Java, la classe `Scanner` est couramment utilisée pour lire les entrées de l'utilisateur à partir de la console. Elle permet de lire différents types de données, y compris les entiers, les flottants et les chaînes de caractères. Voici un guide détaillé sur la façon de permettre à l'utilisateur d'entrer un nombre, ainsi que les raisons derrière chaque étape.

### Étapes 

1. **Importer la Classe Scanner :**
   - Avant d'utiliser la classe `Scanner`, vous devez l'importer. Cela se fait en utilisant l'instruction `import java.util.Scanner;`.
   - **Raison :** La classe `Scanner` se trouve dans le package `java.util`, qui n'est pas automatiquement importé.

   ```java
   import java.util.Scanner;
   ```

2. **Créer une Instance de Scanner :**
   - Vous devez créer une instance de la classe `Scanner` en passant `System.in` comme argument au constructeur de `Scanner`.
   - **Raison :** `System.in` est l'entrée standard (généralement le clavier) à partir de laquelle le `Scanner` lira les données.

   ```java
   Scanner scanner = new Scanner(System.in);
   ```

3. **Afficher un Message à l'Utilisateur :**
   - Avant de lire l'entrée de l'utilisateur, il est utile d'afficher un message demandant à l'utilisateur d'entrer un nombre.
   - **Raison :** Cela informe l'utilisateur sur ce qu'il doit faire.

   ```java
   System.out.println("Veuillez entrer un nombre :");
   ```

4. **Lire l'Entrée de l'Utilisateur :**
   - Utilisez la méthode `nextInt()` de l'objet `Scanner` pour lire un entier à partir de l'entrée de l'utilisateur.
   - **Raison :** `nextInt()` lit l'entrée suivante comme un entier. Si l'utilisateur entre une valeur qui n'est pas un entier, une `InputMismatchException` sera lancée.

   ```java
   int nombre = scanner.nextInt();
   ```

5. **Afficher le Nombre Entré :**
   - Après avoir lu l'entrée de l'utilisateur, vous pouvez afficher le nombre pour confirmer que la lecture s'est bien déroulée.
   - **Raison :** Cela permet de vérifier que l'entrée a été lue correctement.

   ```java
   System.out.println("Vous avez entré le nombre : " + nombre);
   ```

6. **Fermer le Scanner :**
   - Une fois que vous avez terminé d'utiliser le `Scanner`, il est recommandé de le fermer en appelant `scanner.close()`.
   - **Raison :** Cela libère les ressources associées au `Scanner`.

   ```java
   scanner.close();
   ```

### Exemple 

Voici un exemple complet qui met en œuvre toutes les étapes ci-dessus :

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Créer une instance de Scanner
        Scanner scanner = new Scanner(System.in);
        
        // Afficher un message à l'utilisateur
        System.out.println("Veuillez entrer un nombre :");
        
        // Lire l'entrée de l'utilisateur
        int nombre = scanner.nextInt();
        
        // Afficher le nombre entré
        System.out.println("Vous avez entré le nombre : " + nombre);
        
        // Fermer le Scanner
        scanner.close();
    }
}
```


## Exercices

1. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   - `int a = 5, b = 10, c = 0;`
   - `c = a++ + b;`
   - `c = ++a + b;`

2. **Évaluer les expressions logiques suivantes et afficher le résultat :**
   - `int x = 5, y = 8;`
   - `boolean res1 = (x < y) && (++x == y);`
   - `boolean res2 = (x == y) || (y++ > x);`

3. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   - `int a = 3, b = 6, c = 1;`
   - `c = ++a * b--;`

4. **Comparer deux valeurs en utilisant des opérateurs logiques et afficher le résultat :**
   - `int m = 7, n = 7;`
   - `boolean res = (m == n) && (m++ < ++n);`

5. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   - `int p = 10, q = 3;`
   - `p = p++ + --q * p;`

6. **Combiner des opérations arithmétiques et logiques pour évaluer les expressions et afficher le résultat :**
   - `int u = 4, v = 9;`
   - `boolean res3 = (u++ + v > 10) || (--v - u <= 3);`

1. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   - `int a = 3, b = 5, c = 0;`
   - `c = a + b * 2;`

2. **Calculer le résultat de l'expression suivante en utilisant les parenthèses et afficher le résultat :**
   - `int a = 3, b = 5;`
   - `int resultat = (a + b) * 2;`

3. **Évaluer l'expression suivante et afficher la valeur finale de la variable :**
   - `int x = 10;`
   - `x = x++ * 2 + 3;`

4. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   - `int a = 4, b = 7, c = 10;`
   - `c = a * b - c / 2;`

5. **Calculer le résultat de l'expression suivante en utilisant les opérateurs de pré-incrémentation et de post-incrémentation :**
   - `int a = 5, b = 6;`
   - `int resultat = ++a * b--;`

6. **Évaluer l'expression suivante et afficher la valeur finale des variables :**
   - `int p = 8, q = 4;`
   - `p = p / 2 * (q + 3) - p++;`


## Solution

1. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   ```java
   int a = 5, b = 10, c = 0;
   c = a++ + b; // c = 5 + 10 = 15, a devient 6
   c = ++a + b; // a devient 7, c = 7 + 10 = 17
   System.out.println("a : " + a + ", b : " + b + ", c : " + c);
   ```

2. **Évaluer les expressions logiques suivantes et afficher le résultat :**
   ```java
   int x = 5, y = 8;
   boolean res1 = (x < y) && (++x == y); // res1 = true, x devient 6
   boolean res2 = (x == y) || (y++ > x); // res2 = true, y devient 9
   System.out.println("res1 : " + res1 + ", res2 : " + res2);
   ```

3. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   ```java
   int a = 3, b = 6, c = 1;
   c = ++a * b--; // a devient 4, c = 4 * 6 = 24, b devient 5
   System.out.println("a : " + a + ", b : " + b + ", c : " + c);
   ```

4. **Comparer deux valeurs en utilisant des opérateurs logiques et afficher le résultat :**
   ```java
   int m = 7, n = 7;
   boolean res = (m == n) && (m++ < ++n); // res = true, m devient 8, n devient 8
   System.out.println("m : " + m + ", n : " + n + ", res : " + res);
   ```

5. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   ```java
   int p = 10, q = 3;
   p = p++ + --q * p; // q devient 2, p = 10 + 2 * 10 = 30
   System.out.println("p : " + p + ", q : " + q);
   ```

6. **Combiner des opérations arithmétiques et logiques pour évaluer les expressions et afficher le résultat :**
   ```java
   int u = 4, v = 9;
   boolean res3 = (u++ + v > 10) || (--v - u <= 3); // res3 = true, u devient 5, v devient 8
   System.out.println("u : " + u + ", v : " + v + ", res3 : " + res3);
   ```
1. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   ```java
   int a = 3, b = 5, c = 0;
   c = a + b * 2; // c = 3 + 5 * 2 = 3 + 10 = 13
   System.out.println("a : " + a + ", b : " + b + ", c : " + c);
   ```

2. **Calculer le résultat de l'expression suivante en utilisant les parenthèses et afficher le résultat :**
   ```java
   int a = 3, b = 5;
   int resultat = (a + b) * 2; // resultat = (3 + 5) * 2 = 8 * 2 = 16
   System.out.println("a : " + a + ", b : " + b + ", resultat : " + resultat);
   ```

3. **Évaluer l'expression suivante et afficher la valeur finale de la variable :**
   ```java
   int x = 10;
   x = x++ * 2 + 3; // x = 10 * 2 + 3 = 20 + 3 = 23, puis x devient 11
   System.out.println("x : " + x);
   ```

4. **Calculer le résultat de l'expression suivante et afficher la valeur finale des variables :**
   ```java
   int a = 4, b = 7, c = 10;
   c = a * b - c / 2; // c = 4 * 7 - 10 / 2 = 28 - 5 = 23
   System.out.println("a : " + a + ", b : " + b + ", c : " + c);
   ```

5. **Calculer le résultat de l'expression suivante en utilisant les opérateurs de pré-incrémentation et de post-incrémentation :**
   ```java
   int a = 5, b = 6;
   int resultat = ++a * b--; // a devient 6, resultat = 6 * 6 = 36, puis b devient 5
   System.out.println("a : " + a + ", b : " + b + ", resultat : " + resultat);
   ```

6. **Évaluer l'expression suivante et afficher la valeur finale des variables :**
   ```java
   int p = 8, q = 4;
   p = p / 2 * (q + 3) - p++; // p = 8 / 2 * (4 + 3) - 8 = 4 * 7 - 8 = 28 - 8 = 20, puis p devient 9
   System.out.println("p : " + p + ", q : " + q);
   ```
