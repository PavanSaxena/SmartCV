# SmartCV - Resume Builder 💼📄

**SmartCV** is a full-stack resume builder application that allows users to enter their details and instantly generate a professionally styled PDF resume. The application is split into a responsive frontend for data entry and a powerful backend that handles PDF generation and data persistence.

---

## 🏗️ Tech Stack

### Frontend

- **React.js**
- **HTML5**, **CSS3**
- **Axios** for API requests
- **React Hook Form** for form validation
- **React Toastify** for notifications

### Backend

- **Node.js** with **Express**
- **MongoDB** with **Mongoose**
- **jsPDF** for dynamic PDF creation
- **bcryptjs** for password encryption

---

## 📁 Project Structure

```
SmartCV/
├── backend/
│   ├── models/
│   ├── server.js
│   ├── package.json
│   └── .env
└── frontend/
    ├── public/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   └── App.js
    └── package.json
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/PavanSaxena/SmartCV.git
cd SmartCV
```

### 2. Setup Backend

```bash
cd backend
npm install
```

Create a `.env` file:

```env
MONGODB_URI="mongodb://localhost:27017/smartcv"
```

Start the server:

```bash
node server.js
```

### 3. Setup Frontend

```bash
cd ../frontend
npm install
npm start
```

The frontend will run on `http://localhost:3000` and communicate with the backend at `http://localhost:5001`.

---

## ✨ Features

- **Login Required to Build Resume**
- **User Signup/Login Support**
- **PDF Resume Generator**
- **Responsive UI for All Devices**
- **PDF Download on Resume Submission**
- **Modern Clean Design**

---

## 🖥️ Frontend Overview

The frontend of **SmartCV** is built with React and provides a seamless, multi-page resume builder form with sections like:

- Personal Information
- Education History
- Work Experience
- Projects
- Skills and Interests

### Key Highlights

- 🔄 Uses **React Router** for navigation
- ✅ Validates input using **react-hook-form**
- 🔔 Shows status using **react-toastify**
- ⚙️ Modular form components (like `EducationForm`, `ExperienceForm`, etc.)
- 📦 Axios handles communication with backend API

### Frontend Scripts

```bash
npm start       # Start dev server on localhost:3000
npm run build   # Build static production-ready assets
```

---

## 📌 API Endpoints

### `POST /user/signup`

Registers a new user.

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "password": "securePassword"
}
```

### `POST /user/login`

Authenticates a user.

```json
{
  "email": "john@example.com",
  "password": "securePassword"
}
```

### `POST /api/users`

Generates PDF resume based on user input.

```json
{
  "personal": { ... },
  "education": [ ... ],
  "experiences": [ ... ],
  "projects": [ ... ],
  "skills": [ ... ]
}
```

Returns: **PDF resume** as a file.

---

## 🧪 Testing

Use tools like **Postman** or **Thunder Client** to test backend APIs independently.

---

## 💡 Future Improvements

- JWT-based authentication
- Resume templates and customization
- Email resume to user
- Export resume in DOCX format
- Dark mode

---

## 🤝 Contributing

We welcome contributions! Fork the repo and submit a pull request to add features or fix bugs.

---
