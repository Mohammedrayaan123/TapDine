# How to Get Your Firebase Credentials

## Quick Steps

### 1. Open Firebase Console
Go to: https://console.firebase.google.com/

### 2. Open Project Settings
- Click the **gear icon** ⚙️ next to "Project Overview" (top left)
- Click **"Project settings"**

### 3. Create a Web App (if you haven't already)
- Scroll down to **"Your apps"** section
- Click the **web icon** `</>`
- Enter app nickname: `TapDine Web`
- Check "Also set up Firebase Hosting" (optional)
- Click **"Register app"**

### 4. Copy Your Firebase Config
You'll see a code block that looks like this:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyC...",
  authDomain: "tapdine-66c2e.firebaseapp.com",
  projectId: "tapdine-66c2e",
  storageBucket: "tapdine-66c2e.appspot.com",
  messagingSenderId: "133132695923",
  appId: "1:133132695923:web:abc123def456"
};
```

### 5. Copy These Values to Me
Just copy the **apiKey**, **messagingSenderId**, and **appId** values and share them with me, or I can help you update main.html directly.

---

## Alternative: Get Just the API Key

If the web app doesn't show up:

1. In **Project settings**, go to **"General"** tab
2. Scroll to **"Your Firebase SDK snippet"**
3. Select **"Config"** radio button
4. You should see your `apiKey` there

---

## Expected Format

Based on your project, the config should look like:

```javascript
apiKey: "AIzaSyC...", // Your Web API Key
authDomain: "tapdine-66c2e.firebaseapp.com",
projectId: "tapdine-66c2e",
storageBucket: "tapdine-66c2e.appspot.com",
messagingSenderId: "133132695923", // Your project number
appId: "1:133132695923:web:xxxxx" // Your app ID
```

Share these values and I'll update your code! 🚀

