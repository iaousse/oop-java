# Programmation Orientée Objet (POO) en Java : Concepts et Pratiques

La Programmation Orientée Objet (POO) en Java est une méthode de développement qui structure le code autour d'objets et de leurs interactions. Ce modèle repose sur des notions essentielles comme les **classes**, les **objets**, les **méthodes** et les **attributs**. La POO est largement utilisée pour structurer et réutiliser du code dans des applications complexes et modulaires, favorisant la maintenabilité et l'extensibilité des projets.

```{admonition} Définition : Objets et Classes
- **Objet** : Un objet est une instance d'une classe, représentant une entité concrète ou abstraite. Il possède des caractéristiques (attributs) et des comportements (méthodes).
- **Classe** : Une classe est un modèle ou un plan de conception qui définit les attributs et les méthodes que ses objets auront.
```

## Concepts Fondamentaux de la POO

La POO repose sur quatre principes : l'**encapsulation**, l'**héritage**, le **polymorphisme**, et l'**abstraction**. Ces principes sont fondamentaux pour structurer les systèmes de manière modulaire et garantir une organisation claire et flexible du code.

---

### Encapsulation

L'encapsulation consiste à regrouper les données (attributs) et les fonctions (méthodes) qui manipulent ces données dans une même entité (la classe). Elle permet également de restreindre l'accès direct aux données, ce qui favorise la sécurité en protégeant les attributs des modifications extérieures non contrôlées.

```{admonition} Définition : Encapsulation
L'encapsulation consiste à rendre les attributs d'un objet privés (`private`) et à autoriser leur manipulation uniquement via des méthodes spécifiques, généralement des **getters** (méthodes de lecture) et des **setters** (méthodes de modification). Cela permet de contrôler les accès et de garantir une manipulation sécurisée.
```

```{admonition} Exemple d’Encapsulation
Considérons une classe **CompteBancaire** avec un attribut `solde` encapsulé. Plutôt que d'accéder directement à `solde`, l’utilisateur doit utiliser les méthodes `getSolde()` pour consulter le solde et `deposer()` ou `retirer()` pour le modifier. Cela garantit que le solde ne peut pas être modifié de manière inappropriée.
```

```java
public class CompteBancaire {
    private double solde;

    // Getter pour lire le solde
    public double getSolde() {
        return solde;
    }

    // Méthode pour déposer de l'argent
    public void deposer(double montant) {
        if (montant > 0) {
            solde += montant;
        }
    }

    // Méthode pour retirer de l'argent
    public void retirer(double montant) {
        if (montant > 0 && montant <= solde) {
            solde -= montant;
        }
    }
}
```

```{admonition} Exemple d’Encapsulation
Considérons une classe **Etudiant** qui encapsule des attributs privés `nom` et `age`. Ces attributs ne sont accessibles que par des méthodes publiques appelées getters et setters. Cela garantit un contrôle sur l'accès et la modification des données, notamment en validant que l'âge est positif avant de l'attribuer.
```

```java
public class Etudiant {
    private String nom;
    private int age;
    
    // Getters
    public String getNom() {
        return nom;
    }
    
    public int getAge() {
        return age;
    }
    
    // Setters
    public void setNom(String nom) {
        this.nom = nom;
    }
    
    public void setAge(int age) {
        if (age > 0) {
            this.age = age;
        }
    }
}
```

```{admonition} Remarque
L'encapsulation améliore la sécurité et la robustesse d'une application en empêchant les modifications directes des attributs. Les méthodes contrôlent comment ces attributs sont manipulés, ce qui limite les erreurs potentielles.
```

---

### Héritage

L'héritage est un mécanisme permettant de créer une nouvelle classe (appelée classe dérivée ou enfant) à partir d'une classe existante (classe parente). La classe dérivée hérite des attributs et des méthodes de la classe parente, mais peut également définir des caractéristiques supplémentaires ou spécifiques.

```{admonition} Définition : Héritage
L'héritage est un moyen de réutiliser le code en permettant à une classe d'hériter des attributs et des méthodes d'une autre classe. Ce mécanisme favorise la hiérarchisation et l'organisation logique du code.
```

```{admonition} Exemple d’Héritage
Imaginons une classe **Animal** avec des attributs `nom` et `age`. En créant une classe **Chien** qui hérite de **Animal**, la classe **Chien** obtient automatiquement les attributs et méthodes de **Animal** et peut ajouter des fonctionnalités spécifiques, telles que `aboyer()`.
```

```java
public class Animal {
    protected String nom;
    protected int age;

    public void manger() {
        System.out.println(nom + " est en train de manger.");
    }
}

public class Chien extends Animal {
    public void aboyer() {
        System.out.println(nom + " aboie.");
    }
}
```

```{admonition} Exemple d’Héritage
Prenons l'exemple d'une classe **Animal** qui possède une méthode `manger()`. Une classe **Chat** hérite d'**Animal** et utilise cette méthode, tout en ajoutant une méthode `miauler()` spécifique aux chats. Grâce à l'héritage, **Chat** peut réutiliser la fonctionnalité `manger()` sans la redéfinir.
```

```java
public class Animal {
    protected String nom;
    
    public void manger() {
        System.out.println(nom + " mange.");
    }
}

public class Chat extends Animal {
    public Chat(String nom) {
        this.nom = nom;
    }
    
    public void miauler() {
        System.out.println(nom + " miaule!");
    }
}

// Utilisation
Chat monChat = new Chat("Felix");
monChat.manger();    // Méthode héritée
monChat.miauler();   // Méthode spécifique
```



```{admonition} Remarque
L’héritage permet de structurer le code en définissant des hiérarchies de classes. Toutefois, une hiérarchie trop complexe peut devenir difficile à maintenir, donc l’héritage doit être utilisé judicieusement.
```

---

### Polymorphisme

Le polymorphisme permet de manipuler des objets de différentes classes de manière interchangeable grâce à une relation d'héritage. Ce concept permet de redéfinir des méthodes dans les classes dérivées, en adaptant le comportement aux besoins spécifiques de chaque classe.

```{admonition} Définition : Polymorphisme
Le polymorphisme signifie "plusieurs formes". Il permet de traiter différents types d'objets de manière uniforme tout en permettant à chaque objet de définir son propre comportement.
```

```{admonition} Exemple de Polymorphisme
Dans une hiérarchie de classes avec une classe parente **Animal** et des classes enfants **Chien** et **Chat**, une méthode commune `faireDuBruit()` peut être redéfinie dans chaque classe pour produire le son approprié.
```

```java
public class Animal {
    public void faireDuBruit() {
        System.out.println("L'animal fait un bruit.");
    }
}

public class Chien extends Animal {
    @Override
    public void faireDuBruit() {
        System.out.println("Le chien aboie.");
    }
}

public class Chat extends Animal {
    @Override
    public void faireDuBruit() {
        System.out.println("Le chat miaule.");
    }
}
```

```{admonition} Exemple de Polymorphisme
Imaginons une classe **Animal** avec une méthode `faireBruit()`. Les classes dérivées **Chat** et **Chien** redéfinissent cette méthode pour produire des bruits différents. En utilisant le polymorphisme, on peut traiter les deux objets (chat et chien) comme des animaux, mais obtenir des résultats spécifiques selon le type de l'animal.
```

```java
public class Animal {
    public void faireBruit() {
        System.out.println("L'animal fait un bruit");
    }
}

public class Chat extends Animal {
    @Override
    public void faireBruit() {
        System.out.println("Miaou!");
    }
}

public class Chien extends Animal {
    @Override
    public void faireBruit() {
        System.out.println("Wouf!");
    }
}

// Utilisation
Animal animal1 = new Chat();
Animal animal2 = new Chien();
animal1.faireBruit();  // Affiche "Miaou!"
animal2.faireBruit();  // Affiche "Wouf!"
```



```{admonition} Remarque
Le polymorphisme simplifie le code en permettant d'écrire des méthodes génériques qui s'adaptent automatiquement au type spécifique de l'objet manipulé. C'est un concept clé pour l'extensibilité.
```

---

### Abstraction

L'abstraction consiste à ne montrer que les aspects essentiels d'une entité tout en masquant les détails d'implémentation. Cela permet de concevoir des classes abstraites ou des interfaces pour définir les caractéristiques communes d'un ensemble d'objets sans imposer une implémentation spécifique.

```{admonition} Définition : Abstraction
L'abstraction est le processus de simplification en se concentrant sur les caractéristiques essentielles d'un objet, en ignorant les détails secondaires. En POO, elle se réalise souvent avec des interfaces ou des classes abstraites.
```

```{admonition} Exemple d’Abstraction
Une interface **Forme** avec une méthode `calculerSurface()` peut être implémentée par des classes **Cercle** et **Rectangle**, chacune fournissant une implémentation spécifique de `calculerSurface()`.
```

```java
public interface Forme {
    double calculerSurface();
}

public class Cercle implements Forme {
    private double rayon;

    public Cercle(double rayon) {
        this.rayon = rayon;
    }

    @Override
    public double calculerSurface() {
        return Math.PI * rayon * rayon;
    }
}

public class Rectangle implements Forme {
    private double longueur, largeur;

    public Rectangle(double longueur, double largeur) {
        this.longueur = longueur;
        this.largeur = largeur;
    }

    @Override
    public double calculerSurface() {
        return longueur * largeur;
    }
}
```

```{admonition} Exemple d’Abstraction
Dans cet exemple, **Forme** est une classe abstraite avec une méthode `calculerAire()`. La classe concrète **Carre** étend **Forme** et fournit sa propre implémentation de `calculerAire()`. Cette approche permet d'exiger la présence de cette méthode dans toutes les formes sans spécifier son fonctionnement exact dans la classe mère.
```

```java
public abstract class Forme {
    public abstract double calculerAire();
}

public class Carre extends Forme {
    private double cote;
    
    public Carre(double cote) {
        this.cote = cote;
    }
    
    @Override
    public double calculerAire() {
        return cote * cote;
    }
}

// Utilisation
Carre monCarre = new Carre(5);
System.out.println("Aire: " + monCarre.calculerAire());
```



```{admonition} Remarque
L'abstraction permet de définir des comportements attendus sans imposer de détails d'implémentation, rendant le code plus flexible et adaptable.
```

---

## Concepts Avancés : Classes et Objets

### Constructeurs

Les constructeurs sont des méthodes spéciales permettant d'initialiser les objets lors de leur création. Ils portent le même nom que la classe et n'ont pas de type de retour.

```{admonition} Types de Constructeurs
- **Constructeur par défaut** : Sans paramètres, initialise les attributs avec des valeurs par défaut.
- **Constructeur paramétré** : Avec paramètres, permet d'initialiser les attributs avec des valeurs spécifiques.
- **Constructeur surchargé** : Plusieurs versions du constructeur avec différents paramètres.
```

```{admonition} Exemple de Constructeurs
Considérons une classe **Personne** avec un constructeur par défaut, un constructeur paramétré, et un constructeur surchargé. Le constructeur surchargé utilise `this` pour appeler un autre constructeur.
```

```java
public class Personne {
    private String nom;
    private int age;

    // Constructeur par défaut
    public Personne() {
        this.nom = "Inconnu";
        this.age = 0;
    }

    // Constructeur paramétré
    public Personne(String nom, int age) {
        this.nom = nom;
        this.age = age;
    }

    // Constructeur surchargé avec un seul paramètre
    public Personne(String nom) {
        this(nom, 0); // Appel au constructeur paramétré
    }
}
```

```{admonition} Exemple de Constructeurs
La classe **Livre** présente trois types de constructeurs : un constructeur par défaut qui assigne des valeurs prédéfinies, un constructeur paramétré pour fournir des valeurs spécifiques et un constructeur surchargé pour gérer des cas intermédiaires, comme un livre sans auteur spécifié.
```

```java
public class Livre {
    private String titre;
    private String auteur;
    
    // Constructeur par défaut
    public Livre() {
        titre = "Sans titre";
        auteur = "Inconnu";
    }
    
    // Constructeur paramétré
    public Livre(String titre, String auteur) {
        this.titre = titre;
        this.auteur = auteur;
    }
    
    // Constructeur avec un seul paramètre
    public Livre(String titre) {
        this(titre, "Inconnu");  // Appel du constructeur paramétré
    }
}
```


---

### Utilisation du mot-clé `this`

Le mot-clé `this` fait référence à l'instance courante de la classe. Il permet de différencier les attributs des paramètres, d’appeler un autre constructeur, et de passer l'instance courante en paramètre.

```{admonition} Exemple avec `this`
Dans la méthode `setValeur`, `this` est utilisé pour distinguer l’attribut `valeur` du paramètre `valeur`.
```

```java
public class Exemple {
    private int valeur;

    public void setValeur(int valeur) {
        this.valeur = valeur; // 'this.valeur' fait référence à l'attribut
    }

    public Exemple getThis() {
        return this; // Retourne l'instance courante
    }
}
```

---

## Relations entre Classes

### Association

L'association est une relation simple entre deux classes, où une classe utilise une autre.

```{admonition} Exemple d'Association
Dans une relation entre une classe **Voiture** et une classe **Conducteur**, chaque **Voiture** possède un **Conducteur**.
```

```java
public class Voiture {
    private Conducteur conducteur;

    public void setConducteur(Conducteur conducteur) {
        this.conducteur = conducteur;
    }
}

public class Conducteur {
    private String nom;
}
```


```{admonition} Exemple d’Association entre Classes
La relation d'association est illustrée ici avec une classe **Voiture** qui peut avoir un **Conducteur**. Dans cet exemple, **Voiture** ne peut pas fonctionner sans conducteur assigné, mais **Conducteur** existe indépendamment.
```

```java
public class Voiture {
    private Conducteur conducteur;
    
    public void assignerConducteur(Conducteur conducteur) {
        this.conducteur = conducteur;
    }
}

public class Conducteur {
    private String nom;
    
    public Conducteur(String nom) {
        this.nom = nom;
    }
}

// Utilisation
Conducteur paul = new Conducteur("Paul");
Voiture maVoiture = new Voiture();
maVoiture.assignerConducteur(paul);
```
---

### Composition

La composition est une relation forte où une classe est une partie intégrante d’une autre classe. La classe contenant ne peut exister sans ses composants.

```{admonition} Exemple de Composition
Une classe **Maison** composée de **Piece**. Les pièces ne peuvent pas exister sans la maison.
```

```java
public class Maison {
    private final Piece[] pieces;

    public Maison() {
        pieces = new Piece[4];
        pieces[0] = new Piece("Salon");
        pieces[1] = new Piece("Cuisine");
    }
}

public class Piece {
    private String nom;

    public Piece(String nom) {
        this.nom = nom;
    }
}
```

---

### Agrégation

L'agrégation est une relation où une classe contient une autre, mais les deux peuvent exister indépendamment.

```{admonition} Exemple d'Agrégation
Dans une relation entre une **Université** et des **Etudiants**, les étudiants peuvent exister en dehors de l'université.
```

```java
public class Universite {
    private List<Etudiant> etudiants = new ArrayList<>();

    public void ajouterEtudiant(Etudiant etudiant) {
        etudiants.add(etudiant);
    }
}
```

---

## Classes Abstraites et Interfaces

### Classes Abstraites

Une classe abstraite ne peut pas être instanciée et peut contenir des méthodes abstraites, qui sont des méthodes sans corps que les classes dérivées doivent implémenter.

```{admonition} Exemple de Classe Abstraite
Une classe **Forme** abstraite avec une méthode abstraite `calculerSurface()` implémentée différemment dans les classes dérivées.
```

```java
public abstract class Forme {
    protected String couleur;

    public abstract double calculerSurface();

    public void setCouleur(String couleur) {
        this.couleur = couleur;
    }
}

public class Cercle extends Forme {
    private double rayon;

    @Override
    public double calculerSurface() {
        return Math.PI * rayon * rayon;
    }
}
```

### Interfaces

Les interfaces définissent des comportements sous forme de méthodes que les classes implémentant ces interfaces doivent respecter.

```{admonition} Exemple d'Interface
Une interface **Dessinable** avec une méthode `dessiner()` que les classes implémentent.
```

```java
public interface Dessinable {
    void dessiner();

    default void preparation() {
        System.out.println("Préparation du dessin");
    }
}

public class Rectangle implements Dessinable {
    @Override
    public void dessiner() {
        System.out.println("Dessin d'un rectangle");
    }
}
```

```{admonition} Exemple d’Interface
Dans cet exemple, **Jouable** est une interface qui définit les méthodes `jouer()` et `arreter()`. La classe **Musique** implémente cette interface et fournit une implémentation spécifique pour jouer et arrêter une chanson. Cela permet d’avoir un comportement standardisé pour tous les objets qui peuvent être "joués".
```

```java
public interface Jouable {
    void jouer();
    void arreter();
}

public class Musique implements Jouable {
    private String titre;
    
    public Musique(String titre) {
        this.titre = titre;
    }
    
    @Override
    public void jouer() {
        System.out.println("Joue " + titre);
    }
    
    @Override
    public void arreter() {
        System.out.println("Arrête " + titre);
    }
}

// Utilisation
Musique chanson = new Musique("Ma chanson");
chanson.jouer();
chanson.arreter();
```

---


