# 🌟 **TDS Project 2: Intelligent Data Analysis & Judgment Analysis Agent**

> **A powerful FastAPI-based service combining intelligent Q&A capabilities with Indian High Court judgment analysis, powered by Google Gemini AI and Wikipedia integration.**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.68+-green.svg)](https://fastapi.tiangolo.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black.svg)](https://github.com/21f3000697/Tds_Project_2)

---

## 📋 **Table of Contents**

- [Overview](#-overview)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Usage](#-usage)
- [API Endpoints](#-api-endpoints)
- [Configuration](#-configuration)
- [Technologies Used](#-technologies-used)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 **Overview**

**TDS Project 2** is a sophisticated FastAPI-based service that provides two powerful capabilities:

1. **🔍 Intelligent Q&A Agent**: Leverages Google Gemini AI and Wikipedia integration for comprehensive question answering
2. **⚖️ Judgment Analysis**: Analyzes Indian High Court judgments with statistical insights and visualizations

This project demonstrates advanced AI integration, data processing, and web scraping capabilities, making it ideal for legal research, data analysis, and intelligent information retrieval.

---

## ✨ **Features**

### **🤖 Intelligent Q&A Agent**
- **Dual-Mode Operation**: Automatically routes queries to Wikipedia or Google Gemini AI
- **Smart Routing**: Movie-related queries use Wikipedia scraping, general questions use Gemini LLM
- **File Input Support**: Accepts both text and file uploads for analysis
- **Context-Aware Responses**: Provides relevant, accurate answers based on query type

### **⚖️ Judgment Analysis System**
- **High Court Data Analysis**: Comprehensive analysis of Indian High Court judgments
- **Statistical Insights**: State-wise statistics and trends
- **Data Visualization**: Interactive plots and charts for better understanding
- **Remote Dataset Integration**: Connects to external judgment databases

### **🛠️ Technical Features**
- **FastAPI Framework**: High-performance, modern web framework
- **Async Processing**: Efficient handling of concurrent requests
- **Error Handling**: Robust error management and graceful degradation
- **Scalable Architecture**: Modular design for easy extension

---

## 🏗️ **Project Structure**

```
├── app.py              # Main FastAPI application  
├── requirements.txt    # Python dependencies  
├── Dockerfile          # Docker container setup  
├── Procfile            # For Heroku deployment  
├── runtime.txt         # Python runtime version  
├── entrypoint.sh       # Entrypoint script for deployment  
├── index.html          # Frontend interface (if any)  
├── .env.template       # Example environment variables  
├── DEPLOYMENT_GUIDE.md # Detailed deployment steps  
└── README.md           # Project documentation  

```

---

## 🚀 **Installation**

### **Prerequisites**
- Python 3.8 or higher
- pip package manager
- Google API key for Gemini AI

### **Step 1: Clone the Repository**
```bash
git clone https://github.com/21f3000697/Tds_Project_2.git
cd Tds_Project_2
```

### **Step 2: Install Dependencies**
```bash
pip install -r requirements.txt
```

### **Step 3: Environment Configuration**
Create a `.env` file in the root directory:
```env
GOOGLE_API_KEY=your_google_api_key_here
```

### **Step 4: Verify Installation**
```bash
python -c "import fastapi, uvicorn; print('Installation successful!')"
```

---

## 💻 **Usage**

### **Starting the Server**
```bash
# Development mode with auto-reload
uvicorn main:app --reload

# Production mode
uvicorn main:app --host 0.0.0.0 --port 8000
```

### **Accessing the Application**
- **Local Development**: http://localhost:8000
- **API Documentation**: http://localhost:8000/docs
- **Alternative Docs**: http://localhost:8000/redoc

---

## 🔌 **API Endpoints**

### **1. Judgment Analysis**
```http
GET /api/judgment-analysis/
```

**Response**: Returns summary statistics and visualizations for high court judgments

**Example Response**:
```json
{
  "total_judgments": 15000,
  "states_covered": 28,
  "analysis_period": "2020-2024",
  "visualization_url": "/static/plot.png"
}
```

### **2. Intelligent Q&A**
```http
POST /api/
```

**Request Body**:
```json
{
  "question": "What is the plot of Inception?",
  "file": null
}
```

**Response**: AI-generated answer using Wikipedia or Gemini LLM

---

## ⚙️ **Configuration**

### **Environment Variables**
| Variable | Description | Required | Default |
|----------|-------------|----------|---------|
| `GOOGLE_API_KEY` | Google Gemini AI API key | Yes | None |
| `PORT` | Server port | No | 8000 |
| `HOST` | Server host | No | 0.0.0.0 |

### **API Configuration**
- **Rate Limiting**: Configurable request limits
- **Timeout Settings**: Adjustable response timeouts
- **Model Selection**: Choose between different Gemini models

---

## 🛠️ **Technologies Used**

### **Backend Framework**
- **FastAPI**: Modern, fast web framework for building APIs
- **Uvicorn**: Lightning-fast ASGI server implementation

### **AI & Machine Learning**
- **Google Gemini AI**: Advanced language model for intelligent responses
- **LangChain**: Framework for developing applications with LLMs

### **Data Processing**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Matplotlib/Seaborn**: Data visualization

### **Web Scraping**
- **BeautifulSoup**: HTML parsing and web scraping
- **Requests**: HTTP library for making requests

### **Development Tools**
- **Python 3.8+**: Programming language
- **Git**: Version control
- **MIT License**: Open source licensing

---

## 🔧 **Development**

### **Running Tests**
```bash
# Install test dependencies
pip install pytest pytest-asyncio

# Run tests
pytest
```

### **Code Formatting**
```bash
# Install formatting tools
pip install black isort

# Format code
black .
isort .
```

### **Linting**
```bash
# Install linting tools
pip install flake8

# Run linter
flake8 .
```

---

## 🤝 **Contributing**

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch: `git checkout -b feature/amazing-feature`
3. **Commit** your changes: `git commit -m 'Add amazing feature'`
4. **Push** to the branch: `git push origin feature/amazing-feature`
5. **Open** a Pull Request

### **Contribution Guidelines**
- Follow PEP 8 style guidelines
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass

---

## 📄 **License**

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 TDS Project 2 Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## 📞 **Support & Contact**

- **GitHub Issues**: [Report bugs or request features](https://github.com/21f3000697/Tds_Project_2/issues)
- **Repository**: [View source code](https://github.com/21f3000697/Tds_Project_2)
- **Documentation**: [API docs available at `/docs` endpoint]

---

## 🙏 **Acknowledgments**

- **Google Gemini AI** for providing advanced language model capabilities
- **FastAPI** team for the excellent web framework
- **Open Source Community** for the amazing tools and libraries
- **Contributors** who help improve this project

---

## 📊 **Project Status**

![GitHub last commit](https://img.shields.io/github/last-commit/21f3000697/Tds_Project_2)
![GitHub issues](https://img.shields.io/github/issues/21f3000697/Tds_Project_2)
![GitHub pull requests](https://img.shields.io/github/issues-pr/21f3000697/Tds_Project_2)

---

**⭐ Star this repository if you find it helpful!**

---

*Built with ❤️ using FastAPI, Google Gemini AI, and modern Python technologies.*
