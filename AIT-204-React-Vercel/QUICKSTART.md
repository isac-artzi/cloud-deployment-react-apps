# Quick Start Guide
## Get Running in 5 Minutes

This guide gets you up and running as fast as possible.

## 📦 Prerequisites

- Node.js 18+ ([Download](https://nodejs.org/))
- Python 3.8+ ([Download](https://python.org/))

## 🚀 Quick Setup

### 1. Clone Repository

```bash
git clone <your-repo-url>
cd AIT-204-React-Vercel
```

### 2. Setup Backend (Terminal 1)

```bash
# Navigate to backend
cd backend

# Create virtual environment
python -m venv venv

# Activate (macOS/Linux)
source venv/bin/activate

# Activate (Windows)
# venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Start server
uvicorn app.main:app --reload
```

✅ Backend running at: `http://localhost:8000`

### 3. Setup Frontend (Terminal 2)

```bash
# Navigate to frontend
cd frontend

# Install dependencies
npm install

# Create environment file
echo "VITE_API_URL=http://localhost:8000" > .env.local

# Start development server
npm run dev
```

✅ Frontend running at: `http://localhost:5173`

### 4. Test the Application

1. Open `http://localhost:5173` in your browser
2. Upload an image (JPG or PNG)
3. Click "Classify Image"
4. View predictions!

## 🎯 What's Happening?

- **Backend**: FastAPI server with MobileNetV2 model
  - On first run, downloads model (~14MB)
  - Processes images and returns predictions
  - API docs at: `http://localhost:8000/docs`

- **Frontend**: React app built with Vite
  - Provides UI for image upload
  - Communicates with backend API
  - Displays classification results

## 📝 Next Steps

1. **Read the Full Tutorial**: [README.md](README.md)
2. **Deploy Your App**: [DEPLOYMENT.md](DEPLOYMENT.md)
3. **Run Tests**: [TESTING.md](TESTING.md)

## 🐛 Common Issues

### Backend won't start

```bash
# Make sure virtual environment is activated
which python
# Should show path to venv

# Reinstall dependencies
pip install -r requirements.txt
```

### Frontend can't connect to backend

```bash
# Check .env.local exists
cat frontend/.env.local
# Should show: VITE_API_URL=http://localhost:8000

# Make sure backend is running
curl http://localhost:8000/health
```

### Port already in use

```bash
# Change backend port
uvicorn app.main:app --reload --port 8001

# Update frontend .env.local
echo "VITE_API_URL=http://localhost:8001" > frontend/.env.local
```

## 💡 Pro Tips

- **First Time**: Model download takes ~1 minute
- **Dev Tools**: Press F12 to see network requests
- **API Docs**: Visit `http://localhost:8000/docs`
- **Hot Reload**: Both servers auto-reload on code changes

## 🎓 Learning Path

1. ✅ Get it running (you're here!)
2. 📖 Understand the code (README.md)
3. 🧪 Test locally (TESTING.md)
4. 🚀 Deploy to production (DEPLOYMENT.md)
5. 🎨 Customize and extend

---

**Happy Coding!** 🚀

For detailed explanations, see [README.md](README.md)
