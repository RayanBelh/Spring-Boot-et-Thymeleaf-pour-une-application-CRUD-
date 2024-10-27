# Spring-Boot-et-Thymeleaf-pour-une-application-CRUD-

Ce projet est un exemple d'application web CRUD simple développée avec **Spring Boot** et **Thymeleaf**. Il utilise **Spring Data JPA** pour fournir les fonctionnalités CRUD de base pour une entité `User` stockée dans une base de données MySQL.

## Prérequis

- **Java 1.8**
- **MySQL** (Configurer les accès dans `application.properties`)
- **IDE** (IntelliJ IDEA, Eclipse, ou autre)

## Démarrage

### 1. Cloner le projet

Clonez ce dépôt dans votre environnement local :

```bash
git clone <URL_DU_DEPOT>
cd demothymeleaf
```
### 2. Ajouter les dépendances Maven
Ce projet utilise spring-boot-starter-parent comme parent Maven pour gérer les versions de dépendances :

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-thymeleaf</artifactId>
</dependency>
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <scope>runtime</scope>
</dependency>
```
### 3. Configuration MySQL
Dans le fichier application.properties, configurez la connexion à la base de données :

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/thymeleaf?useUnicode=true&useJDBCCompliantTimezoneShift=true&useLegacyDatetimeCode=false&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=
spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=update
```
### 4. Structure des packages

model : Contient la classe User avec des validations.
repository : Interface UserRepository étendant CrudRepository.
controller : Classe UserController gérant les endpoints pour les opérations CRUD.

### 5. Lancer l'application
Dans votre IDE, exécutez la classe DemothymeleafApplication. Une fois démarrée, l'application sera accessible à http://localhost:8080.

### 6. Points de terminaison

`Ajouter un utilisateur :` GET /signup

`Enregistrer un utilisateur :` POST /adduser

`Mettre à jour un utilisateur :` GET /edit/{id}

`Supprimer un utilisateur :` GET /delete/{id}

### 7. Interface utilisateur

Les vues Thymeleaf suivantes sont implémentées :

`add-user.html :` Formulaire d'ajout d'un nouvel utilisateur.

`update-user.html :` Formulaire de mise à jour d'un utilisateur existant.

`index.html :` Liste des utilisateurs.

### Dépendances et Plugins : 
Les plugins Maven pour la gestion et le démarrage de l'application Spring Boot :

```xml

<plugin>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-maven-plugin</artifactId>
</plugin>
```
## Auteurs et Licence
Ce projet est développé dans le cadre d'un TP de démonstration avec Spring Boot et Thymeleaf.

## Video demonstrative : 


https://github.com/user-attachments/assets/79170508-959f-436d-9a19-b01dc566b2c9



