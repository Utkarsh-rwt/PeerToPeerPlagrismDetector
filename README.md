# Peer-to-Peer Plagiarism Detector

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-3.x-000000?logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/docs/Web/JavaScript)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?logo=scikitlearn&logoColor=white)](https://scikit-learn.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-013243?logo=numpy&logoColor=white)](https://numpy.org/)
[![PyPDF2](https://img.shields.io/badge/PyPDF2-PDF%20Parsing-CC3333)](https://pypi.org/project/PyPDF2/)
[![Google OAuth](https://img.shields.io/badge/Google-OAuth%202.0-4285F4?logo=google&logoColor=white)](https://developers.google.com/identity/protocols/oauth2)
[![Gunicorn](https://img.shields.io/badge/Gunicorn-WSGI%20Server-499848)](https://gunicorn.org/)
[![Render](https://img.shields.io/badge/Render-Deployed-46E3B7?logo=render&logoColor=black)](https://render.com/)

A Flask-based web application that detects peer-to-peer plagiarism between student submissions using NLP techniques.

The system compares uploaded content and computes plagiarism scores with **TF-IDF vectorization** and **cosine similarity**, helping educators identify suspiciously similar submissions efficiently.

---

## Table of Contents

- [Live Demo](#live-demo)
- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Deployment on Render](#deployment-on-render)
- [Google Classroom Integration (Optional)](#google-classroom-integration-optional)
- [Working Principle](#working-principle)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

---

## Live Demo

Application Link:  
https://peertopeerplagrismdetector.onrender.com

## Project Overview

This project focuses on **peer-to-peer similarity detection** in classroom submissions.

Unlike internet-wide plagiarism tools, it is designed to detect copying between students in the same course workflow. It supports PDF text extraction and can be extended with Google Classroom for automated assignment retrieval.

## Features

- Upload and compare multiple documents
- Automatic text extraction from PDF files
- Text cleaning and preprocessing pipeline
- TF-IDF based feature extraction
- Cosine similarity score calculation
- Plagiarism percentage display
- Clean, responsive teacher dashboard
- Optional Google Classroom integration
- Cloud deployment support via Render

## Tech Stack

### Backend
- Python
- Flask

### Frontend
- HTML
- CSS
- JavaScript

### Data Processing & NLP
- scikit-learn (TF-IDF, cosine similarity)
- NumPy
- PyPDF2

### Integrations
- Google OAuth 2.0
- Google Classroom API
- Google Drive API

### Deployment
- Gunicorn
- Render

## Project Structure

```text
PeerToPeerPlagrismDetector/
├── app.py
├── requirements.txt
├── Procfile
├── templates/
├── static/
└── README.md
```

## Installation

### Prerequisites
- Python 3.x
- pip

### 1) Clone the repository

```bash
git clone https://github.com/Utkarsh-rwt/PeerToPeerPlagrismDetector.git
cd PeerToPeerPlagrismDetector
```

### 2) Create and activate a virtual environment

```bash
python -m venv venv
```

**Windows**
```bash
venv\Scripts\activate
```

**macOS/Linux**
```bash
source venv/bin/activate
```

### 3) Install dependencies

```bash
pip install -r requirements.txt
```

### 4) Run the application

```bash
python app.py
```

Open in browser:

```text
http://127.0.0.1:5000
```

## Usage

1. Open the app home page.
2. Sign in through the Google login flow (optional for Classroom-based workflow).
3. Select course and assignment (when using Classroom integration).
4. Fetch submissions and run similarity analysis.
5. Review generated plagiarism percentages and matched student pairs.

## Deployment on Render

### Step 1 — Prepare required files

Ensure these files exist in the repository root:

- `requirements.txt`
- `Procfile` with:

```text
web: gunicorn app:app
```

### Step 2 — Push the repository

```bash
git add .
git commit -m "deploy app"
git push
```

### Step 3 — Deploy on Render

1. Go to Render and sign in with GitHub.
2. Create a **New Web Service**.
3. Select this repository.
4. Set build command:

```bash
pip install -r requirements.txt
```

5. Set start command:

```bash
gunicorn app:app
```

6. Click **Deploy**.

## Google Classroom Integration (Optional)

For OAuth integration, update your redirect URI in Google Cloud Console:

```text
https://your-app-name.onrender.com/oauth2callback
```

Also ensure `client_secret.json` is configured correctly for your Google Cloud project.

## Working Principle

The plagiarism detection workflow:

1. Extract text from uploaded documents
2. Clean and normalize text
3. Convert text into TF-IDF vectors
4. Compute cosine similarity
5. Generate plagiarism percentage scores

Similarity formula:

```text
cos(θ) = (A · B) / (||A|| ||B||)
```

## Future Improvements

- AI-based semantic similarity detection
- Teacher analytics dashboard
- Report export system
- Classroom-wide live sync
- Historical plagiarism database
- Student submission insights

## Contributing

Pull requests are welcome.

For major changes, please open an issue first to discuss your proposed improvements.

## License

This project is intended for educational and academic use.

A dedicated open-source license file is not currently included in the repository.
