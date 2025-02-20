# Corporate Tournament Management Web App

## Overview
This web application streamlines corporate tournament management by handling event registrations, scoring, and leaderboards in real time. It enhances employee engagement and teamwork while maintaining anonymity through unique corporate codes. Judges can log scores, and the system automates total point calculations, leaderboards, and certificate generation.

## Features
- Event Creation & Registration: Admins can create events across multiple categories (indoor, outdoor, fun sports). Team leaders register using corporate codes to maintain anonymity.
- Scoring Dashboard for Judges: Judges input scores based on predefined criteria (5 for 1st, 3 for 2nd, 1 for 3rd), with automatic total calculation.
- Real-Time Leaderboard: Displays team standings and individual performances dynamically.
- Sponsorship Promotion: Ad spaces for sponsors with built-in analytics to measure engagement.
- Dynamic Certificate Generation: Automated certificates for participants and winners with unique verification codes.
- Best Athlete Recognition: Identifies the best athlete based on accumulated points.

## Tech Stack
- Frontend: React.js (Vite), Tailwind CSS
- Backend: Node.js, Express.js
- Database: MongoDB with Mongoose
- Authentication: JWT-based authentication
- Real-time Updates: Socket.io for live leaderboards
- File Handling: Multer for certificate generation
- Deployment: Vercel (Frontend), Render/Heroku (Backend)

## Installation

### Prerequisites
- Node.js (v16+)
- MongoDB (Local or Atlas)

### Setup

#### 1. Clone the Repository
\`\`\`sh
git clone https://github.com/yourusername/corporate-tournament-app.git
cd corporate-tournament-app
\`\`\`

#### 2. Install Dependencies
\`\`\`sh
# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
\`\`\`

#### 3. Configure Environment Variables
Create a .env file in the backend directory:
\`\`\`
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
\`\`\`

#### 4. Run the Application
\`\`\`sh
# Start backend server
cd backend
npm start

# Start frontend server
cd ../frontend
npm run dev
\`\`\`

## API Endpoints

### Admin
- POST /api/admin/create-event - Create an event
- GET /api/admin/events - Fetch all events

### Team Leader
- POST /api/team/register - Register team with corporate code
- GET /api/team/details - Get team details

### Judges
- POST /api/judge/submit-score - Submit scores for teams

### Public
- GET /api/leaderboard - Fetch real-time leaderboard
- GET /api/certificate/:id - Generate participant certificate

## License
MIT License
