# 🏥 Health Insurance Smart Query Processor

<div align="center">

![Health Insurance Banner](https://img.shields.io/badge/Accuracy-94%25-success?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

**An AI-powered application that intelligently processes health insurance documents and validates claims against policy clauses**

</div>

---

## 📋 Overview

The **Health Insurance Smart Query Processor** is an intelligent document analysis system that revolutionizes how users interact with their health insurance policies. By leveraging advanced NLP models, the application automatically parses insurance documents, extracts key clauses, and validates user queries against policy terms in real-time.

### 🎯 Problem Statement

Health insurance policies are complex, filled with legal jargon, and often contain hidden clauses that users overlook. This application bridges the gap between policy complexity and user understanding.

### 💡 Solution

Our AI-powered system:
- 📄 **Parses** insurance documents automatically
- 🔍 **Analyzes** user queries using DistilBERT
- ✅ **Validates** claims against policy clauses
- 💰 **Displays** approved amounts or rejection reasons
- 📊 **Returns** structured JSON responses

---

## ✨ Key Features

### 🤖 Intelligent Query Processing
Uses DistilBERT transformer model to understand context and match user queries with relevant policy clauses with **94% accuracy**.

### 📑 Document Parsing
Automatically extracts and structures information from insurance policy documents in various formats.

### 🔐 Clause Matching Engine
Compares user claims against policy terms and identifies matching or conflicting clauses.

### 💬 User-Friendly Interface
Intuitive web interface built with HTML, CSS, and JavaScript for seamless interaction.

### 🎓 Educational Tool
Helps users:
- 🏆 **Choose the best insurance plan** based on their needs
- 🔍 **Unveil hidden clauses** that might affect coverage
- 📚 **Understand complex terms** without prior insurance knowledge

### 📤 JSON Output
Structured responses including:
```json
{
  "status": "approved",
  "claimed_amount": 50000,
  "matching_clause": "Clause 3.2.1: Hospitalization coverage up to ₹5,00,000",
  "confidence_score": 0.94
}
```

---

## 📊 Model Performance

<div align="center">

### Accuracy Metrics

| Metric | Score |
|--------|-------|
| Overall Accuracy | **94%** |
| Precision | 92% |
| Recall | 91% |
| F1-Score | 91.5% |

```
Accuracy Breakdown
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Approved Claims  ████████████████████░  94%
Rejected Claims  ███████████████████░░  93%
Clause Matching  ████████████████████░  95%
```

</div>

---

## 🏗️ Implementation

### Architecture Overview

```
┌─────────────────┐
│   User Input    │
│   (Query +      │
│   Documents)    │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│   FastAPI       │
│   Backend       │
└────────┬────────┘
         │
         ▼
┌─────────────────┐      ┌──────────────────┐
│  Document       │──────▶│   DistilBERT     │
│  Preprocessing  │      │   Model          │
│  (NLTK, spaCy)  │      │   (Transformers) │
└────────┬────────┘      └────────┬─────────┘
         │                        │
         │                        │
         ▼                        ▼
┌─────────────────────────────────────┐
│      Clause Matching Engine         │
│      (PyTorch + Custom Logic)       │
└────────────────┬────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────┐
│         JSON Response               │
│   (Approval/Rejection + Details)    │
└─────────────────────────────────────┘
```

### Core Components

1. **Document Parser**: Extracts text and structures from uploaded insurance documents
2. **NLP Pipeline**: Processes text using spaCy and NLTK for tokenization and entity recognition
3. **DistilBERT Model**: Performs semantic similarity matching between queries and clauses
4. **Validation Engine**: Applies business logic to approve or reject claims
5. **API Layer**: FastAPI endpoints for seamless frontend-backend communication

---

## 🛠️ Tech Stack

<div align="center">

### Backend
<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Uvicorn-499848?style=for-the-badge&logo=gunicorn&logoColor=white" alt="Uvicorn"/>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
</p>

### Machine Learning & NLP
<p>
  <img src="https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch"/>
  <img src="https://img.shields.io/badge/spaCy-09A3D5?style=for-the-badge&logo=spacy&logoColor=white" alt="spaCy"/>
  <img src="https://img.shields.io/badge/NLTK-154f3c?style=for-the-badge&logo=python&logoColor=white" alt="NLTK"/>
</p>

### Frontend
<p>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"/>
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
</p>

### DevOps & Deployment
<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/Fly.io-7B3FF2?style=for-the-badge&logo=fly.io&logoColor=white" alt="Fly.io"/>
</p>

</div>

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8 or higher
- Docker (optional, for containerized deployment)
- Git

### 📥 Installation

1. **Clone the repository**
```bash
git clone https://github.com/Arsh06-github/Health-Insurance.git
cd Health-Insurance
```

2. **Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Download spaCy language model**
```bash
python -m spacy download en_core_web_sm
```

5. **Set up environment variables**
```bash
cp .env.example .env
# Edit .env with your configuration
```

### ▶️ Running the Application

#### Local Development
```bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

The application will be available at `http://localhost:8000`

#### Using Docker
```bash
docker build -t health-insurance-app .
docker run -p 8000:8000 health-insurance-app
```

### 🧪 Running Tests
```bash
pytest tests/
```

---

## 📖 Usage

1. **Upload Insurance Document**: Navigate to the web interface and upload your insurance policy document (PDF, DOCX, or TXT)

2. **Submit Query**: Enter your claim query in natural language
   - Example: "I was hospitalized for 3 days due to dengue. Can I claim ₹45,000?"

3. **Get Results**: The system will analyze your query and return:
   - ✅ Approval status
   - 💰 Claimed amount (if approved)
   - 📜 Relevant policy clause
   - ❌ Rejection reason (if denied)

### API Endpoints

```bash
POST /api/upload
# Upload insurance document

POST /api/query
# Submit claim query

GET /api/health
# Check API health status
```

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### MIT License

```
MIT License

Copyright (c) 2025 [Arsh Maheshwari]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👥 Authors

Project Link: [https://github.com/Arsh06-github/Health-Insurance](https://github.com/Arsh06-github/Health-Insurance)

---

## 🙏 Acknowledgments

- Hugging Face for the DistilBERT model
- FastAPI community for excellent documentation
- Open source NLP libraries (spaCy, NLTK)

---

## 📧 Contact & Support

For questions, issues, or suggestions:
- 📫 Open an issue on GitHub
- 💬 Start a discussion in the Discussions tab
- 📧 Email: arsh.johari55000@gmail.com

---

<div align="center">

### ⭐ Star this repo if you find it helpful!

**Made with ❤️ and 🤖**

![GitHub stars](https://img.shields.io/github/stars/Arsh06-github/Health-Insurance?style=social)
![GitHub forks](https://img.shields.io/github/forks/Arsh06-github/Health-Insurance?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/Arsh06-github/Health-Insurance?style=social)

</div>
