# React Todo App

A simple Todo application built with React that allows you to:
- Add new tasks
- Edit existing tasks
- Mark tasks as complete
- Delete tasks
- Persist tasks using browser's localStorage

## Project Structure

```
react-todo-app/
├── public/
│   ├── index.html
│   └── ...
├── src/
│   ├── App.js         # Main application component
│   ├── App.css        # Styles for the app
│   ├── index.js       # Entry point
│   └── index.css      # Global styles
├── package.json       # Dependencies and scripts
└── Dockerfile         # For containerization
```

## How to Run Locally

1. Install dependencies:
   ```
   npm install
   ```

2. Start the development server:
   ```
   npm start
   ```

3. Open [http://localhost:3000](http://localhost:3000) in your browser.

## How to Build and Run with Docker

1. Build the Docker image:
   ```
   docker build -t react-todo-app .
   ```

2. Run the container:
   ```
   docker run -p 8080:80 react-todo-app
   ```

3. Access the application at [http://localhost:8080](http://localhost:8080)

## Features

- **Add Tasks**: Enter a task and click "Add"
- **Edit Tasks**: Click "Edit" to modify a task
- **Complete Tasks**: Check the checkbox to mark a task as complete
- **Delete Tasks**: Remove tasks you no longer need
- **Data Persistence**: All tasks are saved in your browser's localStorage

## Technical Notes

- This app uses React's useState and useEffect hooks for state management
- LocalStorage is used for data persistence (no backend database required)
- The app is containerized using Docker with a multi-stage build process
- Nginx is used as the web server in the production container