# **Gig+ - Job Listing Platform**

**Gig+** is a web application designed to connect users to job opportunities in a sleek and intuitive interface. This project uses the MERN stack (MongoDB, Express, React, Node.js) and offers features like job listings, filtering, user authentication, and user profiles. The black and gold theme creates an elegant and professional look.

---

## **Table of Contents**
1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [Installation](#installation)
4. [Running the Application](#running-the-application)
5. [Project Structure](#project-structure)
6. [API Routes](#api-routes)
7. [Usage](#usage)
8. [Contributing](#contributing)
9. [License](#license)

---

## **Features**

- **Job Listings**: Users can browse available job opportunities.
- **Job Filtering**: Users can filter job listings by **location**, **pay rate**, and **title**.
- **User Authentication**: Signup and login functionality using JWT.
- **User Profiles**: Users can view and update their profile information, as well as manage jobs they have posted.
- **Responsive UI**: Optimized for both desktop and mobile experiences.
- **Backend API**: CRUD operations for job listings, user management, and authentication.

---

## **Tech Stack**

**Frontend**:
- React.js
- CSS (with custom black and gold theme)
  
**Backend**:
- Node.js
- Express.js
- MongoDB (via Mongoose)

**Authentication**:
- JWT (JSON Web Token) for secure user authentication

---

## **Installation**

1. **Clone the repository:**

```bash
git clone https://github.com/yourusername/gig-plus.git
cd gig-plus
```

2. **Install dependencies for both client and server:**

```bash
# Install backend dependencies
cd server
npm install

# Install frontend dependencies
cd ../client
npm install
```

---

## **Running the Application**

### **Backend (Server)**:
1. Create a `.env` file in the `server` directory and add your MongoDB URI and JWT secret:

```env
MONGO_URI=mongodb+srv://<your-db-username>:<your-db-password>@cluster0.mongodb.net/gigplus
JWT_SECRET=your_jwt_secret_key
```

2. Start the server:
```bash
cd server
npm run dev
```

### **Frontend (Client)**:
1. Start the React frontend:
```bash
cd client
npm start
```

Once the server and client are running, visit [http://localhost:3000](http://localhost:3000) to view the application.

---

## **Project Structure**

```bash
gig-plus/
│
├── client/                # Frontend (React)
│   ├── public/            # Static assets
│   └── src/
│       ├── components/    # React components
│       ├── pages/         # React pages (Home, Login, Profile, etc.)
│       ├── App.js         # Main app component
│       └── index.js       # Entry point for React
│
└── server/                # Backend (Node, Express)
    ├── config/            # Configuration (db connection, environment vars)
    ├── controllers/       # Logic for handling routes (user, job controllers)
    ├── models/            # Mongoose schemas (User, Job)
    ├── routes/            # API routes
    ├── middleware/        # Auth middleware (protecting routes)
    └── server.js          # Entry point for the server
```

---

## **API Routes**

### **User Authentication**

- **POST** `/api/users/register`: Register a new user
- **POST** `/api/users/login`: User login and JWT generation
- **GET** `/api/users/profile`: Get logged-in user profile
- **PUT** `/api/users/profile`: Update user profile

### **Job Listings**

- **GET** `/api/jobs`: Get all jobs (supports filtering via query parameters)
- **POST** `/api/jobs`: Create a new job (authenticated users)
- **GET** `/api/jobs/:id`: Get a single job by ID
- **PUT** `/api/jobs/:id`: Update job (only job poster can edit)
- **DELETE** `/api/jobs/:id`: Delete job (only job poster can delete)

---

## **Usage**

### **Job Listings**
- On the homepage, users can browse the list of available jobs.
- Use the **Filter Form** to filter jobs based on **location**, **pay rate**, or **job title**.

### **User Authentication**
- Sign up for a new account or login with an existing account.
- Upon successful login, a JWT token will be stored in the browser's local storage for future authentication.

### **Profile Management**
- Navigate to the **Profile** page to view or update your user information.
- See a list of jobs you've posted and manage them.

---

## **Contributing**

Contributions are welcome! If you find any issues or would like to improve the project, please feel free to submit a pull request.

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-branch-name`
3. Make your changes and commit: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature-branch-name`
5. Submit a pull request.

---

## **License**

This project is licensed under the MIT License. You are free to use, modify, and distribute the code.

---

**Gig+** - Empowering individuals to find gigs and job opportunities with ease.

---

