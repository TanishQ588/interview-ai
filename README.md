# Interview AI 🎯

**An AI-powered interview preparation platform that helps candidates prepare for job interviews through personalized questions, job-role matching, skill-gap analysis, and preparation roadmaps.**

## 📌 Overview

Interview AI is a full-stack web application that generates personalized interview preparation reports based on a candidate's resume or self-description and the target job description.

The application uses Generative AI to analyze the provided information and create relevant technical questions, behavioral questions, a job-match score, identified skill gaps, and a structured preparation roadmap.

## ✨ Features

- **AI-Powered Interview Questions:** Generate technical and behavioral interview questions tailored to the target role.
- **Job Match Score:** Get an AI-generated estimate of how well your profile matches the target job description.
- **Skill Gap Analysis:** Identify skills that may need improvement for the desired role.
- **Personalized Preparation Roadmap:** Receive a structured plan to guide interview preparation.
- **Resume Upload:** Upload a resume in PDF format for personalized analysis.
- **Self-Description Support:** Generate a report using a short description of your experience and skills when a resume is unavailable.
- **Interview Reports:** View generated reports and access recent interview plans.
- **Resume PDF Generation:** Generate and download a resume PDF through the application.

## 🛠️ Tech Stack

### Frontend
- React.js
- Vite
- JavaScript
- SCSS

### Backend
- Node.js
- Express.js
- REST APIs
- JWT-based authentication
- Multer for file uploads

### Database
- MongoDB
- MongoDB Atlas

### AI Integration
- Google Gemini API
- `@google/genai`

### Development Tools
- Git
- GitHub
- Visual Studio Code
- npm

## 🏗️ Project Structure

```text
interview-ai/
├── Backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── middlewares/
│   │   ├── models/
│   │   ├── routes/
│   │   └── services/
│   ├── server.js
│   ├── package.json
│   └── .env
│
├── Frontend/
│   ├── src/
│   │   ├── features/
│   │   ├── components/
│   │   └── ...
│   ├── package.json
│   └── ...
│
├── .gitignore
└── README.md
```

*Note: The `.env` file is shown here only to illustrate the local project structure. It must not be committed to GitHub.*

## ⚙️ Getting Started

Follow these steps to run the project locally.

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/)
- npm
- [Git](https://git-scm.com/)
- A MongoDB database, such as MongoDB Atlas
- A Google Gemini API key

### 1. Clone the Repository

```bash
git clone https://github.com/TanishQ588/interview-ai.git
cd interview-ai
```

### 2. Configure the Backend

Open a terminal in the project directory:

```bash
cd Backend
npm install
```

Create a `.env` file inside the `Backend` directory and configure the following environment variables:

```env
PORT=3000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_strong_random_secret
GOOGLE_GENAI_API_KEY=your_google_gemini_api_key
```

Replace the placeholder values with your own credentials.

**Never commit your `.env` file or expose your API keys, database credentials, or JWT secret.**

Start the backend:

```bash
node server.js
```

The backend should run on port `3000`, unless configured otherwise.

### 3. Configure the Frontend

Open a second terminal:

```bash
cd Frontend
npm install
```

Start the Vite development server:

```bash
npm run dev
```

Open the local URL printed in the terminal, usually:

```text
http://localhost:5173
```

Keep both development servers running while using the application.

## 🔄 How It Works

1. Enter the target job description.
2. Upload a resume or provide a short self-description.
3. Submit the information to the backend.
4. The backend processes the request and sends the relevant profile information and job description to the Gemini API.
5. The AI generates an interview preparation report.
6. The report is stored in MongoDB.
7. The frontend displays the generated questions, match score, skill gaps, and preparation roadmap.

## 🔐 Security Notes

- Keep API keys and database credentials in environment variables.
- Never commit `.env` files to version control.
- Use strong, unique secrets for authentication.
- Configure production environment variables through your hosting provider.
- Validate uploaded files and handle API errors appropriately.
- Do not expose private credentials in screenshots, logs, or public repositories.

## 🚧 Future Improvements

Potential improvements include:

- More robust handling of AI API errors and rate limits.
- Improved resume parsing and support for additional document formats.
- More detailed job-to-resume skill matching.
- Customizable interview difficulty levels.
- Mock interview sessions with AI feedback.
- Progress tracking across preparation sessions.
- Improved loading states and user-facing error messages.
- Production deployment and performance optimization.

## 🎯 Project Goal

The goal of Interview AI is to make interview preparation more personalized and accessible by helping candidates understand job requirements, identify skill gaps, and prepare strategically for technical and behavioral interviews.

## 👨‍💻 Author

**Tanish Yadav**

- GitHub: [TanishQ588](https://github.com/TanishQ588)

---

If you find this project useful, feel free to explore the repository and share feedback.