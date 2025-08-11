# URL Shortener

A modern, beautiful URL shortener application built with Node.js, Express, MongoDB, and EJS.

## ✨ Features

- 🔗 **URL Shortening**: Create short, memorable URLs
- 👤 **User Authentication**: Secure signup and login system
- 🎨 **Modern UI**: Beautiful, responsive design with animations
- 📊 **Analytics**: Track click history and visit statistics
- 🔒 **Secure**: JWT-based authentication and secure cookies
- 📱 **Responsive**: Works perfectly on all devices

## 🚀 Quick Start

### Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or cloud)
- npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd url-shortner2
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

4. **Start MongoDB**
   ```bash
   mongod
   ```

5. **Run the application**
   ```bash
   # Development
   npm run dev
   
   # Production
   npm start
   ```

6. **Open your browser**
   ```
   http://localhost:3000
   ```

## 🌍 Environment Variables

Create a `.env` file in the root directory:

```env
NODE_ENV=production
PORT=3000
MONGODB_URI=mongodb://127.0.0.1:27017/shorturl
JWT_SECRET=your-super-secret-jwt-key
COOKIE_SECRET=your-cookie-secret-key
```

## 🚀 Deployment Options

### Option 1: Render (Recommended - Free)

1. **Sign up** at [render.com](https://render.com)
2. **Create a new Web Service**
3. **Connect your GitHub repository**
4. **Configure the service:**
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
   - **Environment Variables**: Add your `.env` variables

### Option 2: Railway

1. **Sign up** at [railway.app](https://railway.app)
2. **Deploy from GitHub**
3. **Add environment variables**
4. **Deploy automatically**

### Option 3: Heroku

1. **Install Heroku CLI**
2. **Login and create app**
   ```bash
   heroku login
   heroku create your-app-name
   ```
3. **Set environment variables**
   ```bash
   heroku config:set MONGODB_URI=your-mongodb-uri
   heroku config:set JWT_SECRET=your-jwt-secret
   ```
4. **Deploy**
   ```bash
   git push heroku main
   ```

## 🗄️ Database Setup

### Local MongoDB
```bash
mongod
```

### MongoDB Atlas (Cloud)
1. Create account at [mongodb.com/atlas](https://mongodb.com/atlas)
2. Create a free cluster
3. Get your connection string
4. Update `MONGODB_URI` in your `.env` file

## 📁 Project Structure

```
url-shortner2/
├── controllers/          # Route controllers
├── middleware/           # Authentication middleware
├── model/               # Database models
├── routers/             # Route definitions
├── services/            # Business logic
├── views/               # EJS templates
├── connection.js        # Database connection
├── index.js            # Main application file
└── package.json        # Dependencies and scripts
```

## 🛠️ Available Scripts

- `npm start` - Start production server
- `npm run dev` - Start development server with nodemon
- `npm run build` - Build for production (no build step required)

## 🔧 Configuration

- **Port**: Configurable via `PORT` environment variable
- **Database**: MongoDB connection string via `MONGODB_URI`
- **JWT**: Secret key via `JWT_SECRET`
- **Cookies**: Secret key via `COOKIE_SECRET`

## 📱 API Endpoints

- `GET /` - Home page
- `GET /user/signup` - Signup page
- `GET /user/login` - Login page
- `POST /user/signup` - User registration
- `POST /user/login` - User authentication
- `GET /url` - URL management (requires auth)
- `POST /url` - Create short URL
- `GET /url/:shortId` - Redirect to original URL

## 🎨 Customization

The application uses EJS templates with modern CSS. You can customize:

- Colors and themes in the CSS files
- Layout and components in the EJS files
- Styling and animations

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

This project is licensed under the ISC License.

## 🆘 Support

If you encounter any issues:

1. Check the MongoDB connection
2. Verify environment variables
3. Check the console for error messages
4. Ensure all dependencies are installed

## 🔮 Future Enhancements

- [ ] User dashboard with analytics
- [ ] Custom domain support
- [ ] API rate limiting
- [ ] Bulk URL shortening
- [ ] QR code generation
- [ ] Social media integration
