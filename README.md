# SenaSoft2024

Project Developed in Collaboration whit [Jhon esneider castañeda],GitHub = https://github.com/uranium092, [Development Time: 3 business Days]. 3rd in Free Development category, sponsored by IBM([SkillBuild] https://skillsbuild.org/).

**Technologies:**
	**Frontend:** React whit MUI(**UI Library**) and Leaflet(**Map Library**).
	**Backend:** Java, Spring Boot, Maven, Spring Data.
	**MotorSQL:** MongDB
 [Challenge Details:] https://drive.google.com/file/d/1Np9pFQLVkpLlPe45oRZe_9dg8_8N_Ase/view?usp=drive_link)

**Important Note:** 

To access administrative roles and functions (as requested by the sponsor), you must use the folliwing ID number at the administrative Login: `9999`.

## Necessary requirements###.
### Backend ###:
1.  **Java:** Download and install JDk version 17 or higher from [Oracle](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html).
2.  **MongoDB(2 options):**
    * Install MongoDB Community Edition version 5.0.26 or higher from [MongoDB](https://www.mongodb.com/try/download/community).
    * Alternatively, you can use the cloud service [MongoDB Atlas](https://www.mongodb.com/atlas/database).

### Frontend:
1.  **Node.js:** Download and install Node.js vesion 20.12.2 or higher from [NodeOrg](https://nodejs.org/en/download).


## Repository Structure:
The repository contains two projects: Backend and Frontend.
* `BackSenaSoft/`: Contains the source code written in Spring Boot.
* `frontSenaSoft/`: Contains the source code in React written using both `.jsx` and `.tsx`.😅

## Firts Stpes
1.  **Clone Repository:**

    ```bash
    git clone https://github.com/uranium092/SenaSoft2024
    ```



## Configuración

### Backend (BackSenaSoft)

1.  **Navegar al directorio del backend:**

    ```bash
    cd SenaSoft2024/BackSenaSoft
    ```

2.  **MongoDB:** Asegúrate de que MongoDB esté en ejecución.
3.  **Base de datos:** Crea una base de datos llamada `SenaSoft` en tu instancia de MongoDB (local o Atlas).
4.  **`application.properties`:** El archivo `application.properties` se encuentra en `src/main/resources/`. Por defecto, está configurado para conectar con MongoDB en localhost. Si estás utilizando MongoDB Atlas, debes modificar la cadena de conexión en este archivo.

    ```properties
    spring.application.name=BackSenaSoft
    spring.data.mongodb.uri=mongodb://localhost:27017/SenaSoft
    ```

    Si usas MongoDB Atlas, la cadena de conexión se verá similar a:

    ```properties
    spring.data.mongodb.uri=mongodb+srv://<usuario>:<contraseña>@<cluster>.mongodb.net/SenaSoft?retryWrites=true&w=majority
    ```

### Frontend (frontSenaSoft)

1.  **Navegar al directorio del frontend:**

    ```bash
    cd SenaSoft2024/frontSenaSoft
    ```

2.  **`.env`:** Crea un archivo `.env` en el directorio `frontSenaSoft/` con la siguiente información:

    ```properties
    VITE_SERVER_URL=http://localhost:8080
    ```

    * Este archivo guarda la URL del backend; si este no está en ejecución en el puerto `:8080`, ajusta la URL en el archivo `.env`.

## Ejecución

### Backend (BackSenaSoft)

1.  **Ejecutar la aplicación:**

    * **Usando el Wrapper de Maven (mvnw):**

        ```bash
        mvnw spring-boot:run
        ```

    * **Usando Maven instalado localmente:**

        ```bash
        mvn spring-boot:run
        ```

    * **Ejecutando el JAR compilado:**

        * Compilar el proyecto:

            ```bash
            mvn clean package
            ```

        * Ejecutar el JAR:

            ```bash
            java -jar target/app.jar
            ```
            * Reemplaza app.jar por el nombre del archivo .jar generado en `/target`

### Frontend (frontSenaSoft)

1.  **Instalar dependencias:**

    ```bash
    npm install
    ```

2.  **Ejecutar el frontend:**

    ```bash
    npm run dev
    ```

    * El frontend estará disponible en `http://localhost:5173`.

## Recomendaciones

* Asegúrate de que el backend se esté ejecutando en el puerto `:8080`, ya que el frontend está configurado para conectarse a esta URL por defecto.
* Si necesitas cambiar el puerto del backend, actualiza la variable `VITE_SERVER_URL` en el archivo `.env` del frontend.
