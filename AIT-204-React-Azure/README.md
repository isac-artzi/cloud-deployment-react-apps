# React + FastAPI Todo App - Azure Deployment

A full-stack Todo application built with React (TypeScript) and FastAPI (Python), deployed on Azure using Static Web Apps and Container Apps.

![Architecture](https://img.shields.io/badge/Frontend-React-blue)
![Backend](https://img.shields.io/badge/Backend-FastAPI-green)
![Cloud](https://img.shields.io/badge/Cloud-Azure-0089D6)

## 🚀 Features

- ✅ Create, read, update, and delete todos
- ✅ Mark todos as complete/incomplete
- ✅ Filter by all/active/completed
- ✅ Responsive design
- ✅ TypeScript for type safety
- ✅ RESTful API with automatic documentation
- ✅ Containerized backend
- ✅ Free-tier Azure deployment

## 🏗️ Architecture

```
┌─────────────────┐         ┌──────────────────┐
│  React Frontend │────────▶│  FastAPI Backend │
│  (Static Web    │  HTTPS  │  (Container Apps)│
│   App)          │◀────────│                  │
└─────────────────┘         └──────────────────┘
      Azure                       Azure
   Static Web Apps            Container Apps
```

## 📋 Prerequisites

- Node.js 18+
- Python 3.9+
- Docker (for deployment)
- Azure CLI
- Git

## 🛠️ Local Development

### Quick Start

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd AIT-204-React-Azure
   ```

2. **Start the Backend**
   ```bash
   cd backend
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
   ```

   Backend will run at: `http://localhost:8000`
   API docs at: `http://localhost:8000/docs`

3. **Start the Frontend** (new terminal)
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

   Frontend will run at: `http://localhost:5173`

4. **Test the Application**
   - Open `http://localhost:5173` in your browser
   - Create, update, and delete todos
   - Check the browser console for any errors

### Backend API Endpoints

- `GET /` - Health check
- `GET /api/todos` - Get all todos
- `POST /api/todos` - Create a new todo
- `GET /api/todos/{id}` - Get a specific todo
- `PUT /api/todos/{id}` - Update a todo
- `DELETE /api/todos/{id}` - Delete a todo

## 🌐 Azure Deployment

See [TUTORIAL.md](./TUTORIAL.md) for detailed deployment instructions.

### Quick Deploy Summary

1. **Deploy Backend to Azure Container Apps**
   ```bash
   # Set variables
   RESOURCE_GROUP="rg-todo-app"
   LOCATION="eastus"

   # Create resources
   az group create --name $RESOURCE_GROUP --location $LOCATION

   # Build and deploy (see TUTORIAL.md for full commands)
   ```

2. **Deploy Frontend to Azure Static Web Apps**
   - Connect your GitHub repository
   - Configure build settings
   - Deploy automatically via GitHub Actions

### Environment Variables

**Frontend (.env.production)**:
```env
VITE_API_URL=https://your-backend-url.azurecontainerapps.io
```

**Backend**:
No environment variables needed for basic setup.

## 📁 Project Structure

```
AIT-204-React-Azure/
├── backend/                 # FastAPI backend
│   ├── app/
│   │   ├── __init__.py
│   │   ├── main.py         # FastAPI app with CORS
│   │   ├── models.py       # Pydantic models
│   │   └── routes.py       # API routes
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/                # React frontend
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── services/       # API service
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── package.json
│   └── vite.config.ts
├── TUTORIAL.md             # Detailed tutorial
└── README.md               # This file
```

## 🧪 Testing

### Backend Tests
```bash
cd backend
# Health check
curl http://localhost:8000/

# Get all todos
curl http://localhost:8000/api/todos

# Create a todo
curl -X POST http://localhost:8000/api/todos \
  -H "Content-Type: application/json" \
  -d '{"title": "Test todo", "description": "Test description"}'
```

### Frontend Tests
- Open browser DevTools (F12)
- Check Console for errors
- Check Network tab for API calls
- Test all CRUD operations

## 🐳 Docker

### Build Backend Image
```bash
cd backend
docker build -t todo-api .
docker run -p 8000:8000 todo-api
```

## 💰 Cost Estimation

**Azure Services (Free Tier)**:
- Static Web Apps: FREE (100 GB bandwidth/month)
- Container Apps: FREE (180,000 vCPU-seconds/month)
- Container Registry: ~$5/month (only paid service)

**Total**: ~$5/month for low-traffic applications

## 🔧 Customization

### Add Database Support
Replace in-memory storage with PostgreSQL:
1. Add `sqlalchemy` and `psycopg2` to requirements.txt
2. Create database models
3. Use Azure Database for PostgreSQL (Burstable B1MS free tier)

### Add Authentication
- Azure AD B2C integration
- User-specific todos
- Protected routes

### Enhanced Features
- Todo categories/tags
- Due dates and reminders
- Search and sort
- Dark mode
- Export/import todos

## 📚 Resources

- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [React Documentation](https://react.dev/)
- [Azure Static Web Apps](https://docs.microsoft.com/en-us/azure/static-web-apps/)
- [Azure Container Apps](https://docs.microsoft.com/en-us/azure/container-apps/)
- [Vite Documentation](https://vitejs.dev/)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

MIT License - feel free to use this project for learning and development.

## 🐛 Troubleshooting

**CORS Errors**:
- Verify backend CORS origins include your frontend URL
- Check browser console for specific errors

**API Connection Failed**:
- Ensure backend is running on port 8000
- Verify `VITE_API_URL` in `.env.local`
- Check network tab in browser DevTools

**Build Failures**:
- Run `npm install` to ensure all dependencies are installed
- Clear node_modules and reinstall: `rm -rf node_modules package-lock.json && npm install`

## 👤 Author

Your Name - [GitHub](https://github.com/yourusername)

## 🌟 Acknowledgments

- Tutorial based on modern web development best practices
- Built for educational purposes
- Azure cloud deployment guide

---

**Happy Coding!** 🚀
