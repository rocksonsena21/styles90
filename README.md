# 90+ Styles - Football Jersey Store

A full-stack e-commerce application for selling football jerseys, built with Django (backend) and React + TypeScript (frontend).

---

## 📋 Table of Contents

1. [Project Overview](#project-overview)
2. [Technology Stack](#technology-stack)
3. [Project Structure](#project-structure)
4. [Current Features](#current-features)
5. [API Endpoints](#api-endpoints)
6. [Getting Started](#getting-started)
7. [Recent Changes](#recent-changes)
8. [Future Enhancements](#future-enhancements)
9. [Contributing](#contributing)

---

## 🚀 Project Overview

**90+ Styles** is an e-commerce platform specializing in football jerseys. The application allows users to:

- Browse and search for football jerseys
- View product details
- Add items to cart
- Checkout with payment integration
- Admin users can manage products and orders

---

## 💻 Technology Stack

### Frontend

| Technology    | Version | Purpose            |
| ------------- | ------- | ------------------ |
| React         | 19.x    | UI Framework       |
| TypeScript    | 5.x     | Type Safety        |
| Vite          | 7.x     | Build Tool         |
| TailwindCSS   | 4.x     | Styling            |
| React Router  | 7.x     | Navigation         |
| Framer Motion | 12.x    | Animations         |
| Axios         | 1.x     | HTTP Client        |
| Paystack      | 2.x     | Payment Processing |

### Backend

| Technology            | Version | Purpose               |
| --------------------- | ------- | --------------------- |
| Django                | 6.x     | Web Framework         |
| Django REST Framework | 3.x     | API Development       |
| SimpleJWT             | 5.x     | Authentication        |
| SQLite                | -       | Database              |
| CORS Headers          | 4.x     | Cross-Origin Requests |

---

## 📂 Project Structure

```
90+Styles/
├── backend/                    # Django Backend
│   ├── products/              # Products app
│   │   ├── models.py           # Product & Category models
│   │   ├── views.py            # API views
│   │   ├── serializers.py      # DRF serializers
│   │   └── urls.py             # API routes
│   ├── users/                  # Users app
│   │   ├── models.py           # User Profile model
│   │   ├── views.py            # Auth views
│   │   ├── serializers.py      # Auth serializers
│   │   └── urls.py             # Auth routes
│   ├── styles90/               # Django project settings
│   │   ├── settings.py
│   │   └── urls.py
│   ├── staticfiles/            # Static files
│   ├── requirements.txt        # Python dependencies
│   ├── manage.py               # Django management
│   └── Procfile                # Deployment config
│
├── frontend/                   # React Frontend
│   ├── src/
│   │   ├── api/                # API client functions
│   │   ├── components/         # Reusable components
│   │   │   ├── admin/          # Admin components
│   │   │   └── store/          # Store components
│   │   ├── context/            # React Context
│   │   │   ├── AuthContext.tsx
│   │   │   ├── CartContext.tsx
│   │   │   └── JerseyContext.tsx
│   │   ├── pages/              # Page components
│   │   │   ├── Admin/          # Admin pages
│   │   │   ├── Auth/           # Auth pages
│   │   │   ├── Landing/        # Landing pages
│   │   │   └── Store/          # Store pages
│   │   ├── hooks/              # Custom React hooks
│   │   ├── styles/             # Global styles
│   │   ├── types/              # TypeScript types
│   │   ├── utils/              # Utility functions
│   │   ├── App.tsx             # Main app component
│   │   └── main.tsx            # Entry point
│   ├── package.json
│   ├── tailwind.config.js
│   ├── vite.config.ts
│   └── index.html
│
└── README.md                  # This file
```

---

## ✨ Current Features

### User Features

- **Landing Page**: Hero section, featured products, about section, contact form
- **Product Browsing**: Grid view with filtering and search
- **Product Details**: Detailed view with images and descriptions
- **Shopping Cart**: Add/remove items, quantity management
- **Checkout**: Payment integration with Paystack
- **User Authentication**: Login, Signup (username + email), Forgot password
- **Order Confirmation**: Thank you page after successful purchase

### Admin Features

- **Dashboard**: Overview of store statistics
- **Product Management**: Add, edit, delete products
- **Order Management**: View and manage customer orders

### Authentication System

- JWT-based authentication using SimpleJWT
- Token refresh mechanism
- User registration with validation
- Login with username or email

---

## 🔌 API Endpoints

### Authentication Endpoints

| Method | Endpoint              | Description       |
| ------ | --------------------- | ----------------- |
| POST   | `/api/auth/register/` | Register new user |
| POST   | `/api/auth/login/`    | User login        |
| POST   | `/api/auth/logout/`   | User logout       |
| POST   | `/api/auth/refresh/`  | Refresh JWT token |

### Product Endpoints

| Method | Endpoint             | Description            |
| ------ | -------------------- | ---------------------- |
| GET    | `/api/products/`     | List all products      |
| POST   | `/api/products/`     | Create product (admin) |
| GET    | `/api/products/:id/` | Get product details    |
| PUT    | `/api/products/:id/` | Update product (admin) |
| DELETE | `/api/products/:id/` | Delete product (admin) |

### Category Endpoints

| Method | Endpoint           | Description             |
| ------ | ------------------ | ----------------------- |
| GET    | `/api/categories/` | List all categories     |
| POST   | `/api/categories/` | Create category (admin) |

---

## 🛠️ Getting Started

### Prerequisites

- Python 3.8+
- Node.js 18+
- npm or yarn

### Backend Setup

```
bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Start development server
python manage.py runserver
```

The backend will run at `http://localhost:8000`

### Frontend Setup

```
bash
# Navigate to frontend directory
cd frontend

# Install dependencies
npm install

# Create .env file
echo "VITE_API_URL=http://localhost:8000" > .env

# Start development server
npm run dev
```

The frontend will run at `http://localhost:5173`

---

## 📝 Recent Changes

### Signup Page Update (Latest)

The signup page has been simplified to collect only essential information:

**Current Fields:**

- Username (required)
- Email address (required)
- Password (required)
- Confirm Password (required)

**Removed Fields:**

- Full Name
- Phone Number
- Address
- Profile Picture

This change streamlines the registration process while maintaining all necessary functionality for user authentication.

---

## 🔮 Future Enhancements

### Short-term Improvements

1. **Email Verification** - Add email verification flow for new registrations
2. **Password Reset** - Complete password reset functionality with email
3. **User Profile** - Allow users to view and edit their profile
4. **Order History** - Users can view their past orders
5. **Product Reviews** - Allow users to rate and review products
6. **Wishlist** - Add products to wishlist for later

### Medium-term Features

1. **Social Login** - Google and Facebook authentication
2. **Inventory Management** - Track stock levels
3. **Discount Codes** - Promo codes and coupons
4. **Newsletter** - Email subscription for updates
5. **Multi-language Support** - i18n for international users

### Long-term Enhancements

1. **Mobile App** - React Native or Flutter mobile application
2. **Real-time Notifications** - Push notifications for orders
3. **AI Recommendations** - Product recommendations based on browsing
4. **Advanced Analytics** - Sales analytics dashboard
5. **Multi-vendor Support** - Allow multiple sellers
6. **Live Chat** - Customer support chat

### Technical Improvements

1. **State Management** - Consider Redux or Zustand for complex state
2. **Testing** - Add unit and integration tests
3. **CI/CD** - Set up automated deployment pipeline
4. **Docker** - Containerize the application
5. **API Documentation** - Swagger/OpenAPI documentation
6. **Caching** - Implement Redis for performance

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is for educational and demonstration purposes.

---

## 📞 Support

For questions or issues, please open an issue on the repository.

---

_Last Updated: 2026_
