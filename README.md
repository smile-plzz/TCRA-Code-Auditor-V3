# TCRA Code Auditor

An AI-powered auditing application utilizing the academic TCRA framework (Transparency, Controllability, Reliability, Auditability) to evaluate raw AI-generated code.

## Features
- **Comprehensive Evaluation**: Evaluates code against Transparency, Controllability, Reliability, and Auditability metrics.
- **AI-Powered Analysis**: Uses large language models (LLMs) to perform semantic analysis, structural auditing, and classification (e.g., Automated Execution vs. Delegated Reasoning).
- **Visual Analytics**: Detailed composite scoring with radar charts, score bars, and risk vector identification.
- **Multi-Provider Support**: Choose between Google Gemini, OpenAI, Anthropic, and GroqCloud.
- **Secure Architecture**: Server-side proxy for secure API key management.
- **Export & History**: Export results as PDF and maintain a local history of your code evaluations.

## Getting Started

### Prerequisites
- Node.js
- npm
- API Keys for your preferred AI providers

### Installation
1. Install dependencies:
```bash
npm install
```

2. Set up environment variables:
Create a `.env` file in the root directory based on `.env.example`. This allows you to configure your API keys securely on the backend.

```env
GEMINI_API_KEY="your_gemini_api_key_here"
GROQ_API_KEY="your_groq_api_key_here"
APP_URL="http://localhost:3000"
```

### Running the Application

To run the development server:
```bash
npm run dev
```
The application will be available at `http://localhost:3000`.

To build for production:
```bash
npm run build
```

To start the production server:
```bash
npm run start
```

## Architecture

This application is built as a full-stack React application with an Express backend:
- **Frontend**: React, Vite, Tailwind CSS, `motion/react` (animations), `lucide-react` (icons).
- **Backend**: Express.js server to proxy API requests and securely handle AI model communications without exposing keys to the client.

## Framework: TCRA

The TCRA framework evaluates AI-generated code across four key dimensions:
- **Transparency (T)**: Visible reasoning trails and clear structural mapping.
- **Controllability (C)**: Explicit limits, human steering ability, and parameter constraints.
- **Reliability (R)**: Determinism, safety invariants, and robust exception handling.
- **Auditability (A)**: Traceability, logging mechanisms, and integration of test coverage.
