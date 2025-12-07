# Structure du Projet

## Aperçu

Ce projet est une application Spring Boot qui expose un service web SOAP pour la gestion de comptes bancaires.

## Structure des Fichiers

```
.
├── .gitattributes
├── .gitignore
├── HELP.md
├── mvnw
├── mvnw.cmd
├── pom.xml
├── src
│   ├── main
│   │   ├── java
│   │   │   └── org
│   │   │       └── example
│   │   │           └── demo
│   │   │               └── config
│   │   │                   ├── ConfigApplication.java
│   │   │                   ├── entities
│   │   │                   │   ├── Compte.java
│   │   │                   │   ├── CompteRepository.java
│   │   │                   │   └── TypeCompte.java
│   │   │                   ├── Repositorie
│   │   │                   └── Service
│   │   │                       └── CompteSoapService.java
│   │   └── resources
│   │       ├── application.properties
│   │       ├── static
│   │       └── templates
│   └── test
│       └── java
│           └── org
│               └── example
│                   └── demo
│                       └── config
│                           └── ConfigApplicationTests.java
```

## Composants Clés

### `ConfigApplication.java`

Fichier principal de l'application Spring Boot.

### `entities`

Contient les entités JPA qui modélisent les objets du domaine.

*   `Compte.java`: Entité représentant un compte bancaire.
*   `TypeCompte.java`: Énumération pour les types de comptes (par exemple, COURANT, EPARGNE).
*   `CompteRepository.java`: Interface Spring Data JPA pour l'accès aux données des comptes.

### `Service`

Contient la logique métier de l'application.

*   `CompteSoapService.java`: Implémente le service web SOAP pour les opérations sur les comptes.

### `resources`

*   `application.properties`: Fichier de configuration de l'application (par exemple, configuration de la base de données).
*   `static`: Pour les fichiers statiques (CSS, JavaScript, images).
*   `templates`: Pour les modèles de vue (par exemple, Thymeleaf, FreeMarker).

## Comment Exécuter

1.  Assurez-vous d'avoir Java et Maven installés.
2.  Exécutez la commande `mvnw spring-boot:run` à la racine du projet.
3.  Le service web sera accessible à l'adresse `http://localhost:8080/BanqueWS?wsdl`.
