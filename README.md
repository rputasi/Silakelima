# SilaKelima: Dashboard Fiskal

*An intelligent fiscal dashboard for monitoring financial transactions and tax collection, powered by a Gemini-based AI assistant for data analysis and insights.*

---

**SilaKelima** is a proof-of-concept dashboard designed for financial analysts at a ministry of finance or central bank. It provides a comprehensive suite of tools to monitor real-time transaction data, analyze tax collection patterns, and leverage the power of Google's Gemini AI for deep, actionable insights.

The project was developed for the **BI-OJK Hackathon 2025**, with a focus on Financial Innovation & Public Services.

## ✨ Core Features

### 📊 Interactive Dashboard
A central hub providing a high-level overview of key fiscal metrics:
- **Stat Cards**: At-a-glance view of total collected tax, transaction volume, and progress towards key social program targets like Universal Basic Income (UBI) and Universal Health Coverage (UHC).
- **Data Visualizations**: Dynamic charts showing transaction volume by category, tax collected per channel, and trends over time.
- **Recent Transactions**: A quick look at the latest financial activities.

### 🤖 Gemini-Powered AI Suite
The dashboard is supercharged with Google's Gemini AI to provide advanced analytical capabilities:
- **Automated AI Insights**: The dashboard automatically surfaces key trends, anomalies, and observations from the dataset, helping analysts spot important patterns without manual digging.
- **Conversational AI Assistant**: A dedicated, full-screen chat interface where analysts can ask complex, natural language questions about the data. The AI maintains conversational context and provides detailed, markdown-formatted answers.
- **AI-Powered Classification**: A tool to automatically categorize transactions and identify their associated industry based on unstructured text descriptions, streamlining data enrichment.

### 📈 Advanced Analytics & Monitoring
- **Tax Analytics Page**: A deep dive into tax data, featuring visualizations of tax distribution by industry and a dedicated table for monitoring high-value tax transactions.
- **Comprehensive Transaction Explorer**: A full-featured page to view all 1,000+ transactions, complete with powerful search and filtering by category.

### 📱 Responsive Design
- **Mobile-First Experience**: A clean, modern UI that adapts seamlessly to any screen size. Includes a dedicated bottom navigation bar for easy access on mobile devices.
- **Modern Aesthetics**: A sleek dark mode theme with professional typography, subtle gradients, and smooth animations for an exceptional user experience.

## 🛠️ Tech Stack

- **Frontend**: React (with Hooks) & TypeScript
- **Styling**: Tailwind CSS
- **AI Integration**: Google Gemini API (`@google/genai`)
- **Charting**: Recharts
- **Bundling**: No bundler! Uses modern browser features like ES Modules and Import Maps.

## 🚀 Getting Started

This application is designed to run directly in a modern browser without a build step.

### Prerequisites
- A modern web browser (e.g., Chrome, Firefox, Edge).
- A valid Google Gemini API Key.

### Installation & Running
1.  **Clone the repository or download the source files.**

2.  **Set up the API Key:**
    The application requires a Google Gemini API key to be available as an environment variable named `process.env.API_KEY`. The execution environment must handle the injection of this variable.

    **Note:** The API key is **not** to be hardcoded into the source files. The application is built to read it from the environment.

3.  **Open `index.html`:**
    Serve the project directory using a simple local server and open `index.html` in your browser.
    ```bash
    # If you have Python 3
    python -m http.server

    # Or use npx
    npx serve
    ```
    Then, navigate to `http://localhost:8000` (or the appropriate port) in your browser.

## 📂 Project Structure

```
.
├── components/         # Reusable React components
│   ├── AIPage.tsx      # Full-screen conversational AI assistant
│   ├── AIInsights.tsx  # Automated insights component for the dashboard
│   ├── Dashboard.tsx   # Main dashboard view
│   ├── TaxAnalytics.tsx# Tax analysis page
│   └── ...             # Other UI components (Header, Sidebar, etc.)
├── services/           # Modules for external services
│   └── geminiService.ts# All logic for interacting with the Gemini API
├── constants.ts        # Mock data and constants, including the transaction generator
├── types.ts            # TypeScript type definitions for the application
├── App.tsx             # Main application component with routing logic
├── index.html          # The entry point of the application
└── index.tsx           # The main React render script
```
