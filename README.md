** Task Management System**

** Features**

** Secure User Authentication:** JWT-based authentication ensures user privacy and data security.
** Task Management:**
Create tasks with clear titles, descriptions, and priority levels.
Edit existing tasks to keep them up-to-date.
Delete tasks you've completed.
** Powerful Search & Filtering:**
Find specific tasks using title or keyword search.
Filter tasks by priority, status, or due date for better organization.
** User Profile Management:** Keep your profile information current.
** Technologies Used**

Frontend

⚛️ Next.js: A React-based framework for efficient frontend rendering.
** Tailwind CSS:** Provides rapid styling and responsive design.
** React Hooks:** Manages state using useState and side effects with useEffect for smooth UI interactions.
** Axios:** Handles HTTP requests to the backend API.
Backend

️ Express.js: A Node.js framework for robust backend routing and API development.
** TypeScript:** Enhances code quality and maintainability with strict typing.
** Prisma ORM:** Simplifies MongoDB database interactions.
️ JWT: JSON Web Tokens provide secure authentication and authorization.
Database

️ MongoDB: A NoSQL database for flexible storage of user data and tasks.
⚙️ Installation

Prerequisites:

Node.js (v14 or later)
MongoDB
npm (Node Package Manager)
Steps:

Clone the repository:

Bash
git clone https://github.com/your-repo/task-management-system.git
cd task-management-system
Use code with caution.

Install dependencies:

Bash
npm install
Use code with caution.

Set up environment variables:

Create a .env file in the root directory and add:

PORT=8000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
Start the development server:

Bash
npm run dev
Use code with caution.

Access the application:

Open http://localhost:3000 in your browser.

** API Documentation**

Authentication

POST /auth/register: Register a new user with name, email, and password.
POST /auth/login: Login using email and password to receive a JWT token.
Tasks

GET /tasks: Retrieve all tasks for the authenticated user.
POST /task/create: Create a new task with title, description, and priority.
PATCH /task/:id: Update an existing task by its ID.
DELETE /task/:id: Delete a task by its ID.
Profile

GET /profile: Get the authenticated user's profile information.
PATCH /profile: Update the user's profile details.
️ System Design

Architecture

Frontend: Built with Next.js and utilizes Axios for HTTP requests.
Backend: Express.js (TypeScript) handles authentication and task management through REST APIs.
Database: MongoDB with Prisma ORM as the data layer.
Database Schema

User Collection

JSON
{
  "_id": "ObjectId",
  "name": "string",
  "email": "string",
  "password": "string (hashed)",
  "createdAt": "Date",
  "updatedAt": "Date"
}
Use code with caution.

Task Collection

JSON
{
  "_id": "ObjectId",
  "title": "string",
  "description": "string",
  "priority": "string (low | medium | high)",
  "completed": "boolean",
  "userId": "ObjectId (ref: User)",
  "createdAt": "Date",
  "updatedAt": "Date"
}
Use code with caution.

** Testing**

Manual Testing: Validated API endpoints using Postman.
Frontend Testing: Verified task creation, editing, and deletion using browser UI testing.
** Challenges Faced**

JWT Implementation: Managing token expiry and user session control effectively.
Efficient MongoDB Queries: Optimized task filtering and sorting for improved performance.
Prisma ORM Integration: Ensured smooth schema management and efficient handling of complex queries.
** Future Enhancements**
