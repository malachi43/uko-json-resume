# 🚀 Auto-Update Resume on GitHub Gist

This repository automates the process of updating a **resume.json** file in a GitHub Gist whenever changes are pushed to this repository.

## 📌 Prerequisites

Before you begin, make sure you have:

- A **GitHub account**
- Basic knowledge of Git
- A JSON version of your resume

---

## 📜 Setup Guide

Follow these steps to set up the automation:

### **1️⃣ Create a Gist for Your Resume**

1. Go to [GitHub Gist](https://gist.github.com/).
2. Click **New Gist**.
3. Create a new file named **resume.json**.
4. Paste your resume in JSON format and **save the Gist**.
5. Copy the Gist ID from the URL (it will be something like `https://gist.github.com/yourusername/abcd1234efgh5678`).
   - Example Gist ID: `abcd1234efgh5678`

### **2️⃣ Fork or Clone This Repository**

You can either fork this repository or create a new one.

#### **Fork this repo (Recommended)**

1. Click the **Fork** button at the top-right corner of this repo.
2. Clone your forked repo:
   ```sh
   git clone https://github.com/yourusername/repo-name.git
   ```
3. Navigate into the project folder:
   ```sh
   cd repo-name
   ```
4. Replace the existing **resume.json** with your own **resume.json**.
5. Commit and push the changes:
   ```sh
   git add resume.json
   git commit -m "Updated resume.json"
   git push origin main
   ```

### **3️⃣ Create a Personal Access Token (PAT) for Gist Updates**

1. Go to **GitHub Settings** → **Developer Settings** → **Personal Access Tokens**.
2. Click **Generate New Token**.
3. **Select the `gist` scope only** to restrict permissions.
4. Click **Generate Token** and copy the token.

### **4️⃣ Add the Token as a GitHub Secret**

1. Go to your repository on GitHub.
2. Navigate to **Settings** → **Secrets and variables** → **Actions**.
3. Click **New repository secret**.
4. Set the **name** as `GIST_PAT_TOKEN`.
5. Paste the **token value** from step 3.
6. Click **Add secret**.

### **5️⃣ Push Changes to Trigger the Update**

Now, every time you push an update to **resume.json**, the automation will:

- Take the new file from your repo
- Override the existing resume.json in your Gist
- Keep your resume up-to-date in the registry

Simply update and push:

```sh
git add resume.json
git commit -m "Updated resume"
git push origin main
```

## 🎯 Automation & GitHub Actions

This repository includes a GitHub Action that automates the syncing process. The action is triggered on every push to the **main** branch and updates the Gist.

---

## 💡 Additional Notes

- Make sure your **resume.json** follows the [JSON Resume schema](https://jsonresume.org/).
- The **GitHub token should remain private**. Do not expose it in commits.
- If you ever regenerate your **Personal Access Token**, update it in your repository secrets.

---

## 🎉 Congratulations!

You have successfully automated your resume updates! 🚀

