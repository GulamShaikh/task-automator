# 🚀 Task Automator - AI-Powered Workflow Automation Tool

[![Live Demo](https://img.shields.io/badge/Live-Demo-blue?style=for-the-badge)](https://gulamshaikh.github.io/task-automator/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge&logo=github)](https://github.com/GulamShaikh/task-automator)

## 📋 Project Overview

**Task Automator** is a modern, AI-powered workflow automation tool designed to help users schedule, manage, and execute repetitive tasks directly from their web browser. Built as a single-page application, it combines intuitive task scheduling with cutting-edge AI capabilities powered by Google's Gemini API.

This project was developed as a **Mini-Project** for college submission, demonstrating the integration of modern web technologies, AI services, and responsive design principles.

---

## ✨ Key Features

### 🎯 Core Functionality
- **Task Creation & Scheduling**: Define tasks with custom names, action messages, and recurring intervals (seconds, minutes, or hours)
- **Real-time Task Management**: View, pause, resume, and delete scheduled tasks with ease
- **Live Countdown Timer**: Track time remaining until each task's next execution
- **Activity Logging**: Comprehensive real-time log panel showing all task activities (creation, execution, pausing, deletion)
- **Persistent Storage**: Tasks are saved in browser's local storage, surviving page reloads and browser restarts

### 🤖 AI-Powered Features
- **AI Action Execution**: Transform any task into an AI-powered action by checking the "Make this an AI Action" checkbox. The task will use Gemini API to generate intelligent responses based on your prompt
  - Example: "Generate a random motivational quote"
  - Example: "Summarize today's top tech news headlines"
  
- **AI Task Suggester**: Click the "Suggest Tasks with AI" button to describe your goal, and the AI will generate a list of relevant, pre-configured tasks that can be added with a single click
  - Example: "Create tasks for a more focused work session"
  - Example: "Suggest tasks for my evening wind-down routine"

### 🎨 User Interface
- **Modern Design**: Dark-themed interface built with Tailwind CSS
- **Responsive Layout**: Fully responsive design that works seamlessly on desktop, tablet, and mobile devices
- **Intuitive Icons**: Lucide icons for enhanced visual communication
- **Smooth Animations**: Polished transitions and hover effects for better user experience
- **Real-time Clock**: Live date and time display in the header

---

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| **HTML5** | Semantic markup and structure |
| **CSS3** | Custom styling and animations |
| **Tailwind CSS** | Utility-first CSS framework for rapid UI development |
| **JavaScript (ES6+)** | Core application logic and interactivity |
| **Gemini API** | AI-powered task suggestions and dynamic actions |
| **Local Storage API** | Persistent data storage in browser |
| **Lucide Icons** | Modern, customizable icon library |

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, or Edge)
- Internet connection (for CDN resources and Gemini API)
- Gemini API key (optional, for AI features)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/GulamShaikh/task-automator.git
   cd task-automator
   ```

2. **Open the application**
   - Simply open `index.html` in your web browser
   - Or use a local server:
     ```bash
     # Using Python
     python -m http.server 8000
     
     # Using Node.js
     npx http-server
     ```

3. **Configure Gemini API (Optional)**
   - Obtain an API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Enter your API key in the settings when prompted
   - AI features will be enabled automatically

### Live Demo
Visit the live application: **[https://gulamshaikh.github.io/task-automator/](https://gulamshaikh.github.io/task-automator/)**

---

## 📖 How to Use

### Creating a Basic Task
1. Enter a task name (e.g., "Daily Standup Reminder")
2. Add an action message (e.g., "Time for daily standup meeting!")
3. Set the interval (e.g., 10 minutes)
4. Click "Create Task"

### Creating an AI-Powered Task
1. Enter a task name (e.g., "Morning Motivation")
2. Add an AI prompt (e.g., "Generate an inspiring quote for starting the day")
3. **Check the "Make this an AI Action" checkbox**
4. Set the interval (e.g., 1 hour)
5. Click "Create Task"

### Using AI Task Suggester
1. Click the "✨ Suggest Tasks with AI" button
2. Enter your goal (e.g., "Create a productive morning routine")
3. Review AI-generated task suggestions
4. Click "Add Task" for any suggestions you want to schedule

### Managing Tasks
- **Pause**: Click the pause button to temporarily stop a task
- **Resume**: Click the play button to resume a paused task
- **Delete**: Click the delete button to permanently remove a task
- **View Logs**: Scroll through the activity log to see task history

---

## 🎓 Project Highlights

### Educational Value
This project demonstrates proficiency in:
- **Frontend Development**: Modern HTML5, CSS3, and JavaScript
- **API Integration**: RESTful API consumption (Gemini AI)
- **Responsive Design**: Mobile-first, adaptive layouts
- **Data Persistence**: Browser storage mechanisms
- **Asynchronous Programming**: Promises, async/await, and timer management
- **UI/UX Design**: User-centered design principles

### Innovation
- Integration of cutting-edge AI technology (Gemini API) with traditional task scheduling
- Intelligent task suggestion system that learns from user goals
- Dynamic task execution with AI-generated content

### Practical Applications
- Personal productivity management
- Workflow automation for repetitive tasks
- AI-assisted goal planning and achievement
- Study schedule management for students
- Reminder system for important activities

---

## 🔧 Technical Implementation

### Architecture
The application follows a modular architecture with clear separation of concerns:
- **UI Layer**: Handles rendering and user interactions
- **Logic Layer**: Manages task scheduling, execution, and state
- **Storage Layer**: Handles data persistence via Local Storage
- **AI Layer**: Interfaces with Gemini API for intelligent features

### Key Code Highlights

**Task Scheduling with setInterval**
```javascript
// Each task runs on its own timer
const timerId = setInterval(() => {
    executeTask(task);
}, task.interval);
```

**AI Integration**
```javascript
// Gemini API call for AI-powered actions
const response = await fetch(GEMINI_API_URL, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ prompt: task.action })
});
```

**Local Storage Persistence**
```javascript
// Save tasks to survive page reloads
localStorage.setItem('tasks', JSON.stringify(tasks));
```

---

## 📊 Features Comparison

| Feature | Traditional Task Manager | Task Automator |
|---------|-------------------------|----------------|
| Task Scheduling | ✅ | ✅ |
| Recurring Tasks | ✅ | ✅ |
| AI Integration | ❌ | ✅ |
| Task Suggestions | ❌ | ✅ |
| Dynamic Content | ❌ | ✅ |
| Browser-Based | ⚠️ Limited | ✅ Full-Featured |

---

## 🌟 Future Enhancements

- [ ] Export tasks to CSV/JSON
- [ ] Task categories and tags
- [ ] Advanced scheduling (specific dates/times)
- [ ] Notification system (browser notifications)
- [ ] Task templates library
- [ ] Multi-language support
- [ ] Dark/Light theme toggle
- [ ] Cloud sync across devices
- [ ] Task analytics and insights
- [ ] Voice command integration

---

## 📝 Project Documentation

### Development Timeline
- **Week 1**: Planning, research, and UI design
- **Week 2**: Core task scheduling implementation
- **Week 3**: AI integration with Gemini API
- **Week 4**: Testing, refinement, and documentation

### Challenges Faced
1. **Timer Synchronization**: Ensuring accurate task execution across page reloads
2. **API Rate Limiting**: Managing Gemini API calls efficiently
3. **State Management**: Maintaining consistent task states across multiple operations
4. **Responsive Design**: Adapting complex UI for mobile devices

### Solutions Implemented
1. Implemented persistent timer state in Local Storage
2. Added request queuing and error handling for API calls
3. Created centralized state management system
4. Utilized Tailwind's responsive utilities and grid system

---

## 👨‍💻 About the Developer

**Developer**: Gulam Shaikh  
**Project Type**: College Mini-Project  
**Date**: October 2025  
**GitHub**: [@GulamShaikh](https://github.com/GulamShaikh)

---

## 📄 License

This project is open source and available for educational purposes.

---

## 🙏 Acknowledgments

- **Google Gemini AI** for providing the AI capabilities
- **Tailwind CSS** for the excellent utility-first framework
- **Lucide Icons** for the beautiful icon set
- **GitHub Pages** for free hosting

---

## 📞 Contact & Support

For questions, suggestions, or issues:
- **GitHub Issues**: [Report a bug](https://github.com/GulamShaikh/task-automator/issues)
- **Email**: Contact through GitHub profile

---

## 🎯 Conclusion

Task Automator represents a successful integration of traditional task management with modern AI capabilities, demonstrating the potential of intelligent automation in everyday productivity tools. This project showcases practical application of web technologies and AI services in solving real-world problems.

**Live Demo**: [https://gulamshaikh.github.io/task-automator/](https://gulamshaikh.github.io/task-automator/)

---

*Built with ❤️ for educational purposes | © 2025 Gulam Shaikh*
