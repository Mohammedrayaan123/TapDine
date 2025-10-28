# TapDine

TapDine lets users reserve seats without having the need to wait in long lines.

## 🚀 Real-time Synchronization

TapDine now features **real-time updates** across all devices using Firebase Firestore. When one user makes a change (reserves a table, confirms seated, etc.), the change appears **instantly** on all connected devices - including the staff dashboard.

### Quick Start with Firebase

1. Follow the detailed setup in [FIREBASE_SETUP.md](FIREBASE_SETUP.md)
2. Get your Firebase credentials from [Firebase Console](https://console.firebase.google.com/)
3. Update the `firebaseConfig` in `main.html`
4. Deploy and watch real-time synchronization work!

### Features

- ✅ Real-time table status updates
- ✅ Multi-device synchronization
- ✅ Staff dashboard integration
- ✅ Offline support (localStorage fallback)
- ✅ Automatic reconnection
