# Task-

Create a task board application where users can manage tasks using drag-and-drop functionality. The board should have columns representing different stages of a task (e.g., To-Do, In Progress, Done). Allow users to move tasks between columns and persist the changes.

Note :- Make a new project and complete the flow using React and Typescript .

#       Project Documentation - 

# Task Board Application Documentation

## Table of Contents

1. Introduction
2. Technologies Used
3. Project Setup
4. Components Overview
5. Drag-and-Drop Implementation
6. Data Persistence
7. Conclusion

## 1. Introduction

The Task Board Application is a web-based application that allows users to manage tasks using drag-and-drop functionality. The application provides a visual representation of tasks in different stages (columns), such as To-Do, In Progress, and Done. Users can easily move tasks between columns, and the changes are persisted to ensure data integrity.

## 2. Technologies Used

- React: A JavaScript library for building user interfaces.
- TypeScript: A typed superset of JavaScript that compiles to plain JavaScript.
- react-beautiful-dnd: A library for implementing drag-and-drop functionality in React applications.
- Local Storage: For persisting task data locally in the browser.

## 3. Project Setup

1. Install Node.js and npm (Node Package Manager) if not already installed.
2. Create a new project directory.
3. Open a terminal in the project directory and run the following commands:
   ```bash
   npm create-react-app task-board-app --template typescript
   cd task-board-app
   npm install 
   ```
4. Replace the content of the `src` folder with your own code.

## 4. Components Overview

### 4.1 `App.tsx`

The main component that sets up the structure of the task board application. It renders the columns and tasks.

### 4.2 `Column.tsx`

Represents a column on the task board. It renders the title of the column and the list of tasks within it.

### 4.3 `Task.tsx`

Represents an individual task. It displays the task's content and handles the drag-and-drop functionality.

## 5. Drag-and-Drop Implementation

To implement drag-and-drop functionality, we'll use the `react-beautiful-dnd` library.

1. Import the necessary components from the library.
2. Create a state to hold the task data.
3. Map through the task data and render tasks within their respective columns.
4. Wrap each task in a `Draggable` component, providing a unique `draggableId`.
5. Wrap each column in a `Droppable` component, providing a unique `droppableId`.
6. Implement event handlers to manage task movement between columns.
7. Update the state when tasks are moved and re-render the components.

## 6. Data Persistence

To persist task data, we'll use the browser's Local Storage API.

1. When a task is moved, update the task data in the state.
2. Use the `localStorage.setItem()` method to store the updated task data in Local Storage.
3. When the application is loaded, use the `localStorage.getItem()` method to retrieve the task data from Local Storage.
4. Initialize the state with the retrieved task data to display the tasks in their last saved positions.

## 7. Conclusion

The Task Board Application provides users with a convenient way to manage tasks using drag-and-drop functionality. It employs React, TypeScript, and the `react-beautiful-dnd` library to create a seamless user experience. The integration of Local Storage ensures that task data is persistently stored, allowing users to pick up where they left off even after closing the application. This project serves as a foundation for building more advanced task management systems and can be extended with additional features and improvements.
