# Security & Environment Setup

## 🔐 Environment Variables

To run this project, you need to set up your environment variables. **Never commit sensitive keys to git.**

### Step 1: Copy the Example File

```bash
cp .env.example .env
```

### Step 2: Add Your API Keys

Edit the `.env` file and add your actual API keys:

```
GEMINI_API_KEY=your_actual_google_gemini_api_key_here
GOOGLE_API_KEY=your_actual_google_api_key_here
```

### Step 3: Load Environment Variables

**For Python (Backend):**

Install python-dotenv:
```bash
pip install python-dotenv
```

In your Python files, load at the start:
```python
from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.getenv("GEMINI_API_KEY")
```

**For JavaScript/Node.js:**

If using Node, install dotenv:
```bash
npm install dotenv
```

Then in your file:
```javascript
require('dotenv').config();
const apiKey = process.env.GOOGLE_API_KEY;
```

**For Chrome Extension:**

Pass API keys from backend to extension via message passing or fetch from a secure backend endpoint.

---

## ⚠️ Important Security Notes

1. **Never commit `.env` files** - They are in `.gitignore` by default
2. **Never hardcode API keys** in source code
3. **Rotate exposed keys immediately** - If a key was ever committed, regenerate it
4. **Use environment variables** for all sensitive data
5. **Use SecretStr** in Python for added safety

### Getting Google API Keys

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project
3. Enable the required APIs:
   - Google Generative AI API
   - Google Maps API (if needed)
4. Create an API key in Credentials section
5. Add the key to your `.env` file

---

## 🔄 If Keys Were Exposed

If you've committed API keys to git:

1. **Immediately rotate/regenerate the keys** in Google Cloud Console
2. **Force push** to remove the commits (if it's your personal repo):
   ```bash
   git reset --hard HEAD~1  # Remove last commit
   git push --force
   ```
3. **Use BFG Repo-Cleaner** to remove from git history:
   ```bash
   bfg --delete-files .env
   git reflog expire --expire=now --all && git gc --prune=now --aggressive
   git push --force
   ```

---

## ✅ Best Practices

- Use environment variables for all configuration
- Use `.gitignore` to exclude sensitive files
- Review commits before pushing
- Enable branch protection rules
- Use GitHub Secrets for CI/CD workflows
- Regularly audit your repository for exposed secrets
- Use tools like `git-secrets` or `detect-secrets` locally

