Peer-to-Peer Plagiarism Detector

A Python-based web application built using Flask and Natural Language Processing (NLP) techniques to detect similarity between student submissions.

The system compares uploaded documents and computes plagiarism scores using TF-IDF vectorization and cosine similarity, enabling efficient peer-to-peer submission analysis for academic environments.

It also supports PDF text extraction and can be extended with Google Classroom integration for automated submission retrieval.

🌐 Live Demo

Application Link:
https://peertopeerplagrismdetector.onrender.com

🚀 Features
Upload and compare multiple documents
Automatic text extraction from PDF files
Text cleaning and preprocessing pipeline
TF-IDF based feature extraction
Cosine similarity score calculation
Plagiarism percentage display
Clean and responsive web dashboard
Optional Google Classroom integration
Cloud deployment support via Render
🛠 Tech Stack
Frontend
HTML
CSS
JavaScript
Backend
Python
Flask
Libraries
scikit-learn
NumPy
PDF processing tools
Deployment
Render
Gunicorn
📂 Project Structure
peer-plagiarism/
│
├── app.py
├── requirements.txt
├── Procfile
├── templates/
├── static/
└── README.md
⚙ Installation (Local Setup)
1. Clone the Repository
git clone https://github.com/your-username/peer-plagiarism.git
cd peer-plagiarism
2. Create Virtual Environment
python -m venv venv

Activate environment:

Windows

venv\Scripts\activate

Mac/Linux

source venv/bin/activate
3. Install Dependencies
pip install -r requirements.txt
4. Run the Application
python app.py

Open in browser:

http://127.0.0.1:5000
🌐 Deployment (Render)
Step 1 — Prepare Required Files

Generate dependencies file:

pip freeze > requirements.txt

Create Procfile:

web: gunicorn app:app
Step 2 — Push to GitHub
git init
git add .
git commit -m "deploy app"
git push
Step 3 — Deploy on Render
Go to Render
Login with GitHub
Create New Web Service
Select repository

Build Command

pip install -r requirements.txt

Start Command

gunicorn app:app

Click Deploy

🔐 Google Classroom Integration (Optional)

For OAuth integration, update the redirect URI in Google Cloud Console:

https://your-app-name.onrender.com/callback
📊 Working Principle

The plagiarism detection workflow follows these steps:

Extract text from uploaded documents
Perform text cleaning and normalization
Convert text into TF-IDF vectors
Compute cosine similarity
Generate plagiarism percentage scores
Similarity Formula

cos
⁡
(
𝜃
)
=
𝐴
⋅
𝐵
∥
𝐴
∥
∥
𝐵
∥
cos(θ)=
∥A∥∥B∥
A⋅B
	​


🧠 Future Improvements
AI-based semantic similarity detection
Teacher analytics dashboard
Report export system
Classroom-wide live sync
Historical plagiarism database
Student submission insights
🤝 Contributing

Pull requests are welcome.

For major changes, please open an issue first to discuss the proposed improvements.

📜 License

This project is intended for educational and academic use.

Feel free to modify and extend it.

✨ Author

Developed as a peer-to-peer plagiarism detection system to support academic integrity and automated submission analysis.