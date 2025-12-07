
# Structure du Projet
<img width="1428" height="517" alt="image" src="https://github.com/user-attachments/assets/e8a5f309-21c0-4f76-a088-745bc8d0e234" />
<img width="1414" height="784" alt="image" src="https://github.com/user-attachments/assets/3a0e48f8-2452-4d73-881f-337cc98a47e7" />
<img width="1414" height="604" alt="image" src="https://github.com/user-attachments/assets/4aca275c-213e-44bd-9657-8197035b719e" />
<img width="1420" height="522" alt="image" src="https://github.com/user-attachments/assets/7a69fbfd-bb62-4456-a4c4-fefcfa540f96" />


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
