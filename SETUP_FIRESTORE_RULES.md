# Setting Up Firestore Security Rules

## Current Status
✅ Firestore Database is enabled
✅ Database location: me-central2
⏳ Security rules need to be set

## Step-by-Step Instructions

### 1. Click on "Rules" Tab
In the Firestore Database page, you should see multiple tabs at the top:
- **Data** (currently selected - shows "Start collection")
- **Rules** ← Click this one
- **Usage**
- **Indexes**

### 2. Replace the Default Rules

You'll see a text editor with default rules. Replace ALL of it with this:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

### 3. Click "Publish"

Look for the "Publish" button (usually blue, in the top right of the rules editor).

### 4. Confirm
You might see a warning about allowing anyone to read/write - that's okay for development/testing. Click "Publish" to confirm.

---

## ⚠️ Important

These rules allow **ANYONE** to read and write to your database. This is only for **development and testing**.

For production, you'll need to add authentication and proper security rules.

---

## What's Next?

After setting the rules:

1. **Go back to your app** (main.html in browser)
2. **Refresh the page** (Ctrl+F5)
3. **Check the browser console** (F12 → Console tab)
4. You should see:
   - ✅ `Firebase initialized successfully`
   - ✅ `Firestore initialized`
5. **Make a reservation** - click on any green table
6. **Go back to Firestore** → "Data" tab
7. You should see:
   - Collection: `restaurants`
   - Document: `resto_001`
   - Fields appearing as you use the app!

---

## Test Real-time Sync

1. Open **2 browser windows** with your app
2. Window 1: Click on a table to reserve it
3. Window 2: Watch it change colors instantly! 🎉

