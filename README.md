\# EduBlog4



A full-stack educational blogging platform built with the MERN stack (MongoDB, Express, React, Node.js).  

Authenticated users can create, read, update, delete (CRUD) posts, comment on them, and “like” each post once.



---



\## 🗂️ Table of Contents



1\. \[Features](#-features)  

2\. \[Tech Stack](#-tech-stack)  

3\. \[Prerequisites](#-prerequisites)  

4\. \[Getting Started](#-getting-started)  

&nbsp;  1. \[Backend Setup](#backend-setup)  

&nbsp;  2. \[Frontend Setup](#frontend-setup)  

5\. \[Environment Variables](#-environment-variables)  

6\. \[API Endpoints](#-api-endpoints)  

7\. \[Usage](#-usage)  

8\. \[Folder Structure](#-folder-structure)  

9\. \[License](#-license)  



---



\## 🚀 Features



\- \*\*User Authentication\*\*: Registration \& login with JWT.  

\- \*\*Blog CRUD\*\*: Create, read, update, delete posts (authors only).  

\- \*\*Image Uploads\*\*: Post images via Multer.  

\- \*\*Comments\*\*: Authenticated users can comment on posts.  

\- \*\*Likes\*\*: Incremental like counter; each user can like a post only once.  



---



\## 🛠️ Tech Stack



\- \*\*Frontend\*\*: React, React Router, Axios, Bootstrap, custom CSS  

\- \*\*Backend\*\*: Node.js, Express, Mongoose (MongoDB ODM)  

\- \*\*Authentication\*\*: bcryptjs (hashing), jsonwebtoken (JWT)  

\- \*\*File Uploads\*\*: Multer  

\- \*\*Misc.\*\*: CORS, dotenv  



---



\## 📋 Prerequisites



\- Node.js (v14+ recommended)  

\- npm or yarn  

\- MongoDB (local or Atlas)  

\- Git  



---



\## ⚙️ Getting Started



\### Backend Setup



1\. Open a terminal and `cd` into the backend folder:  

&nbsp;bash

&nbsp;cd edublog4/backend



Install dependencies:

bash

npm install

Create an uploads/ directory:



bash

mkdir uploads



Copy the example env file and fill in your values:

bash

cp .env.example .env

Start the server:



bash

npm run dev

The API will run on http://localhost:5000.



Frontend Setup

In a new terminal, cd into the frontend folder:



bash

cd edublog4/frontend



Install dependencies:



bash

npm install

Start the React app:



bash



npm start

The UI will open at http://localhost:3000.



🔑 Environment Variables

Create a .env file in backend/ with:



env

MONGO\_URI=your\_mongodb\_connection\_string

JWT\_SECRET=your\_jwt\_secret

PORT=5000       # optional, defaults to 5000



🔗 API Endpoints

All routes are prefixed with /api/blogs



| Method | Route                     | Auth | Description                            |

| ------ | ------------------------- | ---- | -------------------------------------- |

| POST   | `/api/blogs`              | ✅    | Create a new blog post                 |

| GET    | `/api/blogs`              | ❌    | Fetch all blog posts                   |

| GET    | `/api/blogs/:id`          | ✅    | Fetch a single post (and current user) |

| PUT    | `/api/blogs/:id`          | ✅    | Update a post (author only)            |

| DELETE | `/api/blogs/:id`          | ✅    | Delete a post (author only)            |

| POST   | `/api/blogs/:id/comments` | ✅    | Add a comment to a post                |

| PUT    | `/api/blogs/:id/like`     | ✅    | Like a post once per user              |



🎬 Usage

Register a new user or Log In.



Create a blog post with title, category, content, and optional image.



Browse posts on the dashboard; click a card to view details.



Like a post (only once).



Comment on any post.



Edit or Delete your own posts.



📁 Folder Structure

edublog4/

├─ backend/

│  ├─ models/           # Mongoose schemas (Blog.js, User.js)

│  ├─ routes/           # Express route handlers

│  ├─ middleware/       # authMiddleware.js

│  ├─ uploads/          # Image uploads

│  ├─ .env.example

│  ├─ server.js

│  └─ package.json

├─ frontend/

│  ├─ public/

│  ├─ src/

│  │  ├─ components/    # React components (BlogCard, BlogDetail…)

│  │  ├─ services/      # Axios instance (api.js)

│  │  ├─ styles/        # Custom CSS (home.css…)

│  │  └─ App.js

│  ├─ package.json

│  └─ README.md

└─ README.md

📄 License

This project is licensed under the MIT License.

