# Outil de Travail 

## Introduction à Jupyter Notebook

**Jupyter Notebook** est une application open-source qui permet de créer et partager des documents contenant du code, du texte, des visualisations, et bien plus encore. C’est un outil très populaire en science des données, en apprentissage automatique et pour l'enseignement, car il permet de combiner du code et de la documentation de manière interactive.

### Pourquoi Jupyter Notebook ?

- **Code Exécutable** : Permet d'exécuter du code dans de nombreux langages de programmation, dont Python, R, et Java.
- **Interface Interactive** : Facile à utiliser pour exécuter des fragments de code, tester des concepts, et obtenir des retours immédiats.
- **Visualisation des Données** : Intègre facilement des visualisations, ce qui le rend parfait pour l'analyse de données.
- **Documentation et Narration** : Avec le support du Markdown, il est possible d'écrire du texte, des formules mathématiques, et de créer des rapports lisibles et interactifs.

## Installation de Jupyter Notebook

### Prérequis

- **Python** : Jupyter Notebook est basé sur Python, donc Python doit être installé sur votre machine. Téléchargez la version la plus récente de Python sur [python.org](https://www.python.org/downloads/).

Pour vérifier si Python est installé, ouvrez le terminal (ou l’invite de commande) et tapez :
```bash
python --version
```
ou
```bash
python3 --version
```

### Étape 1 : Installation de Jupyter Notebook

La méthode recommandée pour installer Jupyter Notebook est d'utiliser `pip`, le gestionnaire de paquets Python.

1. Ouvrez le terminal (ou l’invite de commande).
2. Tapez la commande suivante pour installer Jupyter Notebook :
   ```bash
   pip install notebook
   ```

Cela va installer Jupyter Notebook ainsi que toutes les dépendances nécessaires.

### Étape 2 : Lancer Jupyter Notebook

Pour lancer Jupyter Notebook, utilisez la commande suivante dans le terminal :
```bash
jupyter notebook
```

Cela ouvrira Jupyter Notebook dans votre navigateur par défaut et affichera une page où vous pouvez créer et organiser des notebooks.

### Étape 3 : Créer un Nouveau Notebook

1. Dans Jupyter Notebook, cliquez sur **New** (Nouveau) en haut à droite.
2. Sélectionnez un noyau de programmation (par exemple, Python 3 pour exécuter du code Python).

Vous avez maintenant un notebook ouvert et prêt pour exécuter du code !


## Installation du noyau Java (IJava)

Pour exécuter du code Java dans Jupyter Notebook, nous devons installer le noyau **IJava**, qui permet de faire fonctionner Java dans Jupyter Notebook.

### Étape 1 : Prérequis pour IJava

#### 1. Installer Java (Java 11 ou version supérieure)

##### Windows

1. Allez sur [oracle.com/java](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Téléchargez l'installateur pour Windows.
3. Ouvrez l'installateur téléchargé et suivez les instructions pour installer Java.
4. Une fois l'installation terminée, ouvrez l'invite de commande et vérifiez l'installation de Java avec la commande :
   ```bash
   java -version
   ```
   Vous devriez voir la version de Java installée si tout est correct.

##### Linux

1. Ouvrez le terminal.
2. Mettez à jour le système et installez Java avec la commande suivante (pour Debian/Ubuntu) :
   ```bash
   sudo apt update
   sudo apt install openjdk-11-jdk
   ```
3. Vérifiez que Java est bien installé avec :
   ```bash
   java -version
   ```

##### macOS

1. Allez sur [oracle.com/java](https://www.oracle.com/java/technologies/javase-downloads.html).
2. Téléchargez le fichier `.dmg` pour macOS et ouvrez-le pour lancer l'installation.
3. Suivez les instructions de l’installateur pour installer Java.
4. Une fois installé, ouvrez le terminal et vérifiez l'installation en tapant :
   ```bash
   java -version
   ```

Si la version de Java s’affiche, l’installation a été réussie.

---

### Étape 2 : Télécharger et Installer IJava

Pour installer IJava, nous devons cloner le dépôt GitHub et utiliser `gradlew` pour installer le noyau.

#### Windows

1. Ouvrez l’invite de commande ou **PowerShell**.
2. **Cloner le dépôt IJava** :
   ```bash
   git clone https://github.com/SpencerPark/IJava.git
   ```
   Cette commande va télécharger IJava dans un dossier nommé `IJava`.
   
3. **Naviguer dans le dossier IJava** :
   ```bash
   cd IJava
   ```
4. **Construire et installer le noyau** :
   ```bash
   gradlew installKernel
   ```
   Une fois terminé, le noyau Java sera installé dans Jupyter.

#### Linux

1. Ouvrez le terminal.
2. **Cloner le dépôt IJava** :
   ```bash
   git clone https://github.com/SpencerPark/IJava.git
   ```
3. **Naviguer dans le dossier IJava** :
   ```bash
   cd IJava
   ```
4. **Construire et installer le noyau** :
   ```bash
   ./gradlew installKernel
   ```
   Cette commande va installer le noyau IJava dans Jupyter Notebook.

#### macOS

1. Ouvrez le terminal.
2. **Cloner le dépôt IJava** :
   ```bash
   git clone https://github.com/SpencerPark/IJava.git
   ```
3. **Naviguer dans le dossier IJava** :
   ```bash
   cd IJava
   ```
4. **Construire et installer le noyau** :
   ```bash
   ./gradlew installKernel
   ```
   Une fois terminé, vous verrez un message indiquant que l'installation est réussie.

---

### Étape 3 : Vérifier l'Installation de IJava

1. Lancez Jupyter Notebook en tapant la commande suivante dans le terminal (ou l'invite de commande sous Windows) :
   ```bash
   jupyter notebook
   ```
   
2. Dans Jupyter Notebook, créez un nouveau notebook et, dans la liste des noyaux, vous devriez maintenant voir **Java** en plus de Python.

3. Sélectionnez **Java** pour créer un notebook qui supporte le code Java.

---

### Étape 4 : Tester le noyau Java dans Jupyter Notebook

Dans votre nouveau notebook Java, vous pouvez maintenant exécuter des commandes Java. Par exemple, tapez le code suivant dans une cellule et exécutez-la :

```java
System.out.println("Hello, Jupyter and Java!");
```

Si tout est installé correctement, vous verrez le texte `Hello, Jupyter and Java!` s'afficher sous la cellule.



---









