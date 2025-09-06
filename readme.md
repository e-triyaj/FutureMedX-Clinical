# FutureMedX Clinical Decision Support System

![FutureMedX Logo](docs/images/logo.png)

## 🏥 Overview

FutureMedX Clinical is an advanced AI-powered clinical decision support system that provides:

- **Emergency Triage System**: AI-driven ESI (Emergency Severity Index) scoring
- **Risk Assessment**: Cardiovascular and multi-system risk calculations
- **Signal Analysis**: Real-time analysis of ECG, EEG, and EMG signals
- **Clinical Decision Support**: Evidence-based recommendations and alerts

## 🚀 Features

### Emergency Triage
- Automated ESI scoring (Level 1-5)
- Vital signs monitoring and alerts
- Symptom-based priority assessment
- Wait time predictions

### Risk Assessment
- Framingham Risk Score
- SCORE2 European risk assessment
- Diabetes risk calculation
- Custom risk modeling

### Signal Analysis
- **ECG Analysis**
  - Arrhythmia detection
  - MI (Myocardial Infarction) detection
  - QT interval analysis
  - Heart rate variability

- **EEG Analysis**
  - Epilepsy detection
  - Sleep stage classification
  - Cognitive assessment
  - Alzheimer's early detection

- **EMG Analysis**
  - ALS detection
  - Neuropathy assessment
  - Muscle fatigue analysis
  - Movement disorder detection

## 🛠️ Tech Stack

### Frontend
- HTML5, CSS3, JavaScript (ES6+)
- Chart.js for data visualization
- Bootstrap for responsive design

### Backend
- Node.js with Express.js
- PostgreSQL for primary database
- MongoDB for session management
- Redis for caching

### AI/ML Engine
- Python 3.9+
- TensorFlow 2.x for deep learning
- scikit-learn for traditional ML
- NumPy, Pandas for data processing
- FastAPI for AI service endpoints

## 📋 Prerequisites

- Docker & Docker Compose
- Node.js 16+ (for local development)
- Python 3.9+ (for AI engine development)
- 8GB RAM minimum (16GB recommended)
- 10GB free disk space

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/futuremedx/clinical.git
   cd futuremedx-clinical
   ```

2. **Configure environment**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

3. **Start with Docker Compose**
   ```bash
   docker-compose up -d
   ```

4. **Access the application**
   - Frontend: http://localhost:3000
   - API: http://localhost:5000
   - AI Engine: http://localhost:8000
   - PgAdmin: http://localhost:5050 (dev profile)

## 🔧 Development Setup

### Backend Development
```bash
cd backend
npm install
npm run dev
```

### AI Engine Development
```bash
cd ai-engine
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

### Frontend Development
```bash
cd frontend
# Serve with any static server
python -m http.server 3000
```

## 📊 API Documentation

### Triage Endpoints
```bash
POST /api/triage/calculate
GET /api/triage/history/:patientId
POST /api/triage/vitals
```

### Risk Assessment Endpoints
```bash
POST /api/risk/cardiovascular
POST /api/risk/diabetes
GET /api/risk/report/:patientId
```

### Signal Analysis Endpoints
```bash
POST /api/signals/ecg/analyze
POST /api/signals/eeg/analyze
POST /api/signals/emg/analyze
GET /api/signals/results/:analysisId
```

Full API documentation available at `/api/docs` when running the backend.

## 🧪 Testing

### Run all tests
```bash
npm test
```

### Backend tests
```bash
cd backend && npm test
```

### AI Engine tests
```bash
cd ai-engine && pytest
```

## 📈 Monitoring

### Enable monitoring stack
```bash
docker-compose --profile monitoring up -d
```

- Prometheus: http://localhost:9090
- Grafana: http://localhost:3001 (admin/admin)

## 🔐 Security

- All patient data is encrypted at rest
- JWT-based authentication
- Role-based access control (RBAC)
- HIPAA compliance features
- Audit logging for all clinical actions

## 📝 Clinical Validation

This system has been validated against:
- ESI Implementation Handbook v5
- Framingham Risk Score 2008
- SCORE2 2021 Guidelines
- ACC/AHA Clinical Guidelines

## 🤝 Contributing

Please read [CONTRIBUTING.md](docs/CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Medical Disclaimer

This software is intended for use as a clinical decision support tool only. It should not replace professional medical judgment. Always consult with qualified healthcare professionals for medical decisions.

## 📞 Support

- Documentation: [docs.futuremedx.com](https://docs.futuremedx.com)
- Issues: [GitHub Issues](https://github.com/futuremedx/clinical/issues)
- Email: support@futuremedx.com

## 🙏 Acknowledgments

- ESI Triage Research Group
- Open-source medical AI community
- All contributors and clinical validators

---

**FutureMedX** - Advancing Healthcare with AI

*Last updated: January 2025*