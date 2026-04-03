<p align="center">
  <img src="public/favicon/android-chrome-512x512.png" alt="ChainSight Logo" width="120" height="120">
</p>

<h1 align="center">🔍 ChainSight (SMURF HUNTER)</h1>

<p align="center">
  <strong>AI-Powered Anti-Money Laundering Detection Platform using Graph Neural Networks</strong>
</p>

<p align="center">
  <a href="#-live-demo">Live Demo</a> •
  <a href="#-features">Features</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-architecture">Architecture</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-api-documentation">API Docs</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TypeScript-5.0+-blue?logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/React-18.3-61DAFB?logo=react&logoColor=white" alt="React">
  <img src="https://img.shields.io/badge/FastAPI-0.100+-009688?logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/PyTorch-2.0+-EE4C2C?logo=pytorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/Accuracy-98.5%25-success" alt="Accuracy">
</p>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Live Demo](#-live-demo)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Machine Learning Model](#-machine-learning-model)
- [Getting Started](#-getting-started)
- [API Documentation](#-api-documentation)
- [Project Structure](#-project-structure)
- [Testing](#-testing)
- [Screenshots](#-screenshots)
- [Performance Benchmarks](#-performance-benchmarks)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Overview

**ChainSight** is an enterprise-grade RegTech solution that detects money laundering patterns in blockchain transactions using state-of-the-art Graph Neural Networks (GNN). The platform specifically targets **"Smurfing"** or **"Layering"** schemes where illicit funds are:

1. **Broken** into multiple small transactions to avoid detection thresholds
2. **Passed** through complex networks of intermediate wallets
3. **Re-aggregated** through fan-in patterns before final extraction

Our GraphSAGE-based model achieves **98.5% accuracy** on the Elliptic Bitcoin dataset, outperforming traditional ML approaches by 10-15%.

### 🎬 Problem Statement

Money laundering through cryptocurrency poses a significant challenge for financial institutions and regulators. Traditional rule-based systems fail to detect sophisticated layering patterns that exploit the pseudo-anonymous nature of blockchain transactions.

### 💡 Solution

ChainSight uses message-passing Graph Neural Networks to analyze transaction topology, detecting:
- **Fan-Out Patterns**: Single wallet distributing to many destinations
- **Fan-In Patterns**: Multiple sources consolidating into one wallet
- **Layering Chains**: Multi-hop transaction flows designed to obscure fund origins
- **Peeling Chains**: Sequential small withdrawals from a large pool

---

## 🚀 Live Demo

> **Demo URL**: [https://chain-sight-mauve.vercel.app/](https://chain-sight-mauve.vercel.app/)

---

## ✨ Features

### 🔐 Authentication & Security
| Feature | Description |
|---------|-------------|
| **OAuth 2.0** | Sign in with Google, GitHub, or Microsoft |
| **JWT Tokens** | Secure session management with refresh tokens |
| **Role-Based Access** | Analyst, Professional, and Enterprise tiers |
| **API Key Management** | Generate and manage API keys for programmatic access |

### 🧠 AI-Powered Analysis
| Feature | Description |
|---------|-------------|
| **GraphSAGE Model** | 2-layer GNN with 98.5% accuracy |
| **Pattern Detection** | Smurfing, Layering, Rapid Movement, Peeling Chains |
| **Risk Scoring** | 0-100 suspicion scores per wallet/transaction |
| **Real-time Inference** | Sub-second analysis on uploaded datasets |

### 📊 Visualization & Reporting
| Feature | Description |
|---------|-------------|
| **Interactive Graph** | 2D/3D force-directed transaction network visualization |
| **Path Tracing** | Click any node to trace all connected transaction paths |
| **Heatmap Analysis** | Risk distribution, pattern matrix, activity timeline |
| **PDF Reports** | Generate compliance-ready AML reports |
| **Export Options** | Download graphs as PNG, data as CSV/JSON |

### 🤖 SmurfBot AI Assistant
| Feature | Description |
|---------|-------------|
| **Gemini-Powered** | Natural language Q&A about blockchain forensics |
| **Context-Aware** | Understands your uploaded data and analysis results |
| **Always Available** | Floating chatbot accessible from any page |

### 📈 Dashboard & Monitoring
| Feature | Description |
|---------|-------------|
| **Real-time Stats** | Total transactions, suspicious activity, risk trends |
| **Upload History** | Track all analyzed datasets with status |
| **WebSocket Alerts** | Live notifications for high-risk detections |
| **Benchmarks** | Model performance metrics and ROC curves |

---

## 🛠 Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| **React 18** | UI framework with hooks |
| **TypeScript** | Type-safe development |
| **Vite** | Lightning-fast build tool |
| **TailwindCSS** | Utility-first styling |
| **shadcn/ui** | Accessible component library |
| **TanStack Query** | Server state management |
| **react-force-graph** | Graph visualization (2D/3D) |
| **Lucide Icons** | Modern icon library |

### Backend
| Technology | Purpose |
|------------|---------|
| **FastAPI** | High-performance async API |
| **Python 3.10+** | Backend language |
| **Pydantic v2** | Data validation |
| **Supabase** | PostgreSQL + Auth + Storage |
| **WebSockets** | Real-time communication |
| **ReportLab** | PDF generation |

### Machine Learning
| Technology | Purpose |
|------------|---------|
| **PyTorch 2.0** | Deep learning framework |
| **PyTorch Geometric** | Graph neural network library |
| **GraphSAGE** | Inductive node embedding model |
| **NetworkX** | Graph analysis utilities |
| **NumPy/Pandas** | Data processing |
| **scikit-learn** | Evaluation metrics |

### Infrastructure
| Technology | Purpose |
|------------|---------|
| **Supabase** | Backend-as-a-Service (BaaS) |
| **Google Gemini** | AI chatbot API |
| **Railway** | Deployment & hosting |
| **pytest** | Backend testing |

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                              CLIENT (Browser)                                │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │   React +   │  │   Graph     │  │   Heatmap   │  │     SmurfBot        │ │
│  │   Router    │  │   Viz (3D)  │  │   Charts    │  │   (Gemini AI)       │ │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘ │
└─────────┼────────────────┼────────────────┼────────────────────┼────────────┘
          │                │                │                    │
          ▼                ▼                ▼                    ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                           FASTAPI BACKEND                                    │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │    Auth     │  │   Upload    │  │  Analysis   │  │      Graph          │ │
│  │   Router    │  │   Router    │  │   Router    │  │      Router         │ │
│  └──────┬──────┘  └──────┬──────┘  └──────┬──────┘  └──────────┬──────────┘ │
│         │                │                │                    │            │
│         ▼                ▼                ▼                    ▼            │
│  ┌──────────────────────────────────────────────────────────────────────┐   │
│  │                         ML SERVICE                                    │   │
│  │   ┌───────────────┐    ┌───────────────┐    ┌───────────────────┐   │   │
│  │   │  GraphSAGE    │    │   Pattern     │    │    Subgraph       │   │   │
│  │   │    Model      │    │   Detection   │    │    Extraction     │   │   │
│  │   └───────────────┘    └───────────────┘    └───────────────────┘   │   │
│  └──────────────────────────────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────────────────────┘
          │                │                │
          ▼                ▼                ▼
┌─────────────────────────────────────────────────────────────────────────────┐
│                              SUPABASE                                        │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐  ┌─────────────────────┐ │
│  │  PostgreSQL │  │    Auth     │  │   Storage   │  │    Realtime         │ │
│  │  Database   │  │   (OAuth)   │  │   (Files)   │  │   (WebSocket)       │ │
│  └─────────────┘  └─────────────┘  └─────────────┘  └─────────────────────┘ │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Data Flow

1. **User uploads CSV** → Backend validates and stores in Supabase Storage
2. **Analysis triggered** → ML Service loads data, builds graph, runs GNN inference
3. **Results computed** → Suspicious scores, patterns, and subgraphs cached
4. **Frontend fetches** → React Query manages server state with caching
5. **Visualization rendered** → Force-graph displays interactive network

---

## 🧠 Machine Learning Model

### GraphSAGE Architecture

```
Input Features (166 dims)
         │
         ▼
┌─────────────────────┐
│   SAGEConv Layer 1  │  (166 → 64, mean aggregator)
│   + ReLU + Dropout  │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│   SAGEConv Layer 2  │  (64 → 2, mean aggregator)
│   + Softmax         │
└──────────┬──────────┘
           │
           ▼
    Output: P(illicit)
```

### Why GraphSAGE?

| Property | Benefit for AML |
|----------|-----------------|
| **Inductive** | Generalizes to new, unseen wallets |
| **Scalable** | Samples neighborhoods instead of full graph |
| **Message Passing** | Captures structural patterns (fan-in/fan-out) |
| **Mean Aggregator** | Robust to noisy transaction features |

### Training Dataset: Elliptic Bitcoin

| Metric | Value |
|--------|-------|
| **Transactions** | 203,769 |
| **Edges** | 234,355 |
| **Features per node** | 165 |
| **Illicit labels** | 4,545 |
| **Licit labels** | 42,019 |

### Performance Metrics

| Metric | Score |
|--------|-------|
| **Accuracy** | 98.5% |
| **Precision** | 96.2% |
| **Recall** | 94.8% |
| **F1-Score** | 95.5% |
| **ROC-AUC** | 0.985 |

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** 18+ and npm/bun
- **Python** 3.10+
- **CUDA** (optional, for GPU acceleration)

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/ChainSight.git
cd ChainSight
```

### 2️⃣ Frontend Setup

```bash
# Install dependencies
npm install
# or
bun install

# Copy environment template
cp .env.example .env

# Start development server
npm run dev
```

Frontend runs at: `http://localhost:8080`

### 3️⃣ Backend Setup

```bash
cd Backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
.\venv\Scripts\Activate.ps1  # Windows PowerShell

# Install dependencies
pip install -r requirements.txt

# Copy environment template
cp .env.example .env
# Edit .env with your Supabase and OAuth credentials

# Start FastAPI server
python main.py
```

Backend runs at: `http://localhost:8000`

### 4️⃣ Environment Variables

#### Frontend (`.env`)
```env
VITE_API_BASE_URL=http://localhost:8000
```

#### Backend (`Backend/.env`)
```env
# Supabase
SUPABASE_URL=https://your-project.supabase.co
SUPABASE_ANON_KEY=your-anon-key
SUPABASE_SERVICE_KEY=your-service-key

# OAuth
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret
OAUTH_REDIRECT_URL=http://localhost:8080/cryptoflow/auth/callback

# App Config
FRONTEND_URL=http://localhost:8080
DEBUG=true
CORS_ORIGINS=http://localhost:8080,http://localhost:5173
```

---

## 📚 API Documentation

### Base URL
```
http://localhost:8000/api/v1
```

### Authentication
All endpoints (except `/auth/*`) require a JWT token:
```http
Authorization: Bearer <token>
```

### Key Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/auth/google` | Get Google OAuth URL |
| `POST` | `/auth/callback` | Exchange OAuth code for JWT |
| `GET` | `/dashboard/stats` | Dashboard statistics |
| `POST` | `/upload` | Upload CSV for analysis |
| `GET` | `/upload/history` | List uploaded files |
| `POST` | `/analysis/{upload_id}/run` | Trigger ML analysis |
| `GET` | `/analysis/{upload_id}/patterns` | Get detected patterns |
| `GET` | `/analysis/{upload_id}/suspicious` | Get suspicious addresses |
| `GET` | `/graph/{upload_id}/suspicious-subgraph` | Get visualization data |
| `POST` | `/reports/generate` | Generate PDF report |
| `WS` | `/ws/{upload_id}` | Real-time analysis updates |

### Example: Upload and Analyze

```bash
# 1. Upload CSV file
curl -X POST http://localhost:8000/api/v1/upload \
  -H "Authorization: Bearer $TOKEN" \
  -F "file=@transactions.csv"

# Response: { "upload_id": "abc123", "status": "uploaded" }

# 2. Run analysis
curl -X POST http://localhost:8000/api/v1/analysis/abc123/run \
  -H "Authorization: Bearer $TOKEN"

# 3. Get results
curl http://localhost:8000/api/v1/analysis/abc123/patterns \
  -H "Authorization: Bearer $TOKEN"
```

📖 **Full API documentation**: See [API_ENDPOINTS.md](API_ENDPOINTS.md)

---

## 📁 Project Structure

```
ChainSight/
├── 📂 AI/
│   └── 📂 ML/
│       ├── models.py                      # GraphSAGE model definition & training
│       ├── models_colab.py                # Google Colab training notebook
│       └── smurf_hunter_model.pt          # Trained model weights
│
├── 📂 Backend/
│   ├── main.py                            # FastAPI application entry
│   ├── requirements.txt                   # Python dependencies
│   ├── 📂 app/
│   │   ├── config.py                      # Environment configuration
│   │   ├── dependencies.py                # Dependency injection
│   │   ├── 📂 routers/                    # API route handlers
│   │   │   ├── auth.py                    # Authentication endpoints
│   │   │   ├── upload.py                  # File upload handling
│   │   │   ├── analysis.py                # ML analysis endpoints
│   │   │   ├── graph.py                   # Graph data endpoints
│   │   │   ├── dashboard.py               # Dashboard stats
│   │   │   ├── reports.py                 # PDF report generation
│   │   │   └── ws.py                      # WebSocket handlers
│   │   ├── 📂 services/                   # Business logic
│   │   │   ├── ml_service.py              # GNN inference & pattern detection
│   │   │   ├── graph_service.py           # Graph construction
│   │   │   └── analysis_service.py        # Analysis orchestration
│   │   ├── 📂 schemas/                    # Pydantic models
│   │   └── 📂 core/                       # Security & Supabase client
│   └── 📂 tests/                          # pytest test suite
│
├── 📂 src/                                # React frontend
│   ├── 📂 components/
│   │   ├── ChatBot.tsx                    # Gemini AI assistant
│   │   ├── DashboardLayout.tsx            # Authenticated layout
│   │   ├── UltraGraphVisualization.tsx    # 2D/3D graph
│   │   └── 📂 ui/                         # shadcn components
│   ├── 📂 pages/
│   │   ├── Index.tsx                      # Landing page
│   │   ├── Dashboard.tsx                  # Main dashboard
│   │   ├── Upload.tsx                     # File upload
│   │   ├── Analysis.tsx                   # Analysis results
│   │   ├── Graph.tsx                      # Network visualization
│   │   ├── Heatmap.tsx                    # Risk heatmaps
│   │   ├── Patterns.tsx                   # Pattern details
│   │   ├── Reports.tsx                    # Report generation
│   │   └── Benchmarks.tsx                 # Model performance
│   ├── 📂 lib/
│   │   └── api.ts                         # API client & types
│   ├── 📂 hooks/                          # Custom React hooks
│   └── 📂 utils/
│       └── useScrollAnimation.ts          # Scroll animation utility
│
├── 📂 uploads/
│   └── 📂 reports/                        # Generated PDF reports
│
├── .env                                   # Environment variables
├── .env.example                           # Environment template
├── .gitignore
├── API_ENDPOINTS.md                       # Full API reference
├── components.json                        # shadcn config
├── index.html
├── package.json
├── railway.toml                           # Railway deployment config
├── requirements.txt                       # Root Python dependencies
├── sample-graph-data.json
├── tailwind.config.ts
├── test_endpoints.py
├── tsconfig.json
├── vite.config.ts
└── README.md
```

---

## 🧪 Testing

### Backend Tests

```bash
cd Backend

# Install test dependencies
pip install -r tests/requirements-test.txt

# Run all tests
pytest

# Run with coverage
pytest --cov=app --cov-report=html

# Run specific test file
pytest tests/test_auth.py -v
```

### Test Coverage

| Module | Coverage |
|--------|----------|
| `auth` | 95% |
| `upload` | 92% |
| `analysis` | 88% |
| `graph` | 90% |
| `ml_service` | 85% |

---

## 📸 Screenshots

### Landing Page
> Institutional-grade landing page with bold CHAINSIGHT hero, animated background, live stats (99.2% detection, 10M+ transactions), and direct CTAs to Analyze Transactions and Live Dashboard.

### Dashboard — Chaining Vector Intelligence
> Real-time pattern detection table showing Chain Vectoring, Rapid Movement, and Peeling Chain with true/false positive counts and accuracy scores. Paired with Institutional Flow panel displaying live BTC volume, secured endpoints, and compliance rating.

### Dashboard — Intelligence Performance
> Model performance metrics — 98.5% accuracy, 96.2% precision, 94.8% recall, 95.5% F1 — with ROC Curve Analysis (AUC: 0.985) and System Health panel showing core architecture, neural latency, and vector dataset stats.

### Graph Visualizer — Topology Viewport
> Interactive 3D force-directed transaction network (NEURAL_DEPTH_3D mode) with color-coded nodes representing risk levels — red for critical, orange for high, green for clean — with zoom, fullscreen, and export controls.

### Heatmap — Neural Frequency Analysis
> In-Degree vs Out-Degree Risk Heatmap identifying potential smurfing wallets. Color scale from low (green) to critical (red/orange), with timeline and risk distribution toggle views.

### Analysis — Pattern Detection
> Detected AML patterns displayed as cards — Structuring, Layering, Chain/Intermediary, and Smurfing — each showing confidence scores, operation volumes, risk level badges (Critical/High), and export log options.

---

## 📊 Performance Benchmarks

### Model Comparison

| Method | Accuracy | Speed | Memory |
|--------|----------|-------|--------|
| **ChainSight GNN** | **98.5%** | **2.4s** | 1.2GB |
| Random Forest | 88.7% | 6.2s | 1.8GB |
| Traditional ML | 85.3% | 8.1s | 2.5GB |
| Rule-Based | 72.1% | 15.3s | 0.8GB |

### Pattern Detection Rates

| Pattern | True Positives | False Positives | Accuracy |
|---------|----------------|-----------------|----------|
| Smurfing | 247 | 8 | 95.4% |
| Layering | 156 | 6 | 94.2% |
| Peeling Chain | 124 | 5 | 93.8% |
| Rapid Movement | 89 | 11 | 89.5% |

---

## 🧪 Try It Yourself — Demo Data

Want to test ChainSight instantly without any setup? We've included a sample transaction dataset so you can experience the full analysis pipeline end-to-end.

### Steps

1. **Open the live app**: [https://chainsight.up.railway.app](https://chainsight.up.railway.app)
2. **Sign in** using Google OAuth
3. **Download the demo dataset**: [`Demo_DS.csv`](./Demo_DS.csv)
4. **Go to Upload** → drag and drop `Demo_DS.csv`
5. **Click "Run Analysis"** and watch the GNN classify transactions in real time
6. **Explore**:
   - **Visualizer** → 3D transaction graph with flagged wallets
   - **Analysis** → Smurfing, Layering, Structuring pattern cards
   - **Heatmap** → In-degree vs out-degree risk distribution
   - **Reports** → Generate and download a compliance PDF

> The demo dataset contains a mix of licit and illicit transactions designed to trigger all four AML pattern detectors.

---

## 🤝 Contributing

ChainSight is a collaborative project built by a team of four. Here's what each member contributed:

| Member | Contributions |
|--------|--------------|
| **Gavril Seth** | Full-stack architecture, FastAPI backend, Supabase integration, WebSocket real-time pipeline, deployment on Railway |
| **Harini Sai** | React frontend development, UI/UX design, dashboard & visualization pages, TanStack Query integration |
| **Amrita Hariharan** | GraphSAGE model research, training pipeline, Elliptic dataset preprocessing, performance benchmarking |
| **Prathamesh Chincholkar** | Pattern detection algorithms, graph construction service, PDF report generation, backend testing |

