# **Full-Stack Kanban Task Management Application**

## **Project Summary**

The **Kanban Task Management Web App** is a modern task management platform that enables individuals and teams to organize, manage, and track tasks efficiently.

The application provides:

- Workflow visualization

- Task tracking

- Team collaboration

- Secure access control

Learners will build the backend using:

- Node.js

- Express.js

- MongoDB or PostgreSQL

The backend will be connected to an existing frontend Kanban application previously developed in earlier frontend modules.

The goal is to demonstrate full-stack development skills through:

- API development

- Authentication

- Database persistence

- Frontend-backend integration

# **Learning Objectives**

By completing this project, learners should be able to:

- Design RESTful APIs using Node.js and Express.

- Model relational or document-based database schemas.

- Implement authentication and authorization using JWT and bcrypt.

- Perform CRUD operations for persistent data.

- Integrate backend APIs into a frontend application.

- Manage frontend state using backend responses.

- Deploy a complete full-stack application.

## **Core Features**

## **1. User Authentication ****&**** Authorization**

Implement secure authentication features including:

- User registration

- User login

- JWT authentication

- Password hashing with bcrypt

### **Role-Based Access Control (RBAC)**

Support multiple user roles such as:

| **Role** | **Permissions** |
| --- | --- |
| Admin | Full access |
| Editor | Can modify boards/tasks |
| Viewer | Read-only access |

### **Optional Feature**

- Password reset functionality

## **2. Persistent Kanban Board Management**

Implement full CRUD functionality for:

### **Boards**

| **Operation** | **Description** |
| --- | --- |
| Create | Create new boards |
| Read | Retrieve boards |
| Update | Rename/edit boards |
| Delete | Remove boards |

### **Columns**

Support:

- Add columns

- Rename columns

- Reorder columns

- Delete columns

### **Tasks ****&**** Subtasks**

Support:

- Create tasks

- Edit tasks

- Delete tasks

- Mark tasks complete

- Manage subtasks

All data must persist in the database.

## **3. Persistent Drag-and-Drop Functionality**

Implement backend logic for:

- Updating task positions

- Moving tasks between columns

- Saving reordered task positions

### **Requirements**

When a task is dragged:

- Update the task’s column reference

- Update task order within the column

- Persist changes in the database

## **4. User ****&**** Team Collaboration**

Implement collaborative board functionality.

### **Features**

- Board ownership

- Invite collaborators

- Shared board access

### **Access Levels**

| **Access Level** | **Permissions** |
| --- | --- |
| Viewer | View content only |
| Editor | Modify content |
| Owner | Full board management |

### **Rules**

- Only owners and editors can modify content.

- Viewers cannot edit tasks or boards.

## **5. Advanced Task Features**

Implement additional task management capabilities.

### **Task Assignment**

- Assign tasks to board collaborators.

### **Due Dates**

- Add due dates to tasks.

### **Optional Features**

- Activity tracking:

- Example:"Task moved to Done by User X"
 

- Persist user theme preferences:

- Light mode

- Dark mode

# **Technical Requirements**

| **Category** | **Requirements** |
| --- | --- |
| Backend Framework | Node.js + Express |
| Database | MongoDB (Mongoose) or PostgreSQL (Prisma/Sequelize) |
| Authentication | JWT + bcrypt |
| API Design | RESTful endpoints |
| Validation | Joi, Zod, or similar |
| Error Handling | Proper HTTP codes and messages |
| Testing | Jest or Supertest |
| Deployment | Live backend deployment |

# **Suggested Database Models**

## **User Model**

{
  name,
  email,
  password,
  role,
  themePreference
}
 

## **Board Model**

{
  title,
  owner,
  collaborators,
  columns
}
 

## **Column Model**

{
  title,
  boardId,
  position
}
 

## **Task Model**

{
  title,
  description,
  status,
  assignedTo,
  dueDate,
  subtasks,
  position,
  columnId
}
 

# **Suggested API Endpoints**

# **Authentication Routes**

| **Method** | **Endpoint** | **Description** |
| --- | --- | --- |
| POST | /auth/register | Register user |
| POST | /auth/login | Login user |

# **Board Routes**

| **Method** | **Endpoint** | **Description** |
| --- | --- | --- |
| GET | /boards | Get all boards |
| POST | /boards | Create board |
| GET | /boards/:id | Get single board |
| PUT | /boards/:id | Update board |
| DELETE | /boards/:id | Delete board |

# **Column Routes**

| **Method** | **Endpoint** | **Description** |
| --- | --- | --- |
| POST | /boards/:id/columns | Add column |
| PUT | /columns/:id | Update column |
| DELETE | /columns/:id | Delete column |

# **Task Routes**

| **Method** | **Endpoint** | **Description** |
| --- | --- | --- |
| POST | /tasks | Create task |
| GET | /tasks/:id | Get task |
| PUT | /tasks/:id | Update task |
| DELETE | /tasks/:id | Delete task |

# **Drag-and-Drop Update Route**

| **Method** | **Endpoint** | **Description** |
| --- | --- | --- |
| PATCH | /tasks/:id/move | Update task position |

# **Validation Requirements**

Validate:

- Required fields

- Email format

- Password length

- Role values

- Task status values

Use:

- Joi

- Zod

- express-validator

# **Error Handling**

Use:

- Proper HTTP status codes

- Structured JSON responses

## **Example Success Response**

{
  "status": "success",
  "data": {}
}
 

## **Example Error Response**

{
  "status": "error",
  "message": "Unauthorized access"
}
 

# **Testing Requirements**

Use:

- Jest

- Supertest

Test:

- Authentication routes

- CRUD operations

- Protected routes

- Validation errors

# **Deployment Requirements**

Deploy:

- Backend API

- Frontend application

Suggested platforms:

- Render

- Railway

- Vercel

# **Deliverables**

# **1. Backend Repository**

Must include:

- Controllers

- Routes

- Models

- Middleware

- Configuration

# **2. Database Setup**

Include seed/sample data for:

- Users

- Boards

- Tasks

# **3. Connected Frontend**

The frontend should:

- Fetch live backend data

- Persist updates

- Support drag-and-drop updates

# **4. Documentation**

Include:

- API documentation

- Setup instructions

- README.md

Optional:

- Swagger

- Postman collection

# **5. Deployment Links**

Provide:

- Frontend URL

- Backend API URL

# **Suggested Project Structure**

project-root/
│
├── client/                 # Frontend application
│
├── server/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── services/
│   │   ├── utils/
│   │   └── app.js
│   │
│   ├── tests/
│   ├── .env
│   ├── package.json
│   └── server.js
│
├── README.md
└── postman/
 

# **Evaluation Criteria**

| **Criteria** | **Description** | **Weight** |
| --- | --- | --- |
| API Design & Structure | RESTful architecture and modular code | 20% |
| Database Modeling & Persistence | Logical schema design and persistence | 20% |
| Authentication & Authorization | JWT, RBAC, password hashing | 20% |
| Functionality & Feature Completion | CRUD features and collaboration tools | 15% |
| Frontend Integration | Frontend successfully connected to APIs | 10% |
| Code Quality & Documentation | Readable code and setup documentation | 10% |
| Bonus Features | Real-time updates, notifications, activity logs | 5% |

# **Bonus / Stretch Features**

If completed early, try implementing:

- Real-time updates with Socket.IO

- Notifications

- Activity logs

- File attachments

- Comments on tasks

- Theme persistence

- Offline support
