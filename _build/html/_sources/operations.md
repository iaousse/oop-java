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

**Exemple 15 : Expression complexe avec `&&` et `||`**
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

