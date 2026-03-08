# Book-Doctor - Setup and Installation Guide

## Prerequisites
- Node.js (v14 or higher)
- MongoDB (local installation or MongoDB Atlas account)
- npm or yarn package manager

## Installation Steps

### 1. Clone the Repository
```bash
git clone <repository-url>
```

### 2. Navigate to Project Directory
```bash
cd Book-Doctor
```

### 3. Install Backend Dependencies
```bash
cd backend
npm i
cd ..
```

### 4. Install Frontend Dependencies
```bash
cd frontend
npm i
cd ..
```

### 5. Install Admin Panel Dependencies
```bash
cd admin
npm i
cd ..
```

## Database Configuration

### MongoDB Setup

The application currently uses MongoDB for database operations. You need to configure your own MongoDB connection.

#### Option 1: Local MongoDB
1. Install MongoDB on your local machine
2. Start MongoDB service
3. Create a `.env` file in the `backend` directory
4. Add the following environment variable:
   ```
   MONGODB_URI=mongodb://localhost:27017/book-doctor
   ```

#### Option 2: MongoDB Atlas (Cloud)
1. Create a free account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
2. Create a new cluster
3. Get your connection string
4. Create a `.env` file in the `backend` directory
5. Add the following environment variable:
   ```
   MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/book-doctor?retryWrites=true&w=majority
   ```
   Replace `<username>` and `<password>` with your MongoDB Atlas credentials

### Other Environment Variables

Create a `.env` file in the `backend` directory and add the following variables:

```env
MONGODB_URI=<your-mongodb-connection-string>
JWT_SECRET=<your-jwt-secret-key>
CLOUDINARY_NAME=<your-cloudinary-name>
CLOUDINARY_API_KEY=<your-cloudinary-api-key>
CLOUDINARY_SECRET_KEY=<your-cloudinary-secret-key>
ADMIN_EMAIL=<admin-email>
ADMIN_PASSWORD=<admin-password>
```

**Note:** Replace all placeholder values with your actual credentials.

## Running the Application

### Start Backend Server
```bash
cd backend
npm start
```
The backend server will start on the configured port (usually `http://localhost:4000` or `http://localhost:5000`)

### Start Frontend
Open a new terminal:
```bash
cd frontend
npm run dev
```
The frontend will start on `http://localhost:5173` (default Vite port)

### Start Admin Panel
Open another new terminal:
```bash
cd admin
npm run dev
```
The admin panel will start on `http://localhost:5174` (or next available port)

## Access the Application

- **Frontend (User):** http://localhost:5173
- **Admin Panel:** http://localhost:5174
- **Backend API:** http://localhost:4000 (or your configured port)

## Troubleshooting

### MongoDB Connection Issues
- Ensure MongoDB service is running (for local setup)
- Check if the connection string is correct
- Verify network access in MongoDB Atlas (add your IP to whitelist)
- Check if the database user has proper permissions

### Port Already in Use
If you get a port conflict error, you can:
- Stop the process using that port
- Change the port in the configuration files

### Dependencies Issues
If you encounter dependency errors:
```bash
# Clear npm cache
npm cache clean --force

# Delete node_modules and package-lock.json
rm -rf node_modules package-lock.json

# Reinstall dependencies
npm install
```

## Project Structure
- **backend/** - Express.js server and API
- **frontend/** - User-facing React application
- **admin/** - Admin dashboard React application

## Support
For issues and questions, please refer to the main [README.md](README.md) or create an issue in the repository.
