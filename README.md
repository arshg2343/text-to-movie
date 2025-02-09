# 🎬 Text-to-MOVIE

An AI-powered movie recommendation engine that transforms your ideas into perfect movie suggestions! Built with React, Go, and powered by LLaMA 3.2 Nemotron 70B.

![Movie Magic](https://github.com/user-attachments/assets/5b657fcc-362c-470d-8a2c-a61959f0ad36)

## ✨ Features

- 🤖 Advanced AI recommendations using LLaMA 3.2 Nemotron 70B
- 🎯 Natural language processing for accurate movie suggestions
- 🎨 Beautiful 3D animations powered by Three.js
- 🎭 Custom font and modern UI design

## 🚀 Tech Stack

### Frontend
- React (Vite)
- Three.js for 3D animations
- TailwindCSS for styling
- Custom fonts for unique typography

### Backend
- Go
- Gin framework
- OpenRouter API integration
- LLaMA 3.2 Nemotron 70B model

## 🌐 Live Demo & Links

### Live Website
- 🎥 **Main Website**: [text-to-movie.netlify.app](https://text-to-movie.netlify.app)
  - Experience the movie recommendation engine in action!

### API & Backend
- 🚂 **Backend Deployment**: [text-to-movie-be.railway.app](https://railway.com/project/20c4c8d9-a3a6-43b8-8295-6a5453336d73?environmentId=0746b3cd-8d6a-4011-9296-1ce4503b83b5)
- 🎯 **API Endpoint**: Send POST requests to:
  ```bash
  https://movie-recommendation-be-production.up.railway.app/
  ```
  Example cURL request:
  ```bash
  curl -X POST \
    https://movie-recommendation-be-production.up.railway.app/ \
    -H 'Content-Type: application/json' \
    -d '{"prompt": "A sci-fi movie with time travel"}'
  ```

### Source Code
- 💻 **Frontend Repository**: [github.com/yourusername/text-to-movie-frontend](https://github.com/arshg2343/text-to-movie-frontend)
  - Hosted on Netlify
  
- 🔧 **Backend Repository**: [github.com/yourusername/text-to-movie-backend](https://github.com/arshg2343/movie-recommendation-be)
  - Deployed on Railway

## 🛠️ Installation

1. Clone the repository
```bash
git clone https://github.com/your-username/text-to-movie.git
cd text-to-movie
```

2. Install frontend dependencies
```bash
cd frontend
npm install
```

3. Install backend dependencies
```bash
cd backend
go mod tidy
```

4. Set up environment variables
```bash
# Frontend (.env)
VITE_API_URL=your_backend_url

# Backend (.env)
OPENROUTER_API_KEY=your_api_key
```
5. Update the fetching logic in app.jsx under the ```handleSubmit``` function (copy this and replace the function code)
```js
const handleSubmit = async (newPrompt) => {
setPrompt(newPrompt);
setLoading(true);
setShowLanding(false);
savePrompt(newPrompt);
setPreviousPrompts(getPrompts());

try {
  const response = await fetch(
    "http://localhost8080/",
    {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
      },
      body: JSON.stringify({ prompt: newPrompt }),
    }
  );

  if (!response.ok) {
    throw new Error(`HTTP error! status: ${response.status}`);
  }

  const data = await response.json();
  setMovies(data);
} catch (error) {
  console.error("Error fetching movies:", error);
  setMovies(null);
} finally {
  setLoading(false);
}
};
```

## 🏃‍♂️ Running the Project

1. Start the frontend
```bash
cd frontend
npm run dev
```

2. Start the backend
```bash
cd backend
go run main.go
```

Visit `http://localhost:5173` to see the magic! ✨

## 🎯 How to Use

1. Enter any prompt describing the type of movie you're looking for
   - Example: "A sci-fi movie with time travel and romance"
   - Example: "Something like Inception but with more action"

2. The AI will analyze your prompt and suggest movies that match your description

3. Browse through the recommended movies and discover your next favorite film!

## 📝 Project Description

Text-to-MOVIE is a college project that demonstrates the power of AI in providing personalized movie recommendations. The project utilizes the state-of-the-art LLaMA 3.2 Nemotron 70B model to understand natural language prompts and suggest relevant movies.

The application features a modern, responsive design with engaging 3D animations that create an immersive user experience. The backend is built with Go for optimal performance, while the frontend uses React with Vite for fast development and production builds.

## 🔄 Project Evolution

The project initially had a more complex architecture:

### Original Implementation
- 🧠 Used Sentence Transformers for converting movie descriptions to vector embeddings
- 📊 Utilized Pinecone as a vector database for efficient similarity search
- 🎯 Integrated wit.ai for natural language processing of user prompts
- 🔍 Two-step recommendation process:
  1. Vector similarity search in Pinecone to find relevant movies
  2. OpenRouter API processing to explain movie selections

### Current Implementation
Due to web deployment challenges with the original architecture, the project was streamlined to its current form, which offers:
- Simplified deployment process
- Faster response times
- More cost-effective operation
- Easier maintenance

While the current version is more streamlined, the original architecture showcases the potential for even more sophisticated recommendation systems using vector embeddings and multi-stage AI processing.

## 🙏 Acknowledgments

- Shoutout to all our professors and mentors who guided us
- Built with ❤️ for movie lovers everywhere

---
*This project was created as part of our college coursework. Feel free to use and modify it for educational purposes!*
