# 🏥 BDA-HealthCare-MERN

> A full-stack healthcare data management system built with the MERN stack — enabling patients, doctors, and admins to manage health records, appointments, and medical data through a clean, responsive web interface.

![Tech Stack](https://img.shields.io/badge/Stack-MERN-green) ![JavaScript](https://img.shields.io/badge/Language-JavaScript-yellow) ![MongoDB](https://img.shields.io/badge/Database-MongoDB-brightgreen) ![License](https://img.shields.io/badge/License-MIT-blue)

---

## 📸 Screenshots

> See the [`/ss`](./ss) folder for full UI screenshots.

---

## 🗂️ Project Structure

```
BDA-HealthCare-MERN/
├── client/                  # React frontend (CRA)
│   ├── public/
│   └── src/
│       ├── components/      # Reusable UI components
│       ├── pages/           # Route-level page components
│       ├── context/         # React context for auth/state
│       └── App.js
│
├── controllers/             # Express route handler logic
│   ├── authController.js
│   ├── patientController.js
│   └── doctorController.js
│
├── middleware/              # Auth & error middleware
│   └── authMiddleware.js
│
├── models/                  # Mongoose schemas
│   ├── User.js
│   ├── Patient.js
│   ├── Doctor.js
│   └── Appointment.js
│
├── routes/                  # Express API routes
│   ├── authRoutes.js
│   ├── patientRoutes.js
│   └── doctorRoutes.js
│
├── ss/                      # UI Screenshots
├── .env                     # Environment variables (not committed)
├── server.js                # Express app entry point
└── package.json
```

---

## ✨ Features

- **Authentication** — JWT-based login/register for patients, doctors, and admins
- **Patient Management** — Create, view, update, and delete patient health records
- **Doctor Profiles** — Manage doctor details, specializations, and availability
- **Appointment Scheduling** — Book and manage appointments between patients and doctors
- **Protected Routes** — Middleware guards ensure role-based access control
- **Responsive UI** — React frontend with clean component architecture
- **RESTful API** — Well-structured Express routes with controller separation

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React.js, CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Auth | JWT (JSON Web Tokens) |
| Dev Tools | Nodemon, dotenv |

---

## 🚀 Getting Started

### Prerequisites

- Node.js v16+
- MongoDB (local or [MongoDB Atlas](https://www.mongodb.com/cloud/atlas))
- npm

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/DivitaP/BDA-HealthCare-MERN.git
cd BDA-HealthCare-MERN
```

**2. Install backend dependencies**
```bash
npm install
```

**3. Install frontend dependencies**
```bash
cd client
npm install
cd ..
```

**4. Configure environment variables**

Create a `.env` file in the root directory:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

**5. Run the app**

Run backend and frontend concurrently:
```bash
npm run dev
```

Or separately:
```bash
# Backend (from root)
npm start

# Frontend (from /client)
cd client && npm start
```

**6. Open in browser**
```
http://localhost:3000
```

---

## 📡 API Endpoints

### Auth
| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login and receive JWT |

### Patients
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/patients` | Get all patients |
| GET | `/api/patients/:id` | Get patient by ID |
| POST | `/api/patients` | Create patient record |
| PUT | `/api/patients/:id` | Update patient record |
| DELETE | `/api/patients/:id` | Delete patient record |

### Doctors
| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/doctors` | Get all doctors |
| GET | `/api/doctors/:id` | Get doctor by ID |
| POST | `/api/doctors` | Create doctor profile |
| PUT | `/api/doctors/:id` | Update doctor profile |

---

## 👥 Team

| Roll No | Name |
|---|---|
| 8590 | Shreya Bilonikar |
| 8618 | Carol Mendonca |
| 8626 | Divita Phadakale |

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
