# 🏥 Book-Doctor

A full-stack doctor appointment booking system with three portals: User, Doctor, and Admin. Built with MERN stack and integrated payment gateways.

## 🎯 Overview

Healthcare appointment booking platform with:
- **Patient Portal**: Browse doctors, book appointments, manage profile
- **Doctor Portal**: Manage appointments, update availability, view dashboard
- **Admin Portal**: Add doctors, manage appointments, system overview

## ✨ Features

**Users**: Register/Login, Browse & filter doctors by specialty, Book appointments, Payment (Stripe/Razorpay), Profile management

**Doctors**: Dashboard with statistics, Manage appointments, Toggle availability, Profile updates

**Admin**: Add doctors, View all appointments, Manage system, Dashboard overview

## 🛠️ Tech Stack

**Frontend**: React.js, React Router, Axios, Tailwind CSS, Vite

**Backend**: Node.js, Express.js, MongoDB, Mongoose

**Auth**: JWT, bcrypt

**Storage**: Cloudinary (images), Multer

**Payments**: Stripe, Razorpay

## 🚀 Installation

See [SETUP.md](SETUP.md) for detailed instructions.

**Access**: Frontend (http://localhost:5173), Admin (http://localhost:5174), API (http://localhost:4000)

## 📁 Project Structure

```
Book-Doctor/
├── frontend/          # User portal (React)
│   └── src/
│       ├── components/    # Navbar, Footer, Header, etc.
│       ├── pages/         # Home, Doctors, Appointment, etc.
│       └── context/       # State management
├── admin/             # Admin & Doctor portal (React)
│   └── src/
│       ├── pages/
│       │   ├── Admin/     # Dashboard, AddDoctor, etc.
│       │   └── Doctor/    # DoctorDashboard, Profile, etc.
│       └── context/       # Admin/Doctor contexts
└── backend/           # Express API
    ├── config/        # MongoDB, Cloudinary
    ├── controllers/   # Business logic
    ├── middleware/    # Auth, file upload
    ├── models/        # User, Doctor, Appointment
    └── routes/        # API endpoints
```

## 📡 API Endpoints

**User** (`/api/user`): register, login, get/update profile, book/cancel appointment, payments

**Doctor** (`/api/doctor`): login, appointments, complete/cancel, change availability, profile, dashboard

**Admin** (`/api/admin`): login, add doctor, all appointments, all doctors, dashboard

## 🔐 Environment Setup

**MongoDB**: [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) or local installation

**Cloudinary**: Sign up at [Cloudinary](https://cloudinary.com/)

**Stripe**: Get keys at [Stripe](https://stripe.com/)

**Razorpay**: Get keys at [Razorpay](https://razorpay.com/)

---

Made with ❤️ for better healthcare management
