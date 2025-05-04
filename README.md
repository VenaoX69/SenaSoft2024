# SenaSoft2024

** Project Developed in Collaboration with [Jhon esneider castañeda]
** GitHub = https://github.com/uranium092
** Development Time: **3 business Days. 
** Result:** 3rd place in the Free Development category, sponsored by IBM([SkillBuild] https://skillsbuild.org/).

**Technologies:**
	**Frontend:** React with MUI(**UI Library**) and Leaflet(**Map Library**).
	**Backend:** Java, Spring Boot, Maven, Spring Data.
	**Database:** MongDB
 [Challenge Details:] https://drive.google.com/file/d/1Np9pFQLVkpLlPe45oRZe_9dg8_8N_Ase/view?usp=drive_link)

**Important Note:** 

To access administrative roles and functions (as requested by the sponsor), you must use the folliwing ID number at the administrative Login: `9999`.

## Prerequisites###.
### Backend ###:
1.  **Java:** JDk 17 or higher - download from [Oracle](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html).
2.  **MongoDB (2 options):**
    * Install MongoDB Community Edition version 5.0.26 or higher from [MongoDB](https://www.mongodb.com/try/download/community).
    * Alternatively, you can use the cloud service [MongoDB Atlas](https://www.mongodb.com/atlas/database).

### Frontend:
1.  **Node.js:** vesion 20.12.2 or higher - download from [NodeOrg](https://nodejs.org/en/download).


## Firts Steps
1.  **Clone the repository:**

    ```bash
    git clone https://github.com/VenaoX69/SenaSoft2024.git
    ```

	## Repository Structure:
		The repository contains two projects: Backend and Frontend.
			* `BackSenaSoft/`: Spring Boot backend.
			* `frontSenaSoft/`: React frontend(`.jsx` and `.tsx`😅).


## Configuration

### Backend
1.  **MongoDB:** Ensure your MongoDB instance is running(local ot Atlas).
		**DataBase:** Create a database named `SenaSoft`.

2.  **Backend Configuration:**

		Edit `BackSenaSoft/src/main/resources/application.properties`:
	   ```
		   properties
		   # Default: local MongoDB
		   spring.data.mongodb.uri=mongodb://localhost:27017/SenaSoft

		   # For Atlas, replace with:
		   spring.data.mongodb.uri=mongodb+srv://<user>:<password>@<cluster>.mongodb.net/SenaSoft?retryWrites=true&w=majority
	   ```
			
### Frontend:

1.  **Enviroment variables**	
		In 'frontSenaSoft/' create a file name `.env`:
				```properties
				VITE_SERVER_URL=http://localhost:8080
				```
			**If your backend runs on a different port, update VITE_SERVER_URL accordingly.**

## Execution

### Backend
1. **Run the application:**

   - **Using the Maven Wrapper**  
     - **Unix/macOS:**
       ```bash
       ./mvnw spring-boot:run
       ```
     - **Windows (PowerShell / CMD):**
       ```powershell
       mvnw.cmd spring-boot:run
       ```

    - **Run with a local Maven install:**

        ```bash
        mvn spring-boot:run
        ```

    - **Excecute the compiled JAR:**

        * Build the project:

            ```bash
            mvn clean package
            ```

        * Run the JAR:

            ```bash
            java -jar target/app.jar
            ```
            **Note:** Replace `app.jar` with the actual JAR filename generated in the `/target` directory.

### Frontend
1.  **Install dependencies:**

    ```bash
    npm install
    ```

2.  **Run Frontend:**

    ```bash
    npm run dev
    ```

    * Available at: `http://localhost:5173`.

## Recomendaciones

* The Frontend deafults to `http://localhost:8080`, If you change you backend port, update `VITE_SERVER_URL` in the `.env` file.
