# Deploying Basic Security Log Analyzer to Vercel

This project is pre-configured and 100% ready for deployment on **Vercel Serverless Functions**.

---

## Pre-Configured Vercel Files
1. **`vercel.json`** – Directs all incoming web traffic to the Vercel Python serverless runtime (`@vercel/python`).
2. **`api/index.py`** – Serverless WSGI entrypoint that loads `main.py`'s Flask application.
3. **`requirements.txt`** – Specifies dependencies (`Flask`, `Werkzeug`, `Jinja2`) that Vercel auto-installs during build.
4. **`.vercelignore`** – Excludes unnecessary local files, caches, and archives to optimize upload speed.

---

## Method 1: Deploy via GitHub (Recommended & Easiest)

### Step 1: Create a GitHub Repository
1. Go to [https://github.com/new](https://github.com/new).
2. Create a new repository named `basic-security-log-analyzer` (Public or Private).

### Step 2: Push Your Code
Open PowerShell or Terminal and run:

```powershell
cd "c:\Users\Srinivas\OneDrive\Documents\New folder\basic_security_log_analyzer"

# Rename branch to main
git branch -M main

# Add your GitHub repository URL (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/basic-security-log-analyzer.git

# Push to GitHub
git push -u origin main
```

### Step 3: Connect and Deploy on Vercel
1. Log in to your [Vercel Dashboard](https://vercel.com/dashboard).
2. Click **"Add New..."** -> **"Project"**.
3. Select your GitHub repository (`basic-security-log-analyzer`).
4. Keep all default settings:
   * **Framework Preset**: `Other`
   * **Root Directory**: `./`
5. Click **"Deploy"**.

Within ~40 seconds, Vercel will build and provide your live production URL:
`https://basic-security-log-analyzer.vercel.app`

---

## Method 2: Deploy via Vercel CLI

If you have Node.js installed on your machine, you can deploy directly from your command line:

```powershell
cd "c:\Users\Srinivas\OneDrive\Documents\New folder\basic_security_log_analyzer"

# Run Vercel deployment tool
npx vercel
```

Follow the interactive prompts:
* **Set up and deploy?** Press `y` (Yes).
* **Which scope?** Select your personal account.
* **Link to existing project?** Press `n` (No).
* **What's your project's name?** `basic-security-log-analyzer`
* **In which directory is your code located?** `./`
* **Want to modify settings?** Press `n` (No).

For production deployment:
```powershell
npx vercel --prod
```

Your web application will be live instantly!
