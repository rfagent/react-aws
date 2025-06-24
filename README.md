# React Frontend - Pet Owners Social Network

A modern React frontend application built with Vite for a pet owners social network, featuring user authentication, post management, and pet profiles.

## 🚀 Features

- **User Authentication**: JWT-based login and registration system
- **Social Posts**: Create, view, and interact with posts from other pet owners
- **Pet Management**: Register and manage multiple pets per user
- **Comments System**: Comment on posts and view threaded discussions
- **Profile Images**: Upload and display user profile pictures
- **Responsive Design**: Mobile-friendly interface with modern CSS
- **Real-time Updates**: Dynamic content loading with pagination
- **Protected Routes**: Secure navigation with authentication guards

## 🛠 Tech Stack

- **React 18** - Modern React with functional components and hooks
- **Vite** - Fast build tool and development server
- **React Router DOM** - Client-side routing and navigation
- **Axios** - HTTP client for API communication
- **CSS3** - Custom styling with responsive design
- **ESLint** - Code linting and quality assurance

## 📋 Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager
- Running FastAPI backend server

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd react-aws
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Configuration**
   ```bash
   # Copy the environment template
   cp .env-sample .env
   
   # Edit .env with your configuration
   VITE_API_URL='http://localhost:8000'
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

5. **Access the application**
   - Open your browser and navigate to `http://localhost:3000`

## 📁 Project Structure

```
src/
├── auth/
│   ├── AuthContext.jsx       # Authentication state management
│   ├── LoginPage.jsx         # User login interface
│   ├── ProtectedRoute.jsx    # Route protection component
│   └── NotFound.jsx          # 404 error page
├── register/
│   └── RegisterPage.jsx      # User registration interface
├── posts/
│   ├── PostsList.jsx         # Main feed with infinite scroll
│   └── PostDetails.jsx       # Individual post view with comments
├── dogs/
│   ├── DogsAccount.jsx       # User's pet management
│   └── UserDogs.jsx          # View other users' pets
├── nav/
│   └── Navbar.jsx           # Navigation component
├── App.jsx                  # Main application component
├── App.css                  # Global styles
├── index.css               # Base styles
└── main.jsx               # Application entry point
```

## 🎯 Key Components

### Authentication System
- **AuthContext**: Centralized authentication state management
- **ProtectedRoute**: Guards routes requiring authentication
- **LoginPage/RegisterPage**: User authentication interfaces

### Posts Management
- **PostsList**: Main feed with infinite scroll pagination
- **PostDetails**: Detailed post view with comments functionality
- **New Post Creation**: Inline post creation with image support

### Pet Management
- **DogsAccount**: CRUD operations for user's pets
- **UserDogs**: View pets belonging to other users

### Navigation
- **Navbar**: Responsive navigation with authentication-aware links

## 🔑 Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `VITE_API_URL` | Backend API base URL | `http://localhost:8000` |

## 📱 Features Overview

### User Authentication
- Secure login/logout with JWT tokens
- User registration with profile image upload
- Persistent authentication state
- Automatic token validation

### Social Features
- Create and share posts
- View posts from other pet owners
- Comment on posts with threaded discussions
- View user profiles and their pets
- Infinite scroll pagination

### Pet Management
- Register multiple pets per user
- Add pet details (name, breed, age)
- View pets belonging to other users
- Delete owned pets

## 🎨 Styling Approach

The application uses custom CSS with:
- **Responsive Design**: Mobile-first approach with breakpoints
- **Component-based Styles**: Scoped styling for each component
- **Modern UI Elements**: Cards, hover effects, and smooth transitions
- **Consistent Color Scheme**: Professional blue and grey palette
- **Accessibility**: Proper contrast ratios and semantic markup

## 🔄 API Integration

The frontend communicates with the FastAPI backend through:

- **Authentication Endpoints**: Login, registration, token management
- **Posts API**: CRUD operations for posts and comments
- **Dogs API**: Pet management functionality
- **User Management**: Profile and image handling

### HTTP Client Configuration
```javascript
// Axios interceptors for authentication
headers: { 'Authorization': `Bearer ${token}` }
```

## 🚦 Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server on port 3000 |
| `npm run build` | Build production-ready application |
| `npm run preview` | Preview production build locally |
| `npm run lint` | Run ESLint for code quality checks |

## 🔒 Security Features

- **JWT Token Management**: Secure storage in localStorage
- **Route Protection**: Authentication guards for sensitive routes
- **Input Validation**: Client-side form validation
- **XSS Prevention**: Proper data sanitization
- **CORS Handling**: Configured for cross-origin requests

## 📈 Performance Optimizations

- **Code Splitting**: React Router-based lazy loading
- **Image Optimization**: Base64 encoding for profile pictures
- **Infinite Scroll**: Efficient pagination for large datasets
- **Memoization**: React hooks for performance optimization
- **Bundle Optimization**: Vite's tree-shaking and minification

## 🐛 Common Issues & Solutions

### Development Server Won't Start
```bash
# Clear node modules and reinstall
rm -rf node_modules package-lock.json
npm install
```

### API Connection Issues
- Verify backend server is running on correct port
- Check CORS configuration in FastAPI backend
- Ensure `.env` file has correct API URL

### Authentication Problems
- Clear localStorage: `localStorage.clear()`
- Check JWT token expiration
- Verify backend authentication endpoints

## 🔄 Development Workflow

1. **Feature Development**
   ```bash
   # Create feature branch
   git checkout -b feature/new-feature
   
   # Make changes and test
   npm run dev
   
   # Run linting
   npm run lint
   ```

2. **Building for Production**
   ```bash
   npm run build
   npm run preview  # Test production build
   ```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests and linting
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For issues and questions:
- Check the [Issues](link-to-issues) section
- Review the FastAPI backend documentation
- Ensure both frontend and backend are running on correct ports

---

**Note**: This frontend application requires the FastAPI backend to be running for full functionality. Make sure to start the backend server before running the React development server.# react-aws
