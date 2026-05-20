# 🐙 OctoFit Tracker

Build your fitness journey with AI-powered insights!

## 📋 Project Structure

```
octofit-tracker/
├── frontend/                    # React 19 + Vite
│   ├── src/
│   │   ├── main.jsx            # React entry point
│   │   ├── App.jsx             # Main component
│   │   ├── App.css
│   │   └── index.css
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   └── tsconfig.json
│
├── backend/                     # Express + TypeScript
│   ├── src/
│   │   └── index.ts            # Express server
│   ├── package.json
│   ├── tsconfig.json
│   └── .env.example
│
└── README.md
```

## 🚀 Quick Start

### Prerequisites
- Node.js (v18+)
- MongoDB running locally or connection string

### 1. Frontend Setup (Port 5173)
```bash
cd octofit-tracker/frontend

# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build
```

### 2. Backend Setup (Port 8000)
```bash
cd octofit-tracker/backend

# Install dependencies
npm install

# Copy environment variables
cp .env.example .env

# Run development server
npm run dev

# Build TypeScript
npm run build

# Start production server
npm start
```

### 3. MongoDB Setup (Port 27017)
```bash
# Start MongoDB locally (macOS with Homebrew)
brew services start mongodb-community

# Or using Docker
docker run -d -p 27017:27017 --name mongodb mongo:latest
```

## 📊 Port Configuration

| Service | Port | Purpose |
|---------|------|---------|
| Frontend (Vite) | 5173 | React development server |
| Backend (Express) | 8000 | API server |
| MongoDB | 27017 | Database |

## 🔗 API Endpoints

- `GET /` - API information
- `GET /health` - Health check

## 🛠 Tech Stack

- **Frontend**: React 19, Vite, TypeScript
- **Backend**: Express.js, TypeScript, Node.js
- **Database**: MongoDB with Mongoose ODM
- **Development**: CORS enabled for cross-origin requests

## 📝 Environment Variables

Backend (.env):
```env
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
PORT=8000
NODE_ENV=development
```

## 🎯 Development Workflow

1. **Frontend changes**: HMR (Hot Module Replacement) enabled in Vite
2. **Backend changes**: Monitor and restart with ts-node
3. **Database**: Mongoose models auto-compile on save

## 📦 Dependencies

### Frontend
- React 19.0.0
- Vite 5.0.8

### Backend
- Express 4.18.2
- Mongoose 8.0.0
- TypeScript 5.3.3

## 🐛 Troubleshooting

**MongoDB connection error:**
- Ensure MongoDB is running on port 27017
- Check MONGODB_URI in .env

**Port already in use:**
- Change port in respective config file
- Or kill existing process: `lsof -ti:PORT | xargs kill -9`

**CORS issues:**
- Frontend proxy configured to http://localhost:8000
- Backend CORS middleware enabled

## 📄 License

MIT

## 👥 Contributing

This is a learning project for building modern multi-tier applications with Copilot.

---

**Happy coding! 🚀**
