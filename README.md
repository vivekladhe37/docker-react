# React Docker Production-Grade Workflow

## Overview
This project is a production-ready React application, containerized with Docker and orchestrated using Docker Compose. It follows best practices for modern web development, including multi-stage builds, hot-reload for development, and Nginx for production. The project was built as part of the "Docker and Kubernetes: The Complete Guide" Udemy course (Section 6), and demonstrates hands-on skills in Docker, CI/CD, and React.

## Features
- React 18 application (Create React App)
- Dockerized development and production workflows
- Multi-stage Docker builds for optimized images
- Hot-reloading in development with Docker Compose
- Nginx serving static files in production
- Automated testing with Jest and React Testing Library
- Travis CI configuration for continuous integration
- Git version control

## Technologies Used
- React 18
- Docker & Docker Compose
- Nginx
- Travis CI
- Node.js (16-alpine)
- Jest, React Testing Library

## Getting Started

### Prerequisites
- Docker & Docker Compose installed
- Node.js and npm (for local development)

### Local Development (without Docker)
```bash
npm install
npm start
```
App runs on [http://localhost:3000](http://localhost:3000)

### Development with Docker
```bash
docker-compose up
```
- Hot-reload enabled
- Code changes reflected instantly
- Volumes used for node_modules and source code

### Production Build with Docker
```bash
docker build -t react-prod .
docker run -p 80:80 react-prod
```
- Multi-stage build: Node.js for build, Nginx for serving static files
- App available at [http://localhost](http://localhost)

### Running Tests
```bash
npm test
```
Or with Docker Compose:
```bash
docker-compose run --rm tests
```

### Continuous Integration
- Travis CI is configured to run tests and builds on every push
- See `.travis.yml` for pipeline details

## Folder Structure
```
frontend/
├── build/                # Production build output
│   └── static/           # Compiled JS, CSS, media
├── public/               # Static public assets
├── src/                  # React source code
├── Dockerfile            # Multi-stage production build
├── Dockerfile.dev        # Development Dockerfile
├── docker-compose.yml    # Compose for dev & tests
├── .travis.yml           # Travis CI config
├── package.json          # NPM scripts & dependencies
└── README.md             # Project documentation
```

## Key Learning Highlights
- Multi-stage Docker builds for small, secure images
- Hot-reload setup with Docker volumes
- Nginx as a static file server for React
- Docker Compose for orchestrating dev and test environments
- Automated testing and CI/CD integration
- Git for version control and collaboration

## How This Project Showcases My Skills
- End-to-end workflow: local dev, Docker, CI/CD, production
- Deep understanding of Docker best practices
- Real-world React app structure and deployment
- Automated testing and continuous integration
- Clear, maintainable documentation

---

> Built as part of "Docker and Kubernetes: The Complete Guide" (Udemy, Section 6)

---

Feel free to reach out for more details or a walkthrough of the code and workflow!
