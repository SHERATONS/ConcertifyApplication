# 🎟️ Concertify

A **full-stack concert ticket-selling platform** for users and organizers, developed during your 3rd-4th year of college to improve frontend and backend skills.

---

## 🚀 Tech Stack

### 🖥️ Frontend

- **React (Vite):** SPA framework for fast development
- **Bootstrap 5:** Modern UI components
- **React Router:** Page routing
- **Axios:** HTTP requests to backend
- **Socket.IO Client:** Real-time seat updates
- **qrcode.react:** QR ticket generation
- **JWT:** Auth token storage
- **OAuth2:** Google, Facebook, Twitter login (Firebase or Spring Security)

### ⚙️ Backend

- **Spring Boot:** Main web framework
- **Spring Security + JWT:** User authentication & roles
- **Redis:** Real-time seat locking with TTL
- **WebSocket (STOMP/SockJS):** Live seat updates
- **PostgreSQL:** Relational database
- **Spring Data JPA:** ORM layer
- **JavaMailSender:** Email QR ticket delivery
- **ZXing:** QR code generation
- **Spring OAuth2:** Social login integration

### 🐳 Infrastructure

- **Docker Compose:** Full-stack orchestration
- **Docker:** Backend, frontend, Postgres, Redis
- **pgAdmin:** Optional GUI for DB
- **Postman / Swagger:** API testing & docs
- **GitHub:** Version control
- **Vercel / Render / Railway:** Deployment options

### 💳 Payments

- **Stripe (Test):** Credit card payments
- **PromptPay QR / TrueMoney Wallet:** Thai payment support (mock/API)

---

## 🗃️ Core Features

### 👤 User

- Register/login (JWT)
- OAuth login (Google, FB, Twitter)
- Browse concerts
- Book tickets (standing or seat)
- Real-time seat selection (with locking)
- Pay via PromptPay QR, Stripe, or TrueMoney (mock/real)
- Receive email confirmation with QR ticket
- View tickets on dashboard

### 🧑‍💼 Organizer

- Apply/register as an organizer
- Create concerts (standing or seating)
- Define zones, seats, price, ticket limits
- Set seat hold timer & payment window
- View sales reports & reserved tickets

---

## 🔐 Security

- Role-based access (user, organizer, admin)
- CAPTCHA to prevent bots
- Rate limiting
- JWT + OAuth2 authentication
- Seat lock timeout via Redis

---

### 🚀 Deployment Options (Choose One)

| Option                         | Backend                    | Frontend                       | Notes                            |
| ------------------------------ | -------------------------- | ------------------------------ | -------------------------------- |
| **1. Render (_Easy_)**         | Java Spring Boot           | Build + host on same or Vercel | Free tier, PostgreSQL add-on     |
| **2. Railway (_Easy_)**        | Spring Boot + Postgres     | Vercel frontend                | Good DB & Redis support          |
| **3. Fly.io (_Intermediate_)** | Lightweight Docker + Redis | Netlify/Vercel                 | Fast, efficient                  |
| **4. VPS (_Advanced_)**        | Full Docker stack          | Nginx reverse proxy            | Full control (e.g. DigitalOcean) |
