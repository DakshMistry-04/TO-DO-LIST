# To-Do List App

## 1. Table of Contents
* [About the Project](#2-about-the-project)
* [How It Works (Logic Flowchart)](#3-how-it-works-logic-flowchart)
* [Result and Analysis](#4-result-and-analysis)
* [Technology Used](#5-technology-used)

---

## 2. About the Project
The **To-Do List App** is a modern, responsive task management tool built to help users organize daily activities efficiently. It features a clean user interface with advanced functionality such as real-time filtering (All, Active, Completed) and persistent data storage using the browser's `localStorage`. 

The app focuses on a high-quality User Experience (UX), utilizing CSS transitions for hover states and mobile-responsive layouts to ensure accessibility across all devices.

---

## 3. How It Works (Logic Flowchart)
The application follows a persistent data cycle where the user interface and the local storage are always in sync.

```mermaid
graph TD
    A[User Inputs Task] --> B{Form Submit}
    B --> C[Add to 'todos' Array]
    C --> D[Save to localStorage]
    D --> E[Render Todos to DOM]
    E --> F{User Action}
    F -->|Toggle Checkbox| G[Update Status & Re-save]
    F -->|Click Delete| H[Remove from Array & Re-save]
    F -->|Change Filter| I[Filter Array & Re-render]
    G --> E
    H --> E
    I --> E
