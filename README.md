## Prerequisites

Before you begin, ensure you have the following installed:

-   **Node.js** (v18 or higher) - [Download](https://nodejs.org/)
-   **Python** (v3.8 or higher) - [Download](https://www.python.org/downloads/)
- **MongoDB** - [Download](https://www.mongodb.com/try/download/community) or use a cloud service like [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
- **Google Calendar API credentials**. Follow the instructions [here](https://developers.google.com/workspace/guides/create-credentials) to create OAuth 2.0 Client IDs and download the `credentials.json` file.
- **Gemini API Key** - Sign up for an account at [Gemini](https://ai.google.dev/gemini-api/docs) and obtain your API key.

## Installation & Setup

### 1. Backend Setup (FastAPI)

```cmd
cd backend
pip install -r requirements.txt
```

### 2. Frontend Setup (Nuxt 3)

Open a new terminal and navigate to the project root:

```cmd
npm install
```

### 3. Generate Google API Credentials

Open a terminal in project root and run:

```cmd
python backend/gen_tokens.py
```

This should generate a `token.json` file in the `backend` directory after completing the OAuth2 flow in your browser.


## Running the Application

### Option 1: Run Both Services Separately (Recommended for Development)

#### Terminal 1 - Backend Server:

```cmd
cd backend
python main.py
```

The backend API will be available at: **http://localhost:8000**

API Documentation (Swagger UI): **http://localhost:8000/docs**

#### Terminal 2 - Frontend Server:

```cmd
npm run dev
```

The frontend will be available at: **http://localhost:3000**
