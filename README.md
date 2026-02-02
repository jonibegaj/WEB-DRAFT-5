# UEFA Champions League - Full-Stack Fan Experience

Welcome to the **UCL Web Portal** – a modern, full-stack application dedicated to the UEFA Champions League. This project has evolved from a static site into a dynamic, data-driven experience featuring a robust **C# ASP.NET Core** backend and a **SQLite** database.

---

## Key Features

### Interactive Fan Tools
- **UCL Quiz Game**: Test your knowledge with an interactive quiz. Includes a **Global Leaderboard** that saves your high scores permanently.
- **Fantasy Football**: Build your dream team of 6 players! Simulate match days, calculate points based on player performance, and compete for the top spot on the **Fantasy Leaderboard**.

### Dynamic Data Exploration
- **Top Clubs**: Explore the history of European giants. Click any club to view its founding year, UCL seasons played, and total trophies won.
- **Top Players**: Detailed statistics for the greatest goalscorers and assist providers. View biographies, market values, and career milestones.
- **Real-Time Search**: Quickly find your favorite players using the integrated search system.

### Premium UI/UX
- **Custom Modals**: Replaced generic browser popups with beautiful, themed UCL modals for a seamless, "app-like" feel.
- **Responsive Design**: Optimized for everything from desktop monitors to mobile phones.
- **UCL Gallery**: A visual journey through iconic Champions League moments.

---

## Technology Stack

- **Frontend**: HTML5, CSS3 (Vanilla), JavaScript (ES6+)
- **Backend**: C# ASP.NET Core 10.0
- **Database**: SQLite (via Entity Framework Core)
- **Tooling**: VS Code, .NET SDK

---

## Project Structure
```text
├── UclBackend/          # C# Web API project
│   ├── Controllers/     # API Endpoints (Clubs, Players, Fantasy, Leaderboard)
│   ├── Models/          # Database Schema (PlayerDetails, ClubDetails, etc.)
│   ├── Data/            # Entity Framework DbContext
│   └── DataSeeder.cs    # Automatic database initialization
├── frontend/            # All UI files (HTML, CSS, JS) served by the backend
├── Images/              # Team logos and player photography
└── .vscode/             # Launch configurations for quick debugging
```

---

## How to Run

### **Option 1: The Quick Way (VS Code F5)**
1. Open this folder in **Visual Studio Code**.
2. Press **`F5`** on your keyboard.
3. The project will automatically build, start the server, and open `http://localhost:5000` in your browser.

### **Option 2: Using the Command Line**
1. Open your terminal in the `UclBackend` directory:
   ```powershell
   cd UclBackend
   ```
2. Run the application:
   ```powershell
   dotnet run --urls "http://localhost:5000"
   ```
3. Open your browser and go to `http://localhost:5000`.

---

## Backend Functionality

- **Persistence**: High scores and fantasy teams are stored in `ucl.db`.
- **Dynamic Content**: Data is served via RESTful API endpoints (e.g., `/api/clubs`, `/api/players`).
- **Static Hosting**: The backend is configured to serve all frontend static files from the `frontend` folder, unifying the solution into a single running process.
