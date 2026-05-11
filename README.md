# Système de Reconnaissance de Chiffres Manuscrits : MNIST 3 vs 5

![Java](https://img.shields.io/badge/Java-11%2B-orange)
![Maven](https://img.shields.io/badge/Maven-3.9.5-blue)
![Weka](https://img.shields.io/badge/ML-Weka-yellow)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

Instructeur : Mohamed Mahmoud Moussa
Institution : École Nationale des Sciences et Technologies Avancées de Borj-Cédria
Projet élaboré par : Bennani Firas ( 1TA3 ) 

Projet : Pipeline de Reconnaissance d'Images MNIST avec Java et Weka API
Mise en œuvre d'un classifieur intelligent capable de distinguer des chiffres manuscrits complexes. Le projet couvre l'intégralité du cycle de vie des données : du prétraitement des fichiers MNIST à la prédiction en temps réel via une interface graphique interactive. L'aspect technique repose sur l'implémentation de modèles de Machine Learning au sein d'un environnement Java, garantissant une exécution performante et une gestion rigoureuse des ressources système.

## 📌 Aperçu du Projet :

### Partie 1 : Architecture POO & Traitement de Fichiers
Traitement et conversion multi-format du dataset MNIST (IDX vers CSV, Excel, PNG, ARFF) via une architecture modulaire (`DataProcessor`, `MNISTProvider`, `ExcelExporter`)

### 🔹 Partie 2 : Gestion des Exceptions Personnalisées
Gestion d'erreurs robuste via 3 exceptions personnalisées (`InvalidDimensionsException`, `MNISTFileNotFoundException`, `DataFormatMismatchException`) pour la validation et l'intégrité des données MNIST.

### 🔹 Partie 3 : IA & Polymorphisme (Intégration Weka)
Classification via Naïve Bayes et Random Forest (ML qui utilisent Weka) utilisant un design polymorphe pour l'interchangeabilité et la comparaison de performance des modèles, en utilisant les classes `DigitClassifier`, `NaiveBayesClassifier`, `RandomForestClassifier`, `ModelComparator`

### 🔹 Partie 4 : Interface Graphique (Reconnaissance en Temps Réel)
Interface interactive `RecognitionGUI` avec canvas de dessin `DrawingCanvas`, incluant un prétraitement d'image (280x280 vers 28x28) et la prédiction en temps réel.

---

## 📁 Structure du Projet
TP JAVA PROJECT/
├── src/
│ ├── main/java/com/example/
│ │ ├── data/
│ │ ├── exceptions/
│ │ ├── ml/
│ │ ├── gui/
│ │ ├── Main.java
│ │ └── WekaExample.java
│ └── test/java/com/example/
├── data/mnist/
├── lib/weka-3-8-6/
├── tools/apache-maven-3.9.5/
├── pom.xml
└── README.md

---

## ⚙️ Prérequis

- Java 11+ (compatible Java 21)
- Maven 3.6+
- MNIST Dataset (téléchargement requis)

---

##  Démarrage Rapide

###  Build the project
```bash
./tools/apache-maven-3.9.5/bin/mvn clean compile
1. Download MNIST dataset and place in data/mnist/
 2. Run mvn clean compile to verify build
3. Run mvn test to test Part 1 functionality
 4. Run ModelComparator to compare classifier accuracy
5. Launch GUI with RecognitionGUI to test real-time recognition
1. Open this folder in VS Code
2. Edit files in src/main/java/ and src/test/java/
3. Use the tasks to build and run
 
