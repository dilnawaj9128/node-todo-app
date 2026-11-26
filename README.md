# Node Todo App

A basic to-do list application built with Node.js, Express and EJS. Add, edit and delete tasks through the web interface. Tasks are stored in memory and are lost when the application restarts.

## Run locally

Install Node.js and npm first. On Ubuntu, these are available through `sudo apt install nodejs npm`.

```bash
npm install
npm start
```

Alternatively, start the application with `node app.js`.

Open [http://localhost:8000/todo](http://localhost:8000/todo) in your browser.

## Run tests

```bash
npm test
```

The test script uses Mocha. Install development dependencies before running it.

## Run with Docker

From the repository root:

```bash
docker build -t node-todo-app .
docker run --rm -p 8000:8000 node-todo-app
```

The Dockerfile installs dependencies and runs the test suite during the image build. Open the same `/todo` URL after the container starts.

Docker Compose can also be used if you supply a suitable Compose configuration.

**Note:** The existing Dockerfile uses Node.js 12, which is end-of-life. Treat this image as a learning example rather than a production-ready deployment.
