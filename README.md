## 📂 Demo Repository

This repository contains the **demo version** of the project.

The **complete source code** is available in the original FinMK repository:
https://github.com/Manikumar4/MKCart (private)

# 🛒 MKCart E-commerce Application

A full-stack e-commerce application built with React, Node.js, and MongoDB. This is a **monorepo** where the backend serves both the API and the frontend React app.

## 🌟 Features

- **User Authentication**: JWT-based authentication with HTTP-only cookies
- **Product Management**: Browse, search, and filter products
- **Shopping Cart**: Add, remove, and manage cart items
- **Wishlist**: Save favorite products
- **Order Management**: Complete checkout process and order tracking
- **User Profile**: Manage personal information and preferences
- **AI Chat Assistant**: Interactive shopping assistant
- **Responsive Design**: Works on all devices
- **Real-time Notifications**: Toast notifications for user actions

## 🏗️ Architecture

- **Frontend**: React 19 + Redux Toolkit + RTK Query
- **Backend**: Node.js + Express + MongoDB
- **Authentication**: JWT + HTTP-only cookies
- **Styling**: CSS3 + Framer Motion animations
- **Deployment**: Monorepo - Backend serves frontend

## 🚀 Quick Start

### Development

```bash
# Install all dependencies
npm run install-all

# Start development servers
npm run dev
```

### Production

```bash
# Start production server (serves both frontend and backend)
npm start
```

## 📦 Project Structure

```
finalaimkcart/
├── package.json              # Root package.json (manages both)
├── backend/
│   ├── app.js               # Main server (auto-builds frontend)
│   ├── package.json         # Backend dependencies
│   ├── config/
│   │   └── config.env      # Backend environment
│   ├── controllers/         # API controllers
│   ├── models/             # MongoDB models
│   ├── routes/             # API routes
│   ├── middleware/         # Authentication middleware
│   └── utils/              # Backend utilities
└── frontend/
    ├── package.json         # Frontend dependencies
    ├── src/
    │   ├── components/     # React components
    │   ├── pages/          # Page components
    │   ├── store/          # Redux store and slices
    │   ├── utils/          # Frontend utilities
    │   └── styles/         # CSS files
    └── public/             # Static assets
```

## 🔧 Configuration

### Environment Variables

#### Backend (`backend/config/config.env`)

```env
PORT=8000
NODE_ENV=production
DB_URL=
JWT_SECRET_KEY=
APP_URL=https://mkcart2.onrender.com
FRONTEND_URL=https://mkcart2.onrender.com
```

#### Frontend (`frontend/.env`)

```env
REACT_APP_API_URL=https://mkshoppingbd.onrender.com
```

## 🌐 API Endpoints

### Authentication

- `POST /user/register` - User registration
- `POST /user/login` - User login
- `POST /user/logout` - User logout
- `GET /user/profile` - Get user profile
- `PUT /user/profile` - Update user profile

### Products

- `GET /products` - Get all products (with filters)
- `GET /product/:id` - Get single product
- `GET /products/recommendations` - Get recommended products
- `GET /products/related/:productId` - Get related products

### User Data (Protected)

- `GET /user/wishlist` - Get user wishlist
- `POST /user/wishlist` - Add to wishlist
- `DELETE /user/wishlist` - Remove from wishlist
- `GET /user/carts` - Get user cart
- `POST /user/carts` - Add to cart
- `PUT /user/carts` - Update cart
- `DELETE /user/carts` - Remove from cart
- `GET /user/orders` - Get user orders
- `POST /user/orders` - Create order
- `PUT /user/orders` - Update order
- `DELETE /user/orders` - Cancel order

## 🚀 Deployment

This application is configured for **monorepo deployment** where the backend serves both the API and the frontend.

### Deploy to Render

1. **Connect Repository**
   - Go to Render Dashboard
   - Create new Web Service
   - Connect your GitHub repository

2. **Configure Build Settings**
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`
   - **Root Directory**: `/`

3. **Set Environment Variables**
   ```env
   NODE_ENV=production
   PORT=8000
   DB_URL=
   JWT_SECRET_KEY=
   APP_URL=https://mkshoppingbd.onrender.com
   FRONTEND_URL=https://mkshoppingbd.onrender.com
   REACT_APP_API_URL=https://mkshoppingbd.onrender.com
   ```

### Deployment Process

1. **Install Dependencies**: `npm install` (installs root, backend, and frontend)
2. **Build Frontend**: Backend automatically builds React app
3. **Start Server**: `npm start` starts the backend
4. **Serve Frontend**: Backend serves the built React app

## 🎯 Key Features

### Authentication System

- JWT tokens stored in HTTP-only cookies
- Automatic token refresh
- Protected routes
- Global logout functionality

### Shopping Experience

- Product browsing with filters
- Add to cart/wishlist
- Real-time cart updates
- Secure checkout process

### User Management

- Profile management
- Order history
- Wishlist management
- Review system

### AI Integration

- Chat assistant for shopping help
- Product recommendations
- Order tracking assistance

## 🔒 Security Features

- HTTP-only cookies for JWT storage
- CORS protection
- Input validation
- Password hashing with bcrypt
- Protected API routes

## 📱 Responsive Design

- Mobile-first approach
- Works on all screen sizes
- Touch-friendly interface
- Progressive Web App features

## 🛠️ Technologies Used

### Frontend

- React 19
- Redux Toolkit
- RTK Query
- React Router
- Framer Motion
- Lucide React Icons
- React Toastify

### Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- JWT
- bcryptjs
- CORS

### Development

- Concurrently (for development)
- Nodemon (for backend development)

## 📄 License

MIT License - see LICENSE file for details

## 👥 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 🆘 Support

For support and questions:

- Check the documentation
- Review the deployment guide
- Open an issue on GitHub

---

**Built with ❤️ by MKCart**
