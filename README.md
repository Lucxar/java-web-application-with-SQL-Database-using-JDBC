# Java Web Application with SQL Database using JDBC

This project is a Java web application that is set up with a SQL database using JDBC.

## Project Structure

The project structure is as follows:

- `.gradle/` - Gradle configuration files
- `.idea/` - IntelliJ IDEA configuration files
- `src/main/java/com/example/demo/` - Java source files
  - `controller/` - Contains the controller classes
    - `src/main/java/com/example/demo/controller/Controller.java` - Main controller class
    - `ErrorControllerAdvice.java` - Error handling class
  - `model/` - Contains the model classes and data access objects (DAOs)
    - `src/main/java/com/example/demo/model/FilmDao.java` - Data access object for films
    - `FilmDTO.java` - Data transfer object for films
    - `KinosaalDTO.java` - Data transfer object for kinosaal
    - `KundeDao.java` - Data access object for customers
    - `KundeDTO.java` - Data transfer object for customers
    - `src/main/java/com/example/demo/model/MitarbeiterDao.java` - Data access object for employees
    - `MitarbeiterDTO.java` - Data transfer object for employees
    - `Role.java` - Role enumeration
    - `SimpleRole.java` - Simple role class
    - `SimpleUser.java` - Simple user class
    - `src/main/java/com/example/demo/model/TicketDao.java` - Data access object for tickets
    - `TicketDTO.java` - Data transfer object for tickets
    - `User.java` - User class
    - `UserRepository.java` - User repository interface
    - `src/main/java/com/example/demo/model/VorstellungDao.java` - Data access object for Vorstellungen
    - `VorstellungDTO.java` - Data transfer object for Vorstellungen
  - `persistence/` - Contains the persistence classes
    - `PostgresqlUserRepository.java` - PostgreSQL user repository implementation
  - `security/` - Contains the security configuration classes
    - `CurrentUser.java` - Current user annotation
    - `CustomUserDetailsService.java` - Custom user details service
    - `SecurityConfig.java` - Security configuration
    - `UserToUserDetailsAdapter.java` - User to user details adapter
  - `src/main/java/com/example/demo/DemoApplication.java` - Main application class
- `src/main/resources/` - Resource files
  - `application.properties` - Application properties file
  - `data/` - Contains SQL scripts for database initialization
    - `data.sql` - Data initialization script
    - `schema.sql` - Database schema script
  - `templates/` - Contains HTML templates
    - `addFilm.html` - Template for adding a film
    - `addVorstellung.html` - Template for adding a Vorstellung
    - `changePassword.html` - Template for changing password
    - `demo.html` - Demo template
    - `film.html` - Template for displaying films
    - `index.html` - Index template
    - `registrierung.html` - Template for registration
    - `registrierungGast.html` - Template for guest registration
    - `registrierungMitarbeiter.html` - Template for employee registration
    - `ticket.html` - Template for displaying tickets
    - `vorstellung.html` - Template for displaying Vorstellungen
- `build.gradle` - Gradle build file
- `compose.yaml` - Docker Compose file
- `gradle/` - Gradle wrapper files
- `gradlew` - Gradle wrapper script (Unix)
- `gradlew.bat` - Gradle wrapper script (Windows)
- `settings.gradle` - Gradle settings file

## How to Run

1. Ensure you have Java and Gradle installed on your system.
2. Clone the repository.
3. Navigate to the project directory.
4. Run the following command to build the project:
   ```
   ./gradlew build
   ```
5. Run the following command to start the application:
   ```
   ./gradlew bootRun
   ```
6. The application will be accessible at `http://localhost:8080`.

## Database Configuration

The application uses a PostgreSQL database. The database configuration can be found in the `src/main/resources/application.properties` file. Update the following properties with your database credentials:

```
spring.datasource.url=jdbc:postgresql://localhost:5432/kinodb
spring.datasource.username=postgres
spring.datasource.password=1234
```

## License

This project is licensed under the MIT License.
