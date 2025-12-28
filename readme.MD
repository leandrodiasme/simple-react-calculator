Simple React Calculator

A simple, clean, and modular calculator interface built using React 18 and Tailwind CSS v4.

This project runs entirely in the browser without any build tools (Webpack/Vite) or bundlers, leveraging Babel Standalone for JSX compilation and Tailwind via CDN for styling. It serves as a study case for component composition and React Hooks.

✨ Features

⚛️ Pure React 18: Functional components and Hooks logic.

🎨 Modern Styling: Styled with Tailwind CSS v4 (Alpha/Beta features like CSS variables in @theme).

🔄 State Management: Logic separated between local UI state and global application state.

🧩 Component Architecture: Reusable Text, Button, and Card components with variant props.

📱 Responsive Design: Adaptive layout for mobile and desktop screens.

🚀 No build step required: Just open the HTML file.

🧠 Technical Concepts & Hooks

This project explicitly demonstrates the use of core React Hooks to manage application logic and data flow:

1. useState Hook

Used for managing local component states:

Calculator Logic: Tracks the current operation string (input buffer) and the calculated result.

History Array: Manages the list of past calculations within the provider.

2. useContext Hook & Context API

Implemented to solve the Prop Drilling problem.

A CalculatorContext was created to share the History state and the update function across the application.

This allows the <Calculator /> component to write data to the history, and the <OperationHistory /> component to read it, without passing props through the main <App /> component.

// Simplified logic flow
<CalculatorProvider> { /_ Holds the History State _/ }
<Calculator /> { /_ Writes to Context via updateHistory() _/ }
<OperationHistory /> { /_ Reads from Context via history array _/ }
</CalculatorProvider>

🛠️ Technologies Used

Core: HTML5, JavaScript (ES6+)

Library: React 18, ReactDOM

Styling: Tailwind CSS (Script Version)

Compiler: Babel Standalone (for in-browser JSX transformation)

📂 Project Structure

The project uses a single-file architecture for simplicity, but logically separates concerns:

/
├── index.html # Contains all logic, styles, and markup
└── README.md # Documentation

Component Breakdown

UI Components: Text, Button, Card (Presentational)

Feature Components: Calculator, OperationHistory (Logic-heavy)

Context: CalculatorProvider (State Container)

🚀 How to Run

Since this project requires no build step:

Clone or download the repository.

Open index.html directly in your browser.

Enjoy!
