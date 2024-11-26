### **Take-Home Assignment: Task Management API with JavaScript and SQL**

Build a **RESTful API** using **Node.js** and **SQL** to manage tasks. This assignment will assess your ability to integrate a relational database, write clean and maintainable JavaScript code, and document your solution.

---

### **Assignment Overview**
You are tasked with developing a **Task Management System API** that allows users to perform CRUD (Create, Read, Update, Delete) operations on tasks. Your implementation must use **Node.js** for the backend and **SQL** for the database.

---

### **Detailed Requirements**

#### **1. API Features**
1. **Add a Task**  
   Endpoint: `POST /tasks`  
   - Accepts the following fields in the request body:
     - `title` (string, required): The title of the task.
     - `description` (string, optional): A brief description of the task.
     - `due_date` (date, required): The due date for the task.
     - `status` (string, default: "Pending"): The status of the task.
   - Validates input (e.g., `title` and `due_date` must not be empty).

2. **Retrieve All Tasks**  
   Endpoint: `GET /tasks`  
   - Returns a list of all tasks from the database, sorted by `due_date` in ascending order.

3. **Update a Task**  
   Endpoint: `PUT /tasks/:id`  
   - Updates the task identified by `id`.
   - Accepts the following fields in the request body (all optional):
     - `title`
     - `description`
     - `due_date`
     - `status`
   - Validates that the `id` exists before updating.

4. **Delete a Task**  
   Endpoint: `DELETE /tasks/:id`  
   - Deletes the task identified by `id`.
   - Returns an appropriate response if the `id` does not exist.

---

#### **2. Technical Stack**
- **Backend Framework**: Node.js with **Express**.
- **Database**: Use **SQLite** or **PostgreSQL**.
- **Database Schema**:  
  Use the following schema for the `tasks` table:
  ```sql
  CREATE TABLE tasks (
      id SERIAL PRIMARY KEY,
      title VARCHAR(255) NOT NULL,
      description TEXT,
      due_date DATE NOT NULL,
      status VARCHAR(50) DEFAULT 'Pending'
  );
  ```

---

#### **3. Project Setup**
Your submission should include the following:
1. **Server Setup**:
   - A well-structured Node.js application with separate folders for routes, controllers, models, and database migrations.
   - Middleware for input validation and error handling.

2. **Database Integration**:
   - Include an SQL script or a migration file to set up the database schema.
   - Use a database library like **pg** for PostgreSQL or **better-sqlite3** for SQLite.

3. **Documentation**:
   - A `README.md` file with:
     - Instructions to set up and run the project locally.
     - Details about the API endpoints, including sample requests and responses.

---

#### **4. Expected Deliverables**
1. **Functional API**:
   - All endpoints working as specified.
2. **Code Quality**:
   - Clean, modular, and maintainable code.
   - Use of ES6+ features where appropriate.
3. **Database Setup**:
   - SQL script or migration file included in the repository.
4. **Error Handling**:
   - Graceful handling of invalid inputs and database errors.
5. **Documentation**:
   - Clear and detailed instructions for setting up and testing the API.

---

#### **5. Bonus Points**
1. Add pagination to the `GET /tasks` endpoint.  
2. Add basic authentication (e.g., an API key header) to secure endpoints.  
3. Use Docker to containerize the application and database.  
4. Include unit tests for the API endpoints using **Jest** or another testing framework.

---

#### **6. Submission Guidelines**
1. Submit your project via a **GitHub repository**.
2. Include a `README.md` file with:
   - Setup instructions (how to install dependencies, set up the database, and run the project).
   - API documentation with examples of requests and responses.
3. Deadline: [ within 3-5 days from assignment].

---

### **Evaluation Criteria**
1. **Functionality**: Does the API meet the specified requirements?  
2. **Code Quality**: Is the code clean, modular, and well-documented?  
3. **Database Integration**: Is the database properly set up and integrated?  
4. **Documentation**: Are the setup instructions and API details clear and complete?  
5. **Bonus Features**: Any additional enhancements beyond the core requirements.
