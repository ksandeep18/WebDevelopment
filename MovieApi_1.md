
# 📚 Full Stack Development with Java Spring Boot, React, and MongoDB

---

## Index

- JDK and IntelliJ IDEA Installation
- MongoDB Atlas Setup
- Project Initialization
- Project Structure
- Running the Project
- Writing the First Endpoint
- Database Configuration
- Installing Additional Dependencies
- Setting Up Environment Variables
- Movies and Reviews Endpoints
- Testing
- Backend Conclusion
- Frontend Introduction
- Creating the React Project
- Applying Bootstrap to the React App
- Implementing useState and useEffect Hooks
- Creating Home and Hero Components
- Styling the Carousel
- Creating Header Component (Navigation Bar)
- Creating Trailer Component using react-player
- Movie Reviews Functionality
- Adding and Getting Reviews with HTTP Requests
- Course Wrap-Up

---

## 1. Initial Setup (Backend Preparation)

### Tech Stack
- **Backend:** Java + Spring Boot
- **Frontend:** React.js
- **Database:** MongoDB Atlas (Cloud)

---

## 1.1 JDK Installation
- Download and install **JDK** (Java Development Kit).
- Verify installation using:
  ```bash
  javac --version

## 1. Initial Setup (Backend Preparation)

### Tech Stack:
- **Backend:** Java + Spring Boot
- **Frontend:** React.js
- **Database:** MongoDB Atlas (Cloud)

---

### 1.1 JDK Installation:
- Download and install **JDK** (Java Development Kit).
- Check installation with:
  ```bash
  javac --version
### 1.2 IntelliJ IDEA Installation:
- Install IntelliJ IDEA (recommended IDE for Java and Kotlin frameworks).

- Prefer Community Edition (free) unless you need advanced features.

1.3 MongoDB Atlas Setup:
Navigate to MongoDB Atlas website.

Create a new project called: movieApi.

Choose Shared Cluster (Free Tier).

Provider: AWS.

Fill necessary cluster details (cluster name, region, etc.).

Create Database User with username/password for accessing DB.

Database is ready for connection and can be used as the local DB for Spring Boot.

1.4 Importing Movie Data:
Clone/download the JSON file containing movies from the project’s GitHub repository.

Import JSON into the MongoDB Atlas cluster database.

2. Project Initialization (Spring Boot)
2.1 Spring Initializr Setup:
Go to start.spring.io.

Select the following:

Project: Maven

Language: Java

Spring Boot Version: Stable one (2.x/3.x)

Dependencies:

Spring Web

Spring Data MongoDB

Spring Boot DevTools

Generate and Download the Project.

2.2 Project Structure:
After unzipping and opening in IntelliJ:

Folder structure:

css
Copy code
src/
  main/
    java/
    resources/
  test/
pom.xml
Inside src/main, important folders:

db (contains imported movie data if needed)

java/ (backend code — controllers, services, models)

2.3 Running the Spring Boot Application:
Try running the application.

Initially, it fails to connect to MongoDB Atlas — that's expected.

Fix:

Go to pom.xml.

Comment out problematic dependency if any causing reload errors.

Reload Maven Project.

After fixing, run the app and open:

arduino
Copy code
http://localhost:8000
(Or the port specified.)

🛠 Commands / Actions Mentioned
Purpose	Command
Check JDK version	javac --version
Create MongoDB Atlas DB and import JSON	(done via UI)
Generate Spring Boot Project	start.spring.io
📝 Notes:
MongoDB Atlas needs IP Whitelisting (0.0.0.0/0 for public access).

IntelliJ automatically detects pom.xml and manages dependencies.

First error is normal because DB connection is not yet configured.

📌 What You Should Do After This:
Proceed to Writing First Endpoint part.

Configure the database connection properly after backend endpoints.

⭐ Current Status:
✔️ Environment setup complete
✔️ MongoDB ready
✔️ Spring Boot project initialized
✔️ Backend project structured

yaml
Copy code

---

✅ Now it's 100% **ready to copy-paste** into any `.md` file (like your GitHub repo, personal notes, etc.) without any changes.

---

Would you also like me to give you a **ready-made blank `.md` template** for your next video section (so you can just fill points)?  
It will save you even more time! 🚀  
Shall I prepare it?






