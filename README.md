# ChronoQuest

Create personalized fictional stories powered by AI. ChronoQuest is a cross-platform mobile app (React Native + Expo) with a secure Node.js/Express backend, integrated with Gemini AI, Firebase Auth, Firestore, and email delivery.

---

## ✨ Features
- Multi-step wizard for story creation (genre, author, heroes, length, delivery)
- Immersive in-app reader (font size, light/dark mode)
- Email delivery of generated stories
- Secure authentication (Firebase Auth)
- Stories saved to user profile (Firestore)
- Modern, responsive UI (Styled Components)

---

## 🛠️ Tech Stack
- **Frontend:** React Native (Expo), Styled Components, Firebase JS SDK
- **Backend:** Node.js, Express.js (Vercel serverless), Firebase Admin, Gemini API, SendGrid
- **Database:** Firebase Firestore
- **Auth:** Firebase Authentication
- **Hosting:** Vercel (frontend & backend)

---

## 🚀 Getting Started

### 1. Clone the repo
```sh
git clone https://github.com/yourusername/chronoquest.git
cd chronoquest
```

### 2. Set up Firebase
- Create a Firebase project at https://console.firebase.google.com/
- Enable **Authentication** (Email/Password)
- Create a **Firestore** database
- Get your **Web App config** (for frontend) and **Admin SDK** (for backend)

### 3. Set up Gemini API
- Get a Gemini API key from Google AI Studio (https://aistudio.google.com/app/apikey)

### 4. Set up Email (SendGrid)
- Create a SendGrid account and get an API key
- Verify your sender email address

### 5. Environment Variables
Copy `.env.example` to `.env` and fill in all required values:

```
# Backend (Vercel Serverless Functions)
GEMINI_API_KEY=your-gemini-api-key-here
SENDGRID_API_KEY=your-sendgrid-api-key-here
EMAIL_FROM=your-verified-sender@example.com
FIREBASE_PROJECT_ID=your-firebase-project-id
FIREBASE_CLIENT_EMAIL=your-firebase-adminsdk-email
FIREBASE_PRIVATE_KEY=your-firebase-adminsdk-private-key (use \n for newlines)

# Frontend (React Native, Expo)
# (No secrets should be exposed here)
```

For the frontend, update `frontend/constants/firebaseConfig.js` with your Firebase Web App config.

---

## 🧑‍💻 Running Locally

### Backend (API)
- Deployed automatically by Vercel from `/api` directory
- For local dev: use [Vercel CLI](https://vercel.com/docs/cli) or run with `node`/`vercel dev`

### Frontend (Expo App)
```sh
cd frontend
npm install
npx expo start
```
- Scan the QR code with Expo Go (iOS/Android)
- Or run on an emulator/simulator

---

## 🛡️ Security Notes
- **Never expose API keys or secrets in the frontend.**
- All AI and email API calls are made from the backend only.
- Firebase Auth tokens are used to secure all API endpoints.

---

## 🏗️ Deployment
- Deploy the root project to Vercel. The `/api` folder is auto-routed as serverless functions.
- The frontend (Expo) can be built and published via Expo or bundled as a static web app for Vercel.

---

## 📁 Project Structure
```
chronoquest/
  api/                # Backend (Vercel serverless functions)
  frontend/           # React Native (Expo) app
  vercel.json         # Vercel routing config
  .env.example        # Environment variable template
  README.md           # This file
```

---

## 📣 Credits
- Built with ❤️ by [Your Name]
