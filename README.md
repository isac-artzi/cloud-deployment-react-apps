# AIT-204 Cloud Deployment Projects

A collection of full-stack deep learning and web application tutorials demonstrating various cloud deployment strategies. Each project showcases different cloud platforms and deployment patterns for educational purposes.

## Projects Overview

This repository contains **5 complete projects** that demonstrate modern web development and cloud deployment techniques. Each project has its own detailed README and tutorial.

---

### 1. AIT-204-React-Azure
**Full-Stack Todo Application on Azure**

A production-ready todo application built with React and FastAPI, deployed on Microsoft Azure.

- **Frontend**: React (TypeScript) on Azure Static Web Apps
- **Backend**: FastAPI (Python) on Azure Container Apps
- **Features**: CRUD operations, filtering, responsive design
- **Highlights**: Containerized deployment, free-tier Azure services
- **Cost**: ~$5/month (Azure Container Registry only)

[→ View Project README](./AIT-204-React-Azure/README.md) | [→ Tutorial](./AIT-204-React-Azure/TUTORIAL.md)

---

### 2. AIT-204-React-Render
**Image Classification with Deep Learning**

A full-stack deep learning application for image classification using PyTorch/TensorFlow.

- **Frontend**: React on Render (Static Site)
- **Backend**: FastAPI with pre-trained ResNet model on Render
- **Features**: Image upload, real-time classification, confidence scores
- **Highlights**: Complete ML pipeline, educational deep learning tutorial
- **Cost**: Free tier available

[→ View Project README](./AIT-204-React-Render/README.md)

---

### 3. AIT-204-React-Vercel
**Deep Learning Deployment with Vercel + Railway**

Image classification application demonstrating Vercel and Railway deployment.

- **Frontend**: React (Vite) on Vercel
- **Backend**: FastAPI with TensorFlow/MobileNetV2 on Railway
- **Features**: Image classification, top-5 predictions, automatic documentation
- **Highlights**: Hybrid cloud deployment, optimized for ML workloads
- **Cost**: Free tier available on both platforms

[→ View Project README](./AIT-204-React-Vercel/README.md)

---

### 4. AIT-204-React-Vercel-Render
**Vercel + Render Deployment Pattern**

Alternative deployment approach using Vercel for frontend and Render for ML backend.

- **Frontend**: React on Vercel
- **Backend**: FastAPI with TensorFlow on Render
- **Features**: Image classification, health monitoring, batch processing support
- **Highlights**: Cost-effective hybrid deployment, detailed deployment guide
- **Cost**: Free tier available

[→ View Project README](./AIT-204-React-Vercel-Render/README.md)

---

### 5. AIT-204-React-local
**Browser-Based Deep Learning (No Backend Required)**

Handwritten digit recognition running entirely in the browser using TensorFlow.js.

- **Frontend**: React with TensorFlow.js
- **Backend**: None (client-side only)
- **Features**: Interactive drawing canvas, real-time prediction, model training in browser
- **Highlights**: No server costs, privacy-friendly, WebGL acceleration
- **Cost**: Free (static hosting only)

[→ View Project README](./AIT-204-React-local/README.md)

---

## Quick Comparison

| Project | Frontend Platform | Backend Platform | ML Framework | Use Case | Complexity |
|---------|------------------|------------------|--------------|----------|------------|
| React-Azure | Azure Static Web Apps | Azure Container Apps | None | Todo App | Medium |
| React-Render | Render | Render | PyTorch/TensorFlow | Image Classification | Medium |
| React-Vercel | Vercel | Railway | TensorFlow | Image Classification | Medium |
| React-Vercel-Render | Vercel | Render | TensorFlow | Image Classification | Medium |
| React-local | Any Static Host | None | TensorFlow.js | Digit Recognition | Easy |

---

## Learning Objectives

By working through these projects, you will learn:

### Cloud Deployment
- Deploy React applications on multiple platforms (Azure, Vercel, Render)
- Deploy FastAPI backends with containerization
- Configure environment variables and CORS
- Understand different cloud pricing models

### Full-Stack Development
- Build React frontends with modern hooks and state management
- Create RESTful APIs with FastAPI
- Handle file uploads and processing
- Implement proper error handling and validation

### Deep Learning Integration
- Load and serve pre-trained models (ResNet, MobileNetV2)
- Implement image preprocessing pipelines
- Run inference in production environments
- Deploy ML models in browsers with TensorFlow.js

### DevOps & Best Practices
- Git-based deployment workflows
- Environment-specific configurations
- Health checks and monitoring
- Cost optimization strategies

---

## Prerequisites

### Required Software
- **Node.js** (v14 or higher)
- **Python** (v3.8 or higher)
- **Git**
- **Docker** (for containerized deployments)

### Cloud Accounts (Free Tiers Available)
- **Azure Account** (for React-Azure project)
- **Vercel Account** (for Vercel projects)
- **Render Account** (for Render projects)
- **Railway Account** (for React-Vercel project)
- **GitHub Account** (for all projects)

---

## Getting Started

### Choose Your Learning Path

**Path 1: Start Simple** (Recommended for beginners)
1. Start with **AIT-204-React-local** (no backend, browser-only)
2. Move to **AIT-204-React-Render** (add backend deployment)
3. Try **AIT-204-React-Vercel** (learn multi-platform deployment)

**Path 2: Cloud Platform Focus**
1. Learn **AIT-204-React-Azure** (Microsoft Azure ecosystem)
2. Compare with **AIT-204-React-Vercel-Render** (alternative platforms)

**Path 3: Deep Learning Focus**
1. Explore **AIT-204-React-local** (browser-based ML)
2. Scale up with **AIT-204-React-Render** (server-based ML)
3. Deploy to **AIT-204-React-Vercel** (production ML)

### General Setup Steps

Each project follows a similar workflow:

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd AIT-204-cloud-deployment
   ```

2. **Navigate to a project**
   ```bash
   cd AIT-204-React-[project-name]
   ```

3. **Follow the project's README**
   - Each project has detailed setup instructions
   - Includes local development and deployment guides
   - Contains troubleshooting sections

---

## Project Structure

```
AIT-204-cloud-deployment/
├── README.md                          # This file
├── AIT-204-React-Azure/              # Azure deployment
│   ├── frontend/                     # React TypeScript app
│   ├── backend/                      # FastAPI with Docker
│   ├── README.md                     # Project documentation
│   └── TUTORIAL.md                   # Step-by-step guide
├── AIT-204-React-Render/             # Render deployment
│   ├── frontend/                     # React app
│   ├── backend/                      # FastAPI with ML
│   └── README.md
├── AIT-204-React-Vercel/             # Vercel + Railway
│   ├── frontend/                     # React with Vite
│   ├── backend/                      # FastAPI ML backend
│   └── README.md
├── AIT-204-React-Vercel-Render/      # Vercel + Render
│   ├── frontend/                     # React app
│   ├── backend/                      # FastAPI ML backend
│   └── README.md
└── AIT-204-React-local/              # Browser-based ML
    ├── src/                          # React + TensorFlow.js
    ├── public/
    └── README.md
```

---

## Common Technologies

### Frontend Stack
- **React** - UI library
- **Vite** - Build tool (some projects)
- **Create React App** - Build tool (some projects)
- **TypeScript** - Type safety (Azure project)
- **Axios** - HTTP client

### Backend Stack
- **FastAPI** - Python web framework
- **Uvicorn** - ASGI server
- **Pydantic** - Data validation
- **Python-multipart** - File upload handling

### Machine Learning
- **TensorFlow** - Deep learning framework
- **PyTorch** - Deep learning framework
- **TensorFlow.js** - Browser-based ML
- **Pre-trained Models** - ResNet, MobileNetV2

### DevOps & Deployment
- **Docker** - Containerization
- **GitHub Actions** - CI/CD (Azure project)
- **Azure CLI** - Azure deployments
- **Vercel CLI** - Vercel deployments

---

## Cost Considerations

All projects can be deployed on **free tiers**:

| Platform | Free Tier | Limitations |
|----------|-----------|-------------|
| Azure Static Web Apps | 100 GB bandwidth/month | Sufficient for learning |
| Azure Container Apps | 180,000 vCPU-seconds/month | Good for demos |
| Vercel | 100 GB bandwidth | Hobby projects |
| Render | 750 hours/month | Sleeps after inactivity |
| Railway | $5 free credit/month | Limited resources |

**Cost-Saving Tips:**
- Use free tiers for learning and testing
- Deploy during development, tear down when done
- Monitor usage in platform dashboards
- Use serverless for low-traffic apps

---

## Troubleshooting

### Common Issues Across Projects

**CORS Errors:**
- Verify backend CORS configuration includes frontend URL
- Check that API endpoint URLs are correct
- Ensure both frontend and backend are running

**API Connection Failed:**
- Confirm backend is running and accessible
- Check environment variables are set correctly
- Verify firewall/network settings

**Build Failures:**
- Clear caches: `npm cache clean --force`
- Delete `node_modules` and reinstall
- Check Node/Python versions

**Deployment Issues:**
- Review platform-specific logs
- Verify all environment variables are set
- Check that all files are committed to Git

For project-specific issues, consult individual README files.

---

## Learning Resources

### Documentation
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [React Documentation](https://react.dev/)
- [TensorFlow.js Guide](https://www.tensorflow.org/js)
- [Azure Documentation](https://docs.microsoft.com/azure)
- [Vercel Documentation](https://vercel.com/docs)
- [Render Documentation](https://render.com/docs)

### Tutorials & Courses
- [Full Stack Deep Learning](https://fullstackdeeplearning.com/)
- [FastAPI Tutorial](https://fastapi.tiangolo.com/tutorial/)
- [React Official Tutorial](https://react.dev/learn)

---

## Contributing

This is an educational repository for AIT-204 students. Contributions are welcome:

1. Fork the repository
2. Create a feature branch
3. Make improvements (code, documentation, examples)
4. Submit a pull request

**Ideas for contributions:**
- Add new deployment platforms (AWS, GCP)
- Improve error handling
- Add authentication examples
- Create video tutorials
- Add database integration examples

---

## License

MIT License - Free for educational and commercial use.

---

## Support & Contact

For questions and support:
- Check individual project README files
- Review troubleshooting sections
- Consult your course instructor
- Open an issue on GitHub

---

## Acknowledgments

These projects are designed for the **AIT-204 Cloud Deployment** course, demonstrating modern web development and cloud deployment best practices.

**Happy Learning & Building!** 🚀

---

*Last Updated: February 2026*
