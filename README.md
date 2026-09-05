
smart-backend
Live website: https://verifiedsmart.netlify.app/
Backend API for the Smart website.  
Built with Node.js, Express, and MongoDB. Handles authentication, user management, and file uploads.

🚀 Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: MongoDB + Mongoose
- **Auth**: JWT + Google OAuth
- **File Upload**: Multer
- **Other**: Custom error middleware, file helpers

📁 Project Structure

smart-backend/
├── uploads/              # Uploaded files storage
├── AuthController.js     # Login, Register, Auth logic
├── Google.js             # Google OAuth integration
├── /Uploader.js           # Multer upload config
├── /upload.js             # Upload route handler
├── errorMiddleware.js    # Central error handling
├── /filehelper.js         # File utility functions
├── /generateToken.js      # JWT token generation
├── //mongo.js              # MongoDB connection
├── /user.js               # User model/schema
├── userRoutes.js         # User API routes
├── userfile.js           # User file operations
├── //index.js              # App entry point
├── //package.json
└── .gitignore

⚙️ Setup & Installation

1. Clone the repo
   ```bash
   git clone https://github.com/smartworkie/smart-backend.git
   cd smart-backend
2. *Install dependencies*
   npm install
3. *Environment Variables*  
   Create a `.env` file in the root:
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   GOOGLE_CLIENT_ID=your_google_client_id
   GOOGLE_CLIENT_SECRET=your_google_client_secret
4. *Run the server*
   npm start
For development with nodemon:
   npm run dev
🔑 API Endpoints

Auth
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/google` - Google OAuth login

Users
- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user
- `DELETE /api/users/:id` - Delete user

Uploads
- `POST /api/upload` - Upload file to `/uploads`

🛡️ Features

- JWT Authentication
- Google Sign-in
- File upload with Multer
- MongoDB integration
- Centralized error handling
- File helper utilities

📝 Scripts
"scripts": {
  "start": "node index.js",
  "dev": "nodemon index.js"
}
📄 License

MIT

---
Made with ❤️ by smartworkie

