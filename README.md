Here is your complete, raw Markdown code matching that exact structure and content, fully cleaned up with proper formatting, code blocks, and lists.

You can copy and paste this directly into your **README.md** file:

```markdown
# Automated React CI/CD & Static Azure Web Hosting

An end-to-end cloud deployment project that automates the continuous integration and continuous deployment (CI/CD) lifecycle of a ReactJS application. The frontend application is built, tested, and deployed entirely through automated pipelines into highly available Azure Storage static web containers.

## 🚀 Live Demo

The application is deployed and accessible at: 👉 http://abdullah12345.z32.web.core.windows.net

## 🏗️ Architecture & Workflow

* **Code Commit:** Developer pushes React code to the main branch on GitHub.
* **CI Trigger:** The Azure DevOps Pipeline automatically spins up an environment running Node 18.x.
* **Build & Compile:** The runner installs dependencies (`npm install`) and builds production-optimized static assets (`npm run build`).
* **CD Cloud Deployment:** The Azure Blob File Copy task securely authenticates with Azure and uploads the contents of the compiled `build/` folder directly to the `$web` storage container.
* **Static Hosting:** Azure Storage Account serves the single-page application (SPA) natively with low-latency delivery.

## 🛠️ Tech Stack & Key Concepts

* **Frontend Framework:** React.js
* **Runtime Environment:** Node.js (v18.x)
* **CI/CD Orchestration:** Azure DevOps Pipelines
* **Cloud Infrastructure:** Azure Blob Storage (Static Website Hosting)
* **Identity & Access Management:** Azure Service Connections / RBAC Contributor access

## 📋 Pipeline Configuration Summary

The core automation is handled within Azure DevOps. The workflow includes the following pipeline steps:
* **Node.js Tool Installer:** Sets the build agent environment to use modern Node 18.x.
* **npm install:** Restores and caches project dependencies.
* **npm run build:** Compiles the source files, generating a lean, optimized `build/` directory.
* **AzureBlob File Copy:** Extracts the compiled static assets and writes them to the `$web` destination container of the target Azure Storage account.

## ⚙️ Client-Side Routing Fix (Handling 404s on Page Refresh)

To ensure that direct URLs and browser reloads (such as `/employee` or `/department`) route smoothly within a Single Page Application (SPA), the Azure Storage Account static website configuration is optimized by mapping the **Error document path** back to `index.html`. This ensures the client-side router handles deep links flawlessly.

## 💻 How to Run Locally

To test the application or build scripts locally, clone the repository and execute the following commands:

```bash
# Clone the repository
git clone [https://github.com/abpatel12/react-azure-devops-cicd.git](https://github.com/abpatel12/react-azure-devops-cicd.git)

# Navigate into the project directory
cd react-azure-devops-cicd

# Install dependencies
npm install

# Run the development server locally
npm start

# Test the production build locally
npm run build

```

```

```