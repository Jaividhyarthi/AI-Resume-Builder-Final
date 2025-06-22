# 🧠 AI Resume Builder

The AI Resume Builder is a modern web application that helps users quickly generate, edit, and manage professional resumes using AI. Built with React, Clerk for authentication, and Strapi as the CMS backend, it provides a seamless and user-friendly experience.

---

## 📁 Project Structure

AI-Resume-Builder-Final/
├── backend/ # Strapi backend (Node.js CMS)
│ └── src/api/user-resume/ # Content-type for storing user resumes
├── frontend/ # Vite + React frontend
│ ├── src/
│ │ ├── auth/ # Clerk sign-in page
│ │ ├── dashboard/ # Resume dashboard components
│ │ ├── home/ # Landing page
│ │ ├── components/ # Shared components
│ │ ├── App.jsx
│ │ └── main.jsx
│ ├── .env # Frontend environment config
│ └── index.html
└── README.md


## 🚀 Features

- ✅ User authentication with Clerk
- ✅ Create, edit, and view resumes
- ✅ Store and fetch resume data from Strapi
- ✅ Clean dashboard with editable UI components
- ✅ Responsive design using Tailwind CSS

---

## 🔧 Tech Stack

| Technology      | Purpose                              |
|-----------------|--------------------------------------|
| **React**       | Frontend framework                   |
| **Vite**        | Fast bundler for React               |
| **Tailwind CSS**| Styling and responsive UI            |
| **Strapi**      | CMS backend and REST API provider    |
| **Clerk**       | User Authentication and Sessions     |
| **Axios**       | API calls between frontend and Strapi|

---

## 🌍 Environment Variables

### Frontend `.env`

```env
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
VITE_API_BASE_URL=https://your-strapi-url.strapiapp.com/api
VITE_STRAPI_API_KEY=your_strapi_api_token  # Optional if public role allows access
Important: Don't include /admin in the API base URL.

🔐 Clerk Setup
Go to Clerk Dashboard

Create a new application

Copy the Publishable Key

Paste it in .env as VITE_CLERK_PUBLISHABLE_KEY

Enable "Email address" in Sign-in options

Add allowed redirect URLs (e.g., http://localhost:5173/*)

🧰 Backend Setup (Strapi)
Option 1: Use Strapi Cloud
Go to Strapi Cloud

Create a new project using the Blank template

Create a Collection Type named user-resume with fields:

title (text)

resumeId (UID)

userEmail (email)

userName (text)

In Settings > API Tokens, create a token for frontend access.

In Roles > Public, allow find, findOne, and create permissions for user-resume.

Option 2: Run locally

npx create-strapi@latest my-strapi-backend
cd my-strapi-backend
npm install
npm run develop
Set up the same collection type and permissions.

⚙️ Frontend Setup
cd frontend
npm install
npm run dev
🛠 Backend API Methods
Function	HTTP Method	Description
CreateNewResume(data)	POST	Creates a new resume entry
GetUserResumes(email)	GET	Fetches all resumes by user
UpdateResumeDetail()	PUT	Updates resume content
GetResumeById(id)	GET	Gets a single resume with data
DeleteResumeById(id)	DELETE	Deletes a resume

🧪 Development Scripts
Script	Purpose
npm run dev	Run React app using Vite
npm run build	Build for production
npm run preview	Preview production build

✅ Deployment Guide
Frontend
Push to GitHub

Deploy using Vercel, Netlify, or GitHub Codespaces

Ensure .env is updated and VITE_* variables are available in the environment settings

Backend
Deploy on Strapi Cloud or platforms like Railway/Render

Make sure the /api/user-resumes endpoint is publicly accessible or protected by API key

Whitelist the frontend domain in CORS settings

🧠 Credits
Inspired by YouTube project: “AI Resume Builder using React, Clerk, and Strapi”

Design inspired by Shadcn UI and Tailwind components

Built with ❤️ by Jaividhyarthi Vivekanand


📬 Contact
For any support or collaboration requests:
📧 jaividhyarthivivekanand@gmail.com


Let me know if you'd like to include installation screenshots or auto-deployment inst
