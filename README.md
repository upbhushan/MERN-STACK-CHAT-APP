# Real-Time Chat Application

A full-featured real-time chat application with user authentication, instant messaging, online status indicators, and media sharing capabilities.

## Features

- 🔐 **Secure Authentication**: JWT-based authentication with HTTP-only cookies
- 💬 **Real-time Messaging**: Instant message delivery using Socket.io
- 🖼️ **Media Sharing**: Send and receive images in conversations
- 🟢 **Online Status**: Real-time user online/offline indicators
- 🌓 **Theming**: Light/dark mode with customizable themes
- 📱 **Responsive Design**: Works seamlessly on mobile and desktop
- 📜 **Message History**: Paginated message loading for performance
- 🔔 **Notifications**: Visual indicators for new messages

## Tech Stack

### Frontend
- React + Vite
- Zustand for state management
- Socket.io-client for real-time communication
- TailwindCSS + DaisyUI for styling
- React Router for navigation

### Backend
- Node.js + Express
- MongoDB + Mongoose
- Socket.io for WebSockets
- JWT for authentication
- Cloudinary for image storage

## Installation

### Prerequisites
- Node.js (v14+)
- MongoDB
- Cloudinary account (for image uploads)

### Backend Setup
```bash
# Clone the repository
git clone https://github.com/yourusername/chat-app.git
cd chat-app/backend

# Install dependencies
npm install

# Create .env file
cp .env.example .env

# Fill in your environment variables
# - MONGODB_URI
# - JWT_SECRET
# - CLOUDINARY_CLOUD_NAME
# - CLOUDINARY_API_KEY
# - CLOUDINARY_API_SECRET

# Start the server
npm run dev




# Navigate to frontend directory
cd ../frontend

# Install dependencies
npm install

# Create .env file
cp .env.example .env

# Start the development server
npm run dev



# API Endpoints

## Authentication
- POST /api/auth/register - Register new user
- POST /api/auth/login - Login user
- POST /api/auth/logout - Logout user
- GET /api/auth/me - Get current user

## Users
- GET /api/users - Get all users
- GET /api/users/:id - Get user by ID
- PUT /api/users/:id - Update user profile

## Messages
- GET /api/messages/:userId - Get messages with specific user
- POST /api/messages - Send a new message
- GET /api/messages/latest - Get latest messages from all conversations

# Socket Events

## Client Emissions
- sendMessage - Send a new message
- typing - Indicate user is typing
- stopTyping - Indicate user stopped typing

## Server Emissions
- newMessage - New message received
- getOnlineUsers - List of online

Author
Bhushan Uparikar
IIIT Nagpur
