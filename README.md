# 🎬 Text-to-MOVIE

An AI-powered movie recommendation engine that transforms your ideas into perfect movie suggestions! Built with React, Go, and powered by LLaMA 3.2 Nemotron 70B.

![Movie Magic](https://raw.githubusercontent.com/your-username/text-to-movie/main/preview.gif)

## ✨ Features

- 🤖 Advanced AI recommendations using LLaMA 3.2 Nemotron 70B
- 🎯 Natural language processing for accurate movie suggestions
- 🎨 Beautiful 3D animations powered by Three.js
- 🎭 Custom font and modern UI design
- ⚡ Lightning-fast performance with Vite and Go

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

## 🤝 Contributing

This is a college project, but we welcome any suggestions or feedback! Feel free to:
- Open issues
- Submit pull requests
- Share ideas for improvements

## 📜 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🙏 Acknowledgments

- Thanks to OpenRouter for providing API access
- Shoutout to all our professors and mentors who guided us
- Built with ❤️ for movie lovers everywhere

---
*This project was created as part of our college coursework. Feel free to use and modify it for educational purposes!*
