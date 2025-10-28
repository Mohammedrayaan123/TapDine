# Testing Your Firebase Integration

## ✅ Configuration Complete!

Your Firebase is now configured with:
- Project ID: `tapdine-66c2e`
- API Key: `AIzaSyDtf6c-moQiSfsbgNiLM13Ye3ep7OScomU`
- App ID: `1:133132695923:web:19c473b2dc068218c5ed06`

## 🎯 Next Steps

### 1. Enable Firestore Database

1. Go to Firebase Console: https://console.firebase.google.com/project/tapdine-66c2e
2. Click **"Firestore Database"** in the left sidebar
3. Click **"Create database"**
4. Choose **"Start in test mode"** (for development)
5. Select a location closest to you (e.g., `us-central`, `europe-west`, `asia-southeast`)
6. Click **"Enable"**

### 2. Set Security Rules (Important!)

After creating the database:

1. Go to the **"Rules"** tab in Firestore
2. Replace with this for **development**:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true; // ⚠️ Only for development!
    }
  }
}
```

3. Click **"Publish"**

⚠️ **Warning**: These rules allow anyone to read/write. Use only for development/testing!

### 3. Test Your App

1. **Open your app** in a browser (double-click `main.html` or serve it)
2. **Open browser console** (F12 or Right-click → Inspect → Console)
3. **Look for these messages**:
   - ✅ `Firebase initialized successfully`
   - ✅ `Firestore initialized`
   - ✅ `State saved to Firebase`

### 4. Test Real-time Sync

1. **Open 2 browser windows/tabs** with your app
2. **Window 1**: Make a reservation (click on an available table)
3. **Window 2**: Watch the table turn **yellow** (reserved) instantly!
4. **Window 1**: Click "I'm Seated"
5. **Window 2**: Watch it turn to **awaiting status**

You should see in console:
- 🔥 `Real-time update received from Firebase`

## 🐛 Troubleshooting

### "Firestore is not a function"
- **Cause**: Firestore not enabled yet
- **Fix**: Complete Step 1 above

### "Permission denied"
- **Cause**: Security rules too restrictive
- **Fix**: Complete Step 2 above and use test mode rules

### "Firebase initialization failed"
- **Cause**: Incorrect credentials
- **Fix**: Double-check your apiKey and appId match Firebase Console

### No real-time updates
- **Check**: Browser console for errors
- **Check**: Network tab for Firebase connections
- **Check**: Firestore shows a `restaurants` collection with `resto_001` document

## 🎉 Success Indicators

You'll know it's working when:
- ✅ Console shows "Firebase initialized successfully"
- ✅ Tables sync instantly across multiple browser windows
- ✅ Firestore database shows data being written
- ✅ No console errors related to Firebase

## 📊 View Your Data

1. Go to Firebase Console → Firestore Database
2. You should see:
   - Collection: `restaurants`
   - Document: `resto_001`
   - Fields: `tables`, `notifications`, `queues`, etc.

---

Ready to test? Let's see those real-time updates! 🚀

