# Blogify - A Modern Blogging Platform

A full-stack blogging application built with Node.js, Express, MongoDB, and EJS templating engine. This project provides a complete blogging platform with user authentication, blog creation, commenting system, and image upload functionality.

## 🚀 Features

- **User Authentication**: Sign up, sign in, and logout functionality
- **Blog Management**: Create, edit, and delete blog posts
- **Image Upload**: Upload cover images for blog posts using Multer
- **Comment System**: Comment on blog posts with user attribution
- **User Profiles**: User management with profile images
- **Responsive Design**: Modern UI with Bootstrap styling
- **Real-time Updates**: Dynamic content loading and updates

## 🛠️ Tech Stack

- **Backend**: Node.js with Express.js
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT tokens with cookie-based sessions
- **File Upload**: Multer for handling file uploads
- **Frontend**: EJS templating engine
- **Styling**: Bootstrap CSS framework
- **Password Security**: SHA-256 hashing with salt

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- Node.js (version 16.0.0 or higher)
- MongoDB (running locally or MongoDB Atlas connection)
- Git

## 🚀 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd Blogify
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   Create a `.env` file in the root directory with the following variables:
   ```env
   MONGO_URL=mongodb://localhost:27017/blogify
   PORT=8000
   JWT_SECRET=your-secret-key-here
   ```

4. **Start MongoDB**
   Make sure MongoDB is running on your system or update the MONGO_URL to point to your MongoDB instance.

5. **Run the application**
   ```bash
   npm start
   ```
   
   For development with auto-restart:
   ```bash
   npm run dev
   ```

6. **Access the application**
   Open your browser and navigate to `http://localhost:8000`

## 📁 Project Structure

```
Blogify/
├── app.js                 # Main application file
├── package.json           # Dependencies and scripts
├── .env                   # Environment variables (create this)
├── .gitignore            # Git ignore file
├── README.md             # Project documentation
├── models/               # Database models
│   ├── user.js          # User model
│   ├── blog.js          # Blog model
│   └── comment.js       # Comment model
├── routes/               # Express routes
│   ├── user.js          # User authentication routes
│   └── blog.js          # Blog management routes
├── middlewares/          # Custom middleware
│   └── authentication.js # JWT authentication middleware
├── services/             # Business logic services
│   └── authentication.js # Authentication service
├── views/                # EJS templates
│   ├── home.ejs         # Homepage
│   ├── signin.ejs       # Sign in page
│   ├── signup.ejs       # Sign up page
│   ├── blog.ejs         # Individual blog page
│   ├── addBlog.ejs      # Add blog page
│   └── partials/        # Reusable template parts
├── public/               # Static files
│   ├── images/          # Default images
│   └── uploads/         # User uploaded files
```

## 🔐 Authentication

The application uses JWT (JSON Web Tokens) for authentication:

- Tokens are stored in HTTP-only cookies
- Password hashing uses SHA-256 with random salt
- Session management through middleware

## 📝 API Endpoints

### User Routes
- `GET /user/signin` - Sign in page
- `POST /user/signin` - Authenticate user
- `GET /user/signup` - Sign up page
- `POST /user/signup` - Register new user
- `GET /user/logout` - Logout user

### Blog Routes
- `GET /` - Homepage with all blogs
- `GET /blog/add-new` - Add new blog page
- `POST /blog` - Create new blog
- `GET /blog/:id` - View specific blog
- `POST /blog/comment/:blogId` - Add comment to blog

## 🎨 Features in Detail

### Blog Creation
- Rich text blog posts with title and body
- Cover image upload support
- Automatic timestamp and author attribution

### Comment System
- Real-time commenting on blog posts
- User attribution for comments
- Nested comment display

### User Management
- Secure password hashing
- Profile image support
- User role system (USER/ADMIN)

### File Upload
- Image upload for blog covers
- Automatic file naming with timestamps
- File storage in public/uploads directory

## 🔧 Configuration

### Environment Variables
- `MONGO_URL`: MongoDB connection string
- `PORT`: Server port (default: 8000)
- `JWT_SECRET`: Secret key for JWT token generation

### Database
The application uses MongoDB with the following collections:
- `users`: User accounts and profiles
- `blogs`: Blog posts and metadata
- `comments`: Blog comments and replies

## 🚀 Deployment

To deploy this application:

1. Set up a MongoDB database (local or cloud)
2. Configure environment variables
3. Install dependencies: `npm install`
4. Start the server: `npm start`

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the ISC License.

## 👨‍💻 Author

This project was created as a learning exercise for full-stack web development with Node.js and MongoDB.

---

**Happy Blogging! 🚀**
