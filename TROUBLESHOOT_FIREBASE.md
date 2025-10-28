# Troubleshooting Firebase Connection

## Let's Debug Step by Step

### Step 1: Check Browser Console

1. **Open main.html in your browser**
2. **Press F12** (or Right-click → Inspect → Console tab)
3. **Take a screenshot** or copy/paste what you see in the console

Look for these messages:
- ✅ Good signs:
  - `🍽️ TapDine Professional Reservation System Loading...`
  - `✅ Firebase initialized successfully`
  - `✅ Firestore initialized`
  - `✅ State saved to Firebase`

- ❌ Bad signs:
  - `❌ Firebase initialization failed`
  - `ReferenceError: firebase is not defined`
  - `Running in offline mode with localStorage`
  - Any red error messages

### Step 2: Test a Simple Action

1. Click on a **green table** (available table)
2. Fill in the reservation form:
   - Name: `Test User`
   - Phone: `1234567890`
   - Party: `2 people`
3. Click "Reserve Table"
4. Look in the console - do you see any messages?

### Step 3: Check Firestore Database

1. Go back to Firebase Console
2. Click Firestore Database
3. Click on **"Data"** tab
4. Do you see anything? Should show:
   - Collection: `restaurants`
   - Document: `resto_001`

---

## Copy/Paste Your Console Output Here

Please share:
1. What messages you see in the browser console (F12)
2. Any error messages in red
3. What happens when you try to make a reservation

---

## Quick Fixes to Try

### Fix 1: Hard Refresh
- Press **Ctrl + Shift + R** (Windows)
- Or **Cmd + Shift + R** (Mac)
- This clears cache and reloads everything

### Fix 2: Clear Browser Cache
- Press F12
- Right-click the refresh button
- Select "Empty Cache and Hard Reload"

样式
### Fix 3: Check Firestore Rules Are Active
- In Firebase Console → Firestore → Rules tab
- Make sure it shows: "Rules deployed successfully"
- If not, click "Publish" again

---

Let me know what you see in the console!

