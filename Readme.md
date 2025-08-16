# Chelsea Bridge Lift Forecast System

> **Note: This is a mockup dashboard using synthetic data. Real implementation completed under NDA with MassDOT.**

<div align="center">

![Dashboard Screenshot](images/dashboard-home.png)
![Dashboard Screenshot](images/dashboard-notfications.png)

**Achieved 75% prediction accuracy • 30-minute advance warnings • Real-time ML integration**

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org)
[![Machine Learning](https://img.shields.io/badge/ML-Random%20Forest-orange.svg)](https://scikit-learn.org)

</div>

## Project Overview

The Chelsea Bridge Lift Forecast System is a machine learning-powered dashboard that revolutionizes bridge lift predictions for the Chelsea Street Bridge in Boston. By integrating real-time environmental data with historical patterns, the system provides accurate forecasts that help thousands of daily commuters avoid traffic delays.

**The Challenge:** Chelsea residents face severe transportation constraints with limited pathways to Boston, frequent bridge lifts (5+ daily), and prediction accuracy that had declined from 80% to approximately 50%.

**The Solution:** An intelligent forecasting system that achieved **75% accuracy** by leveraging multiple data sources and ML algorithms.

---

## Problem Statement & Impact

### **The Transportation Crisis**
- **Geographic Isolation**: Chelsea has no subway access and only a few congested bus routes to Boston
- **Critical Bottleneck**: The Chelsea Street Bridge is one of only three primary roadways
- **Daily Disruptions**: Each bridge lift lasts 15+ minutes, occurring 5+ times per day
- **Failed Predictions**: Existing notification system accuracy dropped to around 50%, making reliable trip planning difficult

### **Real-World Impact**
- **Thousands** of daily commuters affected by unpredictable delays
- **30-45 minutes** of potential delays during peak bridge lift periods
- **30-minute** advance warnings enable better trip planning
- **25%** improvement in prediction accuracy reduces commuter frustration

---

## Technical Solution & Results

### **Key Achievements**
| Metric | Before | After | Improvement |
|--------|--------|-------|-------------|
| **Prediction Accuracy** | ~50% | **75%** | +25% |
| **Data Integration** | 1 source | **5+ sources** | Real-time |
| **User Channels** | 2 | **4** | Multi-platform |

### **Machine Learning Architecture**
```python
# Core ML Pipeline
├── Data Ingestion
│   ├── Historical bridge lift logs (2019-2025)
│   ├── Real-time weather API (OpenWeatherMap)
│   ├── Tide level data (NOAA)
│   └── Vessel scheduling notifications
├── Feature Engineering
│   ├── Temporal patterns (day, hour, season)
│   ├── Environmental factors (weather, tide)
│   └── Vessel type classifications
├── Model Training
│   ├── Random Forest Classifier
│   ├── Time series analysis
│   └── Cross-validation with temporal splits
└── Real-time Prediction
    ├── 30-minute advance forecasts
    ├── Confidence scoring (0-100%)
    └── Automated notifications
```

---

## Dashboard Design

**Requirement:** MassDOT needed a reliable system for commuters to quickly check bridge lift predictions.

**Solution:** Clean interface with prominent lift predictions, confidence scoring, and minimal design for sub-5-second information access.

---

## Technical Stack

### **Frontend**
- **React 18** - Modern component-based UI
- **Tailwind CSS** - Utility-first styling for rapid development
- **Chart.js** - Interactive data visualizations
- **Lucide React** - Consistent iconography
- **Responsive Design** - Cross-platform compatibility

### **Backend**
- **Python 3.8+** - Core application logic
- **Flask** - Lightweight web framework
- **scikit-learn** - Machine learning algorithms
- **pandas** - Data manipulation and analysis
- **PostgreSQL** - Reliable data storage

### **APIs & Integration**
- **OpenWeatherMap** - Real-time weather data
- **NOAA Tides** - Tide level information
- **Custom ML Model** - Bridge lift predictions
- **Twitter API** - Social media notifications

### **Deployment**
- **Docker** - Containerized deployment
- **GitHub Actions** - CI/CD pipeline
- **Automated Testing** - Frontend and backend validation

---

## 🔧 Installation & Quick Start

### **Prerequisites**
```bash
- Python 3.8+
- Node.js 16+
- Git
- Docker (optional)
```

### **Setup Instructions**
```bash
# Clone repository
git clone https://github.com/yourusername/chelsea-bridge-ai.git
cd chelsea-bridge-ai

# Quick setup (runs everything automatically)
./scripts/setup_project.sh

# OR Manual setup:

# Backend setup
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python app.py

# Frontend setup (new terminal)
cd frontend
npm install
npm start

# Access dashboard at http://localhost:3000
```

### **Docker Deployment**
```bash
# One-command deployment
docker-compose up --build

# Access at http://localhost:3000
```

---

## Advanced Features & Future Roadmap

### **Current Capabilities**
- **Multi-source Data Integration** - Combines weather, tide, and historical data
- **Predictive Confidence Scoring** - Transparent uncertainty estimates
- **Automated Notification System** - Streamlined alert distribution
- **Historical Pattern Analysis** - Learning from bridge lift trends

### **Planned Enhancements**
- **Native Mobile Apps** - iOS and Android applications
- **Advanced ML Models** - Deep learning for enhanced accuracy
- **Emergency Overrides** - Manual control for special circumstances  
- **Community Analytics** - User-reported conditions and feedback
- **Regional Integration** - Expand to other Boston-area bridges

---

## 📈 Performance Metrics & Validation

### **Model Performance**
- **Training Data**: 5+ years of historical bridge lifts (2019-2025)
- **Validation Method**: Time-series cross-validation with temporal splits
- **Accuracy**: 75% within ±20 minute window
- **Precision**: 78% for high-confidence predictions
- **Recall**: 71% for all lift events

### **System Performance**
- **API Response Time**: <500ms average
- **Dashboard Load Time**: <3s on mobile
- **System Uptime**: 99% reliability target
- **Concurrent Users**: Designed for typical usage patterns

---

## 🤝 Acknowledgments

- **MassDOT** - Massachusetts Department of Transportation
- **MBTA** - Massachusetts Bay Transportation Authority
- **AECOM** - Engineering consulting and data analysis
- **Community Stakeholders** - Chelsea residents and commuters

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🚨 Important Note

This repository contains a demonstration version using synthetic data. The production implementation was developed under a Non-Disclosure Agreement (NDA) with MassDOT and contains proprietary data and algorithms not disclosed in this public version.

