# Jobify: AI-Powered Job Search Module

This repository contains the **Resume-to-Job Matching** module developed for **Jobify**, a job search platform. This feature automates the discovery of job opportunities by extracting technical skills directly from a user's resume and matching them with live vacancies.

## 📌 Project Context
Jobify is a comprehensive job search platform. This specific module was developed to handle the **Search and Skill Extraction** logic, moving away from traditional manual keyword searches toward an automated, document-driven approach.

## 🚀 Key Features
- **Resume Parsing:** Automated text extraction from `.pdf` and `.docx` files.
- **Intelligent Skill Extraction:** Scans resume content against industry-standard keywords (Python, SQL, JavaScript, Machine Learning, etc.).
- **Real-time API Integration:** Connects to the **Adzuna API** to fetch live job listings including titles, companies, and locations.
- **Dynamic UI:** A seamless frontend that displays extracted skills and matching jobs without requiring a page reload.

## 🛠️ Technical Stack
- **Backend:** FastAPI (Python)
- **Frontend:** Vanilla JavaScript, HTML5, CSS3
- **File Processing:** `PyPDF2` (PDF), `python-docx` (Word)
- **Data Fetching:** `requests` (API communication)

## 📂 System Architecture
The module follows a four-step process:
1. **Ingestion:** User uploads a resume and specifies a location preference.
2. **Extraction:** The system identifies the file type and parses it into raw text.
3. **Skill Mapping:** The backend filters the text for predefined technical keywords.
4. **Matching:** The system queries the Adzuna API for each skill found and returns a consolidated list of opportunities.

## 🔧 Installation & Setup

### 1. Prerequisites
Ensure you have Python 3.8+ installed.

3. API Configuration
Update the following variables in backend.py with your Adzuna credentials:

APP_ID

APP_KEY

4. Running the Application
Start the FastAPI server:

Bash
uvicorn backend:app --reload
Then, simply open the index.html file in your preferred web browser.

🌟 Future Enhancements
Advanced NLP: Integrating SpaCy or NLTK for more sophisticated Named Entity Recognition (NER).

Match Scoring: Implementing a ranking algorithm to show the most relevant jobs first based on skill density.

Performance: Implementing asynchronous API calls using httpx to reduce wait times during multi-skill searches.

### 2. Install Dependencies
```bash
pip install fastapi uvicorn requests PyPDF2 python-docx
