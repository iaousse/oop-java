# Chapitre 1 : Initiation à la Programmation Orientée Objet avec Java

## Objectifs du Chapitre
À la fin de ce chapitre, vous serez capable de :
- Comprendre les principes de base de la Programmation Orientée Objet (POO).
- Connaître l'historique et l'évolution de Java.
- Expliquer le processus de compilation et d'exécution du code Java.
- Comprendre le rôle de la Machine Virtuelle Java (JVM) et du Garbage Collector.
- Maîtriser les éléments syntaxiques de base de Java.

---

## I. Historique de Java

### 1.1 Les Origines
- **1991** : Développement initié par James Gosling chez Sun Microsystems (acquis par Oracle en 2010).
- **Objectif initial** : Créer un langage pour les appareils électroniques grand public (*projet "Green"*).
- **Nom original** : *Oak* (changé en *Java* pour des raisons légales).
- **1995** : Lancement officiel de Java 1.0 avec le slogan *"Write Once, Run Anywhere"* (WORA).

### 1.2 Évolution Clé
- **Java 1.0 (1996)** : Première version publique avec les bases de la POO.
- **Java 2 (1998)** : Introduction de J2SE, J2EE, et J2ME.
- **Java 5 (2004)** : Fonctionnalités majeures : génériques, annotations, énumérations.
- **Java 8 (2014)** : Lambda expressions, API Stream, Optional.
- **Java 11 (2018)** : Version LTS (Long-Term Support), modularisation (JPMS).
- **Java 17 (2021)** : Nouveautés comme les *sealed classes* et améliorations du GC.

### 1.3 Pourquoi Java est-il Indépendant de la Plateforme ?
- **Bytecode Java** : Code intermédiaire compilé (`.class`) exécuté par la JVM.
- **JVM** : Adaptée à chaque OS, permettant l'exécution du même bytecode partout.

---

## II. Fonctionnement de Java : Compilation, JVM et Garbage Collection

### 2.1 Processus de Compilation
```java
// Fichier : HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}