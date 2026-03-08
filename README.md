## 🚀 CI/CD Automation (Jenkins + Vercel)

This project includes a **fully automated CI/CD pipeline** using **Jenkins** and **Vercel**.

Whenever code is pushed to GitHub, Jenkins automatically:

1. Pulls the latest code from GitHub
2. Installs project dependencies
3. Builds the production bundle
4. Deploys the application to **Vercel**

---

## 🔄 CI/CD Workflow

```
Developer
   │
   │ git push
   ▼
GitHub Repository
   │
   │ Webhook Trigger
   ▼
Jenkins Pipeline
   │
   ├── Install Dependencies (npm install)
   │
   ├── Build Application (npm run build)
   │
   └── Deploy to Vercel
           │
           ▼
     Live Production App
```

---

## ⚙️ Jenkins Pipeline Stages

The Jenkins pipeline automatically runs the following stages:

### 1️⃣ Install Dependencies

```
npm install
```

### 2️⃣ Build Application

```
npm run build
```

### 3️⃣ Deploy to Vercel

```
npx vercel --prod --yes --token=$VERCEL_TOKEN
```

---

## 🔐 Secure Deployment

Deployment uses a **secure Vercel token stored in Jenkins Credentials Manager**.

Environment Variable used:

```
VERCEL_TOKEN
```

---

## 🌐 Live Deployment

The application is automatically deployed to Vercel.

**Production URL**

https://jenkins-automate-and-deploy-vercel.vercel.app/

---

## 🧰 Technologies Used

* Jenkins (CI/CD Automation)
* GitHub (Source Control)
* Vercel (Hosting & Deployment)
* Node.js
* Vite + React
* Webhooks for automatic build trigger
