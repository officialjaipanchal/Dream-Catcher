# 🌙 Dream Catcher

A comprehensive dream journaling platform that enables users to capture, organize, and analyze their dreams through multiple media formats including text, audio, and video recordings.

[![React](https://img.shields.io/badge/React-18.2.0-blue.svg)](https://reactjs.org/)
[![React Native](https://img.shields.io/badge/React%20Native-0.72.10-blue.svg)](https://reactnative.dev/)
[![Node.js](https://img.shields.io/badge/Node.js-16+-green.svg)](https://nodejs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-7.5.0-green.svg)](https://mongodb.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## ✨ Features

### 🌟 Multi-Format Dream Capture
- **Text Dreams**: Rich text editor for detailed dream descriptions
- **Audio Dreams**: High-quality audio recording with playback
- **Video Dreams**: Video recording with camera integration
- **Media Upload**: Support for existing audio/video files

### 📱 Cross-Platform Experience
- **Web Application**: Modern React.js website with responsive design
- **Mobile App**: React Native app with Expo for iOS and Android
- **Synchronized Data**: Seamless data sync between platforms

### 🔐 Security & Authentication
- **JWT Authentication**: Secure token-based authentication
- **Password Security**: bcrypt hashing with password reset functionality
- **Protected Routes**: Role-based access control
- **Input Validation**: Comprehensive form validation and sanitization

### 📊 Analytics & Insights
- **Dream Statistics**: Comprehensive analytics dashboard
- **Mood Tracking**: Track emotional patterns in dreams
- **Calendar Heatmap**: Visual dream frequency patterns
- **Achievement System**: Gamified progress tracking with milestones
- **Progress Goals**: Personal goal setting and tracking

### 🎯 Smart Organization
- **Advanced Filtering**: Filter by type, mood, date, and tags
- **Search Functionality**: Full-text search across all dreams
- **Tagging System**: Custom tags for dream categorization
- **Favorites**: Mark and organize important dreams
- **Auto-Backup**: Cloud storage integration for data safety

### 📈 Data Visualization
- **Chart.js Integration**: Beautiful charts and graphs
- **Dream Type Distribution**: Pie charts for media types
- **Mood Analysis**: Visual mood pattern analysis
- **Engagement Tracking**: Calendar heatmap for activity patterns
- **Streak Tracking**: Daily recording streak visualization

## 🏗️ Architecture

```
Dream Catcher/
├── DCWebsite/                 # React.js Web Application
│   ├── src/
│   │   ├── Components/        # React components
│   │   ├── services/          # API services
│   │   └── firebase/          # Firebase configuration
│   └── public/                # Static assets
├── Dream-Catcher - App/       # React Native Mobile App
│   ├── Components/            # Mobile components
│   └── src/                   # Mobile assets
├── dream-catcher-backend-node/ # Node.js Backend API
│   ├── models/                # MongoDB schemas
│   ├── routes/                # API endpoints
│   └── services/              # Business logic
└── scripts/                   # Setup and deployment scripts
```

## 🚀 Quick Start

### Prerequisites

- **Node.js** (v16 or higher)
- **npm** or **yarn**
- **MongoDB** (local or cloud)
- **Expo CLI** (for mobile development)

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/dream-catcher.git
cd dream-catcher
```

### 2. Backend Setup

```bash
# Navigate to backend directory
cd dream-catcher-backend-node

# Install dependencies
npm install

# Create environment file
cp .env.example .env
# Edit .env with your configuration

# Start MongoDB (if local)
brew services start mongodb-community  # macOS
# or use your preferred method

# Start the backend server
npm start
```

**Environment Variables:**
```env
PORT=8080
MONGODB_URI=mongodb://localhost:27017/dreamcatcher
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
NODE_ENV=development
FRONTEND_URL=http://localhost:3000
RESEND_API_KEY=your_resend_api_key_here
```

### 3. Web Application Setup

```bash
# Navigate to website directory
cd DCWebsite

# Install dependencies
npm install

# Create environment file
cp .env.example .env
# Edit .env with your configuration

# Start the development server
npm start
```

**Environment Variables:**
```env
REACT_APP_API_URL=http://localhost:8080
REACT_APP_NAME=Dream Catcher
REACT_APP_VERSION=1.0.0
```

### 4. Mobile App Setup

```bash
# Navigate to mobile app directory
cd "Dream-Catcher - App"

# Install dependencies
npm install

# Start Expo development server
npx expo start
```

## 📱 Features in Detail

### Dream Management
- **Create Dreams**: Add new dreams with title, content, and media
- **Edit Dreams**: Update existing dreams with full editing capabilities
- **Delete Dreams**: Remove dreams with confirmation
- **View Dreams**: Detailed dream viewer with media playback
- **Dream Types**: Support for text, audio, and video formats

### User Profile & Analytics
- **Profile Management**: Update personal information and preferences
- **Dream Statistics**: Comprehensive analytics and insights
- **Achievement System**: Unlock achievements based on usage
- **Progress Tracking**: Visual progress bars and goal completion
- **Export/Backup**: Data export and backup functionality

### Search & Organization
- **Advanced Search**: Search by title, content, tags, and date
- **Filtering**: Filter by dream type, mood, and favorites
- **Sorting**: Sort by date, title, or creation time
- **Tagging**: Add custom tags for better organization
- **Categories**: Organize dreams by categories

## 🔌 API Endpoints

### Authentication
```http
POST /auth/register          # User registration
POST /auth/signin           # User sign in
POST /auth/forgot-password  # Password reset request
POST /auth/reset-password   # Password reset with token
GET  /auth/verify-reset-token/:token  # Verify reset token
```

### Dreams (JWT Required)
```http
GET    /dreams              # Get all dreams for user
POST   /dreams              # Create new dream
GET    /dreams/:id          # Get specific dream
PUT    /dreams/:id          # Update dream
DELETE /dreams/:id          # Delete dream
GET    /dreams/stats        # Get dream statistics
```

### Profile (JWT Required)
```http
GET /profile                # Get user profile
PUT /profile                # Update user profile
```

### Contact
```http
POST /contact               # Send contact message
```

### Health
```http
GET /health                 # Health check endpoint
```

## 🛠️ Technology Stack

### Frontend (Web)
- **React.js** - Modern UI library
- **React Router** - Client-side routing
- **PrimeReact** - UI component library
- **Chart.js** - Data visualization
- **React Calendar Heatmap** - Activity visualization
- **Axios** - HTTP client

### Mobile
- **React Native** - Cross-platform mobile development
- **Expo** - Development platform
- **React Navigation** - Mobile navigation
- **Expo AV** - Audio/video handling
- **Expo Camera** - Camera integration
- **AsyncStorage** - Local data storage

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB ODM
- **JWT** - Authentication tokens
- **bcrypt** - Password hashing
- **Helmet** - Security middleware
- **Morgan** - HTTP request logging

### Development Tools
- **Nodemon** - Development server
- **ESLint** - Code linting
- **Prettier** - Code formatting

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: bcrypt with salt rounds
- **Input Validation**: Comprehensive form validation
- **CORS Protection**: Cross-origin resource sharing
- **Helmet Security**: Security headers middleware
- **Environment Variables**: Secure configuration management
- **Rate Limiting**: API rate limiting protection

## 📊 Database Schema

### User Model
```javascript
{
  email: String (required, unique),
  password: String (required, hashed),
  name: String,
  premium: Boolean (default: false),
  resetPasswordToken: String,
  resetPasswordExpires: Date,
  createdAt: Date,
  updatedAt: Date
}
```

### Dream Model
```javascript
{
  user: ObjectId (ref: User, required),
  title: String (required),
  content: String,
  type: String (enum: ["text", "audio", "video"]),
  mediaUrl: String,
  tags: [String],
  isFavorite: Boolean (default: false),
  mood: String (enum: ["happy", "sad", "excited", "scared", "peaceful", "confused", "neutral"]),
  lucid: Boolean (default: false),
  recurring: Boolean (default: false),
  dreamDate: Date,
  createdAt: Date,
  updatedAt: Date
}
```

## 🚀 Deployment

### Backend Deployment
```bash
# Production build
npm run build

# Environment setup
NODE_ENV=production
MONGODB_URI=your_production_mongodb_uri
JWT_SECRET=your_production_jwt_secret
```

### Frontend Deployment
```bash
# Build for production
npm run build

# Deploy to your preferred hosting service
# (Netlify, Vercel, AWS, etc.)
```

### Mobile App Deployment
```bash
# Build for production
expo build:android
expo build:ios

# Or use EAS Build
eas build --platform all
```

## 🤝 Contributing

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Development Guidelines
- Follow the existing code style
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **React Team** - For the amazing React ecosystem
- **Expo Team** - For the excellent mobile development platform
- **MongoDB Team** - For the powerful database solution
- **Chart.js Team** - For the beautiful data visualization library

## 📞 Support

- **Email**: support@dreamcatcher.com
- **Issues**: [GitHub Issues](https://github.com/yourusername/dream-catcher/issues)
- **Documentation**: [Wiki](https://github.com/yourusername/dream-catcher/wiki)

## 🔮 Roadmap

- [ ] AI-powered dream analysis
- [ ] Dream sharing and social features
- [ ] Advanced analytics and insights
- [ ] Voice-to-text transcription
- [ ] Dream pattern recognition
- [ ] Integration with sleep tracking devices
- [ ] Multi-language support
- [ ] Dark mode theme
- [ ] Offline mode support
- [ ] Push notifications for dream reminders

---

**Made with ❤️ by the Dream Catcher Team**

*Capture your dreams, understand your mind.* 
