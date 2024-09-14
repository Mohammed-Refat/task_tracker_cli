# Task Tracker CLI

A command-line application to manage tasks using Java. This Task Tracker allows users to create, update, delete, and list tasks, with each task stored locally in a JSON file.

## Features

- **Add Task**: Add a new task with a description.
- **Update Task**: Update the description of an existing task.
- **Delete Task**: Remove a task by its ID.
- **List Tasks**: View all tasks, filter by status (e.g., ToDo, InProgress, Done).
- **Change Task Status**: Mark a task as "In Progress" or "Done."
- **Persistence**: Task data is saved in a local JSON file (`tasks.json`).

## Prerequisites

Before running the project, ensure you have the following installed:

- Java 17 or higher
- Git

## Setup

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Mohammed-Refat/task_tracker_cli.git
   cd task_tracker_cli
   ```

2. **Compile the Project**

   Navigate to the `src` folder and compile the Java classes:

   ```bash
   cd src
   javac TaskTrackerApp.java Task.java TaskManager.java Status.java
   ```

3. **Run the Application**

   After compilation, you can run the application using:

   ```bash
   java TaskTrackerApp [command] [options]
   ```

## Usage

### Available Commands:

# Adding a new task
java TaskCLIApp add "Buy groceries"
# Output: Task added successfully (ID: 1)

# Updating a task
java TaskCLIApp update 1 "Buy groceries and cook dinner"
# Output: Task updated successfully (ID: 1)

# Deleting a task
java TaskCLIApp delete 1
# Output: Task deleted successfully (ID: 1)

# Marking a task as in progress
java TaskCLIApp mark-in-progress 1
# Output: Task marked as in progress (ID: 1)

# Marking a task as done
java TaskCLIApp mark-done 1
# Output: Task marked as done (ID: 1)

# Listing all tasks
java TaskCLIApp list
# Output: List of all tasks

# Listing tasks by status
java TaskCLIApp list todo
java TaskCLIApp list in-progress
java TaskCLIApp list done


## Project Structure

```bash
.
├── tasks.json              # Stores the tasks in JSON format
├── Task.java               # Task class with task properties and methods
├── TaskManager.java        # Manages task operations (CRUD)
└── TaskTrackerApp.java     # CLI entry point, handles command-line arguments
```

## JSON File Structure

Tasks are stored in `tasks.json` in the following format:

```json
[
  {
    "id": "1",
    "description": "Solve problem",
    "status": "TODO",
    "createdAt": "2024-09-12T10:15:30",
    "updatedAt": "2024-09-12T10:15:30"
  }
]
```

## Contributions

Feel free to fork this repository and submit a pull request with improvements or bug fixes.
