# DigitalWatchdog

DigitalWatchdog is a Python-based monitoring utility deployed as an **Azure Function**. It is designed to provide automated "watchdog" triggers to monitor the health, status, or availability of digital services and sync data or alerts accordingly.

## 🚀 Overview

The project leverages a serverless architecture to ensure high availability and low overhead. By using GitHub Actions for deployment, the watchdog maintains a continuous synchronization between the repository logic and the live Azure environment.

### Key Components
* **`function_app.py`**: The core logic of the watchdog trigger.
* **`requirements.txt`**: Managed dependencies for the Python environment.
* **GitHub Workflows**: Automated CI/CD pipeline to handle build timeouts and deployment.
* **`.vscode/`**: Pre-configured settings for local development and debugging.

---

## 🛠 Tech Stack

* **Language:** Python 3.x
* **Platform:** Azure Functions (Serverless)
* **CI/CD:** GitHub Actions
* **Editor Support:** Visual Studio Code

---

## ⚙️ Setup & Installation

### Prerequisites
* [Azure Functions Core Tools](https://docs.microsoft.com/en-us/azure/azure-functions/functions-run-local)
* [Python 3.9+](https://www.python.org/downloads/)
* An active Azure Subscription

### Local Development
1.  **Clone the repository:**
    ```bash
    git clone https://github.com/El-walid/DigitalWatchdog.git
    cd DigitalWatchdog
    ```

2.  **Create a Virtual Environment:**
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    ```

3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run Locally:**
    ```bash
    func start
    ```

---

## 🚢 Deployment

This repository is configured to use **GitHub-side builds** to prevent local timeout issues. 

To deploy:
1.  Ensure your Azure Service Principal credentials are added to GitHub Secrets.
2.  Push your changes to the `main` branch.
3.  The workflow in `.github/workflows/` will automatically build and deploy the function to your Azure environment.

---

## 📂 Project Structure

```text
DigitalWatchdog/
├── .github/workflows/  # CI/CD pipeline definitions
├── .vscode/            # VS Code launch and settings configurations
├── function_app.py     # Main Azure Function entry point
├── host.json           # Function host metadata
├── requirements.txt    # Python package dependencies
└── .gitignore          # Files excluded from version control
```

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/El-walid/DigitalWatchdog/issues).

---
*Maintained by [El-walid](https://github.com/El-walid)*
