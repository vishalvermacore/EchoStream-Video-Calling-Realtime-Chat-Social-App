# Streamify

Streamify is a full-stack web application designed to connect language learners worldwide. It allows users to create accounts, find language partners, send friend requests, chat, and even make video calls. The application is built with a modern tech stack, including React, Vite, TailwindCSS, Node.js, Express, MongoDB, and Stream APIs.

---

## Table of Contents


1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [Project Structure](#project-structure)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Environment Variables](#environment-variables)
7. [Scripts](#scripts)
8. [API Endpoints](#api-endpoints)
9. [Contributing](#contributing)
10. [License](#license)

---
## Features

- **User Authentication**: Sign up, log in, and log out securely using JWT-based authentication.
- **Onboarding**: Users can complete their profiles with details like bio, native language, and learning language.
- **Friend Requests**: Send, accept, and manage friend requests.
- **Chat**: Real-time messaging powered by Stream Chat API.
- **Video Calls**: Initiate video calls with friends using Stream Video API.
- **Theme Selector**: Choose from multiple themes using DaisyUI and Zustand for state management.
- **Responsive Design**: Fully responsive UI built with TailwindCSS.

---
## Tech Stack

### Frontend
- **React**: Component-based UI library.
- **Vite**: Fast development server and build tool.
- **TailwindCSS**: Utility-first CSS framework.
- **DaisyUI**: TailwindCSS component library.
- **React Query**: Data fetching and caching.
- **Zustand**: State management.
- **Stream Chat & Video SDKs**: Real-time chat and video call functionality.

### Backend
- **Node.js**: JavaScript runtime.
- **Express**: Web framework for building APIs.
- **MongoDB**: NoSQL database for storing user and friend data.
- **Stream Chat & Video APIs**: Real-time communication services.
- **JWT**: Secure authentication.

---
## Project Structure

STREAMIFY/ ├── backend/ │ ├── src/ │ │ ├── controllers/ # API logic │ │ ├── lib/ # Database and Stream API utilities │ │ ├── middleware/ # Authentication middleware │ │ ├── models/ # Mongoose schemas │ │ ├── routes/ # API routes │ │ └── server.js # Entry point for the backend │ ├── package.json # Backend dependencies and scripts │ └── .env # Backend environment variables ├── frontend/ │ ├── src/ │ │ ├── components/ # Reusable React components │ │ ├── constants/ # Static data like themes and languages │ │ ├── hooks/ # Custom React hooks │ │ ├── lib/ # Utility functions and API calls │ │ ├── pages/ # React pages │ │ ├── store/ # Zustand state management │ │ ├── App.jsx # Main React component │ │ └── main.jsx # React entry point │ ├── public/ # Static assets │ ├── index.html # HTML template │ ├── tailwind.config.js # TailwindCSS configuration │ ├── vite.config.js # Vite configuration │ ├── package.json # Frontend dependencies and scripts │ └── .env # Frontend environment variables ├── package.json # Root-level scripts ├── .gitignore # Ignored files and directories └── README.md # Project documentation

---
## Installation

### Prerequisites
- Node.js (v16+)
- MongoDB
- Stream API credentials (API Key and Secret)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/streamify.git
   cd streamify

2. Install dependencies:

npm install --prefix backend

npm install --prefix frontend   

3. Set up environment variables:

- Create .env files in both backend/ and frontend/ directories.

- Refer to the Environment Variables section for required variables.

4. Start the development servers:

npm run dev --prefix backend

npm run dev --prefix frontend
## Usage

1. Open the frontend in your browser at http://localhost:5173.
2. Sign up for a new account or log in with existing credentials.
3. Complete the onboarding process to start connecting with language partners.
4. Explore features like friend requests, chat, and video calls.
## Environment Variables
Backend (backend/.env)

PORT=5001
MONGO_URI=your_mongodb_connection_string
JWT_SECRET_KEY=your_jwt_secret
STEAM_API_KEY=your_stream_api_key
STEAM_API_SECRET=your_stream_api_secret
NODE_ENV=development

Frontend (frontend/.env)

VITE_STREAM_API_KEY=your_stream_api_key
## Scripts

Root-Level Scripts

- npm run build: Installs dependencies and builds the frontend.
- npm run start: Starts the backend server.

Backend Scripts
- npm run dev: Starts the backend server in development mode with nodemon.

Frontend Scripts
- npm run dev: Starts the frontend development server.
- npm run build: Builds the frontend for production.
- npm run preview: Previews the production build.
## API Endpoints

Authentication

- POST /api/auth/signup: Create a new user.
- POST /api/auth/login: Log in a user.
- POST /api/auth/logout: Log out a user.
- POST /api/auth/onboarding: Complete user onboarding.
- GET /api/auth/me: Get the authenticated user's details.

Users

- GET /api/users: Get recommended users.
- GET /api/users/friends: Get the user's friends.
- POST /api/users/friend-request/:id: Send a friend request.
- PUT /api/users/friend-request/:id/accept: Accept a friend request.
- GET /api/users/friend-requests: Get incoming and accepted friend requests.
- GET /api/users/outgoing-friend-requests: Get outgoing friend requests.
Chat

- GET /api/chat/token: Get a Stream Chat token for the authenticated user.
## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch: git checkout -b feature-name.
3. Commit your changes: git commit -m "Add feature-name".
4. Push to the branch: git push origin feature-name.
5. Open a pull request.
## License
This project is licensed under the MIT License. You are free to use, modify, and distribute this project as per the terms of the license.
