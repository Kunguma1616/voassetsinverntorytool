# Engineer Asset Inventory System

A full-stack application for managing engineer asset inventories with AI-powered metadata extraction and PDF report generation.

## Features

- Upload multiple asset images
- AI-powered metadata extraction using GROQ
- Asset management interface
- Professional PDF report generation
- Modern, responsive UI

## Tech Stack

### Frontend
- React 18 with TypeScript
- Vite for build tooling
- TailwindCSS for styling
- Shadcn/ui components
- Axios for API calls
- React Router for navigation
- Sonner for toast notifications

### Backend
- FastAPI (Python)
- GROQ AI for image analysis
- ReportLab for PDF generation
- CORS enabled for frontend communication

## Quick Start

### Backend Setup

1. Navigate to backend folder:
\`\`\`bash
cd backend
\`\`\`

2. Install dependencies:
\`\`\`bash
pip install -r requirements.txt
\`\`\`

3. Create `.env` file:
\`\`\`bash
cp .env.example .env
\`\`\`

4. Add your GROQ API key to `.env`:
\`\`\`
GROQ_API_KEY=your_actual_api_key_here
\`\`\`

5. Run the FastAPI server:
\`\`\`bash
uvicorn main:app --reload --host 0.0.0.0 --port 8000
\`\`\`

The backend will be available at `http://localhost:8000`

### Frontend Setup

1. Install dependencies:
\`\`\`bash
npm install
\`\`\`

2. Create `.env` file:
\`\`\`bash
cp .env.example .env
\`\`\`

3. Update `.env` with your backend URL (default is correct):
\`\`\`
VITE_API_URL=http://localhost:8000
\`\`\`

4. Run the development server:
\`\`\`bash
npm run dev
\`\`\`

The frontend will be available at `http://localhost:5173`

## Usage

1. **Upload Assets**: Navigate to the home page and upload one or multiple asset images
2. **Review Assets**: View all uploaded assets with extracted metadata
3. **Generate Report**: Enter engineer details and generate a professional PDF report

## API Endpoints

- `GET /` - Health check
- `POST /upload-image` - Upload asset image and extract metadata
- `POST /generate-pdf` - Generate PDF report with all assets

## Environment Variables

### Frontend
- `VITE_API_URL` - Backend API URL (default: http://localhost:8000)

### Backend
- `GROQ_API_KEY` - Your GROQ API key for AI image analysis

## Project Structure

\`\`\`
/
├── backend/
│   ├── main.py              # FastAPI application
│   ├── requirements.txt      # Python dependencies
│   └── .env.example         # Environment variables template
├── src/
│   ├── components/          # React components (shadcn/ui)
│   ├── pages/              # Application pages
│   ├── context/            # React context for state management
│   ├── lib/                # API client and utilities
│   └── main.tsx            # Application entry point
└── README.md
\`\`\`

## Building for Production

### Frontend
\`\`\`bash
npm run build
\`\`\`

### Backend
Deploy using your preferred method (Docker, Vercel, Railway, etc.)

## Troubleshooting

- **CORS Issues**: Ensure backend CORS middleware allows your frontend origin
- **Image Upload Fails**: Check file size limits and GROQ API key
- **PDF Generation Fails**: Verify all required fields are filled and assets are uploaded

## License

MIT
