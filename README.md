# TaskFlow - Simple Task Management App

A minimal task management application built for the GitHub Copilot workshop.

## Features

- ✅ Create, read, update, and delete tasks
- ✅ Mark tasks as completed
- ✅ Simple and clean user interface
- ✅ SQLite database (no external dependencies)
- ✅ REST API

## Tech Stack

- **Backend**: Node.js + Express
- **Database**: SQLite3
- **Frontend**: Vanilla HTML/CSS/JavaScript
- **Testing**: Playwright

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd copilot-sample-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

## Running the App

### Development mode (with auto-restart)
```bash
npm run dev
```

### Production mode
```bash
npm start
```

The app will be available at `http://localhost:3000`

## API Endpoints

### Tasks

- `GET /api/tasks` - Get all tasks
- `GET /api/tasks/:id` - Get a single task
- `POST /api/tasks` - Create a new task
  ```json
  {
    "title": "Task title",
    "description": "Task description (optional)"
  }
  ```
- `PUT /api/tasks/:id` - Update a task
  ```json
  {
    "title": "Updated title",
    "description": "Updated description",
    "completed": 1
  }
  ```
- `DELETE /api/tasks/:id` - Delete a task

## Project Structure

```
copilot-sample-app/
├── src/
│   ├── database/
│   │   ├── db.js           # Database connection
│   │   └── init.js         # Database initialization
│   ├── routes/
│   │   └── tasks.js        # Task API routes
│   └── server.js           # Express server setup
├── public/
│   ├── index.html          # Frontend UI
│   ├── styles.css          # Styles
│   └── app.js              # Frontend JavaScript
├── tests/
│   └── example.spec.js     # Playwright tests
├── package.json
└── README.md
```

## Testing

Run Playwright tests:

```bash
npm test
```

Run tests in headed mode (see browser):

```bash
npm test:headed
```

## Workshop Exercises

This app intentionally has some missing features that will be added during the workshop:

1. **Input Validation** - Add validation to task endpoints
2. **Comments Feature** - Add ability to comment on tasks
3. **Priority System** - Add task priorities (High/Medium/Low)
4. **Due Dates** - Add due dates to tasks (demonstrated in workshop)

## License

MIT
