# AI Code Review Application

![AI Code Review Application Preview](preview.png)

An intelligent code review application powered by Google's Gemini AI that provides expert-level code analysis and suggestions.

## Features

- **🤖 AI-Powered Code Reviews**: Get detailed code reviews from an AI trained to act as a senior developer with 7+ years of experience
- **✨ Modern UI**: Beautiful, dark-themed interface with glassmorphism effects, vibrant gradients, and smooth animations
- **⚡ Real-time Analysis**: Instant feedback on code quality, best practices, and potential improvements
- **📝 Interactive Code Editor**: Built-in syntax highlighting for easy code input
- **🎨 Markdown Output**: Beautifully formatted review results with syntax highlighting

## Tech Stack

### Backend
- Node.js & Express
- Google Generative AI (Gemini 2.0 Flash)
- CORS enabled for cross-origin requests

### Frontend
- React 19
- Vite (for fast development and building)
- Axios (for API requests)
- PrismJS & Highlight.js (for syntax highlighting)
- React Markdown (for rendering AI responses)

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Google Gemini API key ([Get one here](https://ai.google.dev/))

## Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd code-review-main
   ```

2. **Install Backend Dependencies**
   ```bash
   cd BackEnd
   npm install
   ```

3. **Install Frontend Dependencies**
   ```bash
   cd ../Frontend
   npm install
   ```

4. **Configure Environment Variables**
   
   Create a `.env` file in the `BackEnd` directory:
   ```
   GOOGLE_GEMINI_KEY=your_google_gemini_api_key_here
   ```

## Running the Application

### Start the Backend Server

```bash
cd BackEnd
npm start
```

The backend server will start on `http://localhost:3000`

### Start the Frontend Development Server

```bash
cd Frontend
npm run dev
```

The frontend will start on `http://localhost:5173`

## Usage

1. Open your browser and navigate to `http://localhost:5173`
2. Paste or type your code in the left editor panel
3. Click the "Review" button
4. View the AI-generated code review on the right side

## API Endpoints

### Backend API

- **GET** `/` - Health check endpoint (returns "Hello World")
- **POST** `/ai/get-review` - Get AI code review
  - Request body: `{ "code": "your code here" }`
  - Response: Markdown-formatted code review

## Project Structure

```
code-review-main/
├── BackEnd/
│   ├── src/
│   │   ├── controllers/
│   │   │   └── ai.controller.js
│   │   ├── routes/
│   │   │   └── ai.routes.js
│   │   ├── services/
│   │   │   └── ai.service.js
│   │   └── app.js
│   ├── server.js
│   ├── package.json
│   └── .env
├── Frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   └── main.jsx
│   ├── index.html
│   ├── package.json
│   └── vite.config.js
└── .gitignore
```

## AI Review Capabilities

The AI code reviewer focuses on:

- **Code Quality**: Clean, maintainable, and well-structured code
- **Best Practices**: Industry-standard coding practices
- **Performance**: Optimization opportunities and efficiency improvements
- **Security**: Common vulnerabilities (SQL injection, XSS, CSRF, etc.)
- **Scalability**: Making code adaptable for future growth
- **Readability**: Easy to understand and modify code
- **Error Detection**: Potential bugs and logical flaws
- **Test Coverage**: Suggestions for unit and integration tests
- **Documentation**: Recommendations for comments and docstrings
- **Modern Practices**: Latest frameworks, libraries, and patterns

## Contributing

Feel free to submit issues and enhancement requests!

## License

ISC

## Notes

- Make sure both backend and frontend servers are running for the application to work
- The `.env` file is gitignored for security - never commit your API keys
- The application uses Google's Gemini 2.0 Flash model for fast and accurate code reviews
