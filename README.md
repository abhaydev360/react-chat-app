React + Spring Boot Chat Application

A real-time chat application built with React (frontend) and Spring Boot (backend).
This project demonstrates modern full-stack development with WebSockets, REST APIs, and database integration for persistent chat.

🚀 Features

Real-time Messaging with WebSockets

User Authentication & Authorization (JWT-based)

Private & Group Chats

Message Persistence in Database (MySQL/PostgreSQL/any supported DB)

Typing Indicators & Online Status

Responsive UI with React + Tailwind/Material UI

REST APIs for user and message management

Docker Support for deployment

🛠️ Tech Stack
Frontend (React)

React 18+

React Router

Axios (API calls)

Socket.io (or native WebSocket)

TailwindCSS / Material UI

Backend (Spring Boot)

Spring Boot 3+

Spring WebSocket / STOMP

Spring Security (JWT Authentication)

Spring Data JPA / Hibernate

Database: MySQL / PostgreSQL

Maven / Gradle

📂 Project Structure
chat-application/
│── backend/                 # Spring Boot backend
│   ├── src/main/java/com/chatapp
│   │   ├── controller/      # REST & WebSocket controllers
│   │   ├── model/           # Entity classes
│   │   ├── repository/      # JPA Repositories
│   │   ├── service/         # Business logic
│   │   └── security/        # JWT auth
│   └── src/main/resources/  # application.properties
│
│── frontend/                # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/      # UI components
│   │   ├── pages/           # React pages
│   │   ├── services/        # Axios API calls
│   │   └── App.js           # Root component
│
└── docker-compose.yml       # For running backend + frontend + db

⚙️ Setup & Installation
1️⃣ Clone the Repository
git clone https://github.com/your-username/chat-application.git
cd chat-application

2️⃣ Backend (Spring Boot)

Go to backend directory:

cd backend


Configure application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/chatdb
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
jwt.secret=your-secret-key


Run the backend:

mvn spring-boot:run


Backend will start at http://localhost:8080

3️⃣ Frontend (React)

Go to frontend directory:

cd frontend


Install dependencies:

npm install


Start React app:

npm start


Frontend will start at http://localhost:3000

🔗 API Endpoints
Authentication

POST /api/auth/register → Register new user

POST /api/auth/login → Login user & get JWT

Chat

GET /api/messages/{chatId} → Fetch chat messages

POST /api/messages → Send new message

WS: /chat → WebSocket endpoint

🐳 Run with Docker
docker-compose up --build


This will start:

React frontend on http://localhost:3000

Spring Boot backend on http://localhost:8080

MySQL database on localhost:3306

📸 Screenshots

(Add your UI screenshots here)

📌 Future Enhancements

File Sharing (images, docs)

Push Notifications

User Profile & Avatar

Message Reactions (like 👍 ❤️ 😂)

🤝 Contributing

Fork the repo

Create a feature branch (git checkout -b feature-xyz)

Commit changes (git commit -m 'Add xyz feature')

Push to branch (git push origin feature-xyz)

Open a Pull Request

📜 License

This project is licensed under the MIT License.
