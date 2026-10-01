# 🐦 Twitter Clone

A full-stack social media web application inspired by Twitter/X, built with **React.js, Node.js, Express.js, MongoDB, and Cloudinary**.

The application allows users to create accounts, publish posts, interact with other users, follow/unfollow users, like and comment on posts, manage profiles, and receive notifications.

---

## 🚀 Features

### 🔐 Authentication

* User registration and login
* Secure password hashing using **bcryptjs**
* JWT-based authentication
* Authentication stored using HTTP cookies
* Protected routes
* Logout functionality
* Automatic user session verification

### 📝 Posts

* Create text-based posts
* Create posts with images
* Upload images using Cloudinary
* Delete your own posts
* Like/unlike posts
* Comment on posts
* View latest posts
* View posts from followed users
* View posts created by a specific user
* View liked posts

### 👥 User & Profile

* User profile pages
* Follow/unfollow users
* Followers and following counts
* Suggested users
* Edit profile information
* Update username, name, bio and link
* Upload profile and cover images
* Change password securely

### 🔔 Notifications

* Follow notifications
* Like notifications
* Notification read status
* Delete notifications

### 🎨 Frontend

* Responsive React interface
* Twitter/X-inspired UI
* Tailwind CSS styling
* React Router navigation
* Loading states and skeleton components
* Toast notifications
* Reusable React components

---

## 🛠️ Tech Stack

### Frontend

* **React.js**
* **Vite**
* **React Router**
* **Tailwind CSS**
* **React Icons**
* **React Hot Toast**
* **TanStack React Query**
* **JavaScript (ES6+)**

### Backend

* **Node.js**
* **Express.js**
* **MongoDB**
* **Mongoose**
* **JWT**
* **bcryptjs**
* **Cookie Parser**
* **dotenv**
* **Cloudinary**

### Development Tools

* Git & GitHub
* VS Code
* npm
* ESLint

---

## 📂 Project Structure

```text
Twitter Clone/
│
├── backend/
│   ├── controllers/
│   │   ├── auth.controller.js
│   │   ├── notification.controller.js
│   │   ├── post.controller.js
│   │   └── user.controller.js
│   │
│   ├── db/
│   │   └── connectMongoDB.js
│   │
│   ├── lib/
│   │   └── utils/
│   │       └── generateToken.js
│   │
│   ├── middleware/
│   │   └── protectRoute.js
│   │
│   ├── models/
│   │   ├── notification.model.js
│   │   ├── post.model.js
│   │   └── user.model.js
│   │
│   ├── routes/
│   │   ├── auth.route.js
│   │   ├── notification.route.js
│   │   ├── post.route.js
│   │   └── user.route.js
│   │
│   ├── package.json
│   └── server.js
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   │   ├── common/
│   │   │   ├── skeletons/
│   │   │   └── svgs/
│   │   │
│   │   ├── hooks/
│   │   ├── pages/
│   │   │   ├── auth/
│   │   │   ├── home/
│   │   │   ├── notification/
│   │   │   └── profile/
│   │   │
│   │   ├── utils/
│   │   ├── App.jsx
│   │   ├── index.css
│   │   └── main.jsx
│   │
│   ├── package.json
│   └── vite.config.js
│
├── .env-sample
├── .gitignore
└── package.json
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/supriyatiwari148/Twitter-Clone.git
```

Navigate into the project:

```bash
cd Twitter-Clone
```

---

### 2. Install Backend Dependencies

```bash
cd backend
npm install
```

---

### 3. Install Frontend Dependencies

Open another terminal and run:

```bash
cd frontend
npm install
```

---

## 🔑 Environment Variables

Create a `.env` file inside the `backend` folder.

Example:

```env
PORT=5000

MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

NODE_ENV=development
```

### Important

Never upload your real `.env` file to GitHub.

Your `.gitignore` should contain:

```gitignore
node_modules/
.env
dist/
```

Use `.env-sample` to show other developers which environment variables are required without exposing your credentials.

---

## ▶️ Running the Application

### Start Backend

From the `backend` directory:

```bash
npm start
```

The backend server will run on:

```text
http://localhost:5000
```

### Start Frontend

From the `frontend` directory:

```bash
npm run dev
```

Vite will provide a local development URL, normally:

```text
http://localhost:5173
```

Open that URL in your browser.

---

## 🔄 Application Flow

```text
User
 │
 ▼
React Frontend
 │
 │ HTTP Requests
 ▼
Express.js API
 │
 ├── Authentication
 ├── Users
 ├── Posts
 └── Notifications
 │
 ▼
MongoDB
 │
 ▼
Cloudinary
 │
 └── Image Storage
```

---

## 🔐 Authentication Flow

1. User creates an account or logs in.
2. Password is securely hashed using bcryptjs.
3. The server generates a JWT.
4. JWT is stored in an HTTP cookie.
5. Protected routes verify the authenticated user.
6. The user can access protected features such as posts, profiles, likes, comments and notifications.

---

## ☁️ Image Upload

The application uses **Cloudinary** for image management.

Images can be uploaded for:

* Posts
* Profile pictures
* Cover images

Cloudinary returns a secure image URL which is stored with the corresponding application data.

---

## 📡 API Structure

### Authentication

```text
/api/auth
```

Handles:

* Signup
* Login
* Logout
* Current user

### Users

```text
/api/users
```

Handles:

* User profiles
* Follow/unfollow
* Suggested users
* Profile updates

### Posts

```text
/api/posts
```

Handles:

* Create posts
* Delete posts
* Like/unlike
* Comments
* Feed posts
* User posts
* Liked posts
* Following posts

### Notifications

```text
/api/notifications
```

Handles:

* Get notifications
* Delete notifications

---

## 🧪 Available Frontend Commands

### Development

```bash
npm run dev
```

### Production Build

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

### Lint

```bash
npm run lint
```

---

## 📌 Learning Objectives

This project was developed to practice and understand:

* Full-stack web development
* React component architecture
* React Router
* REST API development
* Express.js
* MongoDB and Mongoose
* Authentication and authorization
* JWT-based authentication
* Password hashing
* CRUD operations
* File and image uploads
* Cloudinary integration
* Protected API routes
* Database relationships
* Git and GitHub workflow
* Frontend-backend integration

---

## 🔮 Future Improvements

Possible future enhancements include:

* Real-time messaging
* Real-time notifications
* Search functionality
* Hashtags and trending topics
* Post sharing/reposting
* Bookmarks
* Advanced post filtering
* Infinite scrolling
* Improved mobile responsiveness
* Deployment with production environment configuration

---

## 👩‍💻 Author

**Supriya Tiwari**

Computer Engineering Student

GitHub:
https://github.com/supriyatiwari148

---

## 📄 License

This project is created for **educational and portfolio purposes**.

It is an independent project inspired by the functionality and design concepts of modern social media platforms. It is not affiliated with or endorsed by Twitter or X Corp.
