# CHINARLI live community chat starter

This package includes a responsive village community website and a Firebase-powered real-time **group chat** scaffold.

## What works after Firebase setup
- Email/password registration and sign-in
- Google sign-in (after enabling it in Firebase)
- Real-time group messages using Cloud Firestore
- Six village chat rooms
- Message sender names and timestamps
- Mobile-friendly chat layout

## Before it can go live
The chat is **not active until you connect your own Firebase project**. The starter does not contain your account credentials, and you must never share private service-account keys.

### 1. Create a Firebase project
Go to https://console.firebase.google.com/ and create a project for CHINARLI.

### 2. Register a web app
In Project settings → General → Your apps, add a Web app. Copy the Firebase web configuration into `firebase-config.js`, replacing every `PASTE_...` placeholder.

### 3. Enable authentication
In Authentication → Sign-in method, enable Email/Password. Enable Google only if you want Google login. Add `chinarli.online` to Authentication → Settings → Authorized domains.

### 4. Create Firestore
In Firestore Database, create a database. Open its Rules tab and paste the contents of `firestore.rules`, then publish. These rules require a signed-in user to read or send group messages, restrict message length and prevent users from editing/deleting posted messages. Review and strengthen them for your actual community before launch; consider group membership, admin moderation, abuse reporting and rate limiting.

### 5. Publish to your existing GitHub website
Upload all files in this folder to the root of the repository used for CHINARLI:
- `index.html`
- `style.css`
- `script.js`
- `firebase-config.js`
- `firestore.rules` (keep this for reference; publish the rules in Firebase Console)

Keep your existing `CNAME` file and custom-domain settings. Commit changes and wait for GitHub Pages to deploy. Your domain stays `https://chinarli.online`.

## Important safety and privacy notes
- This starter implements **group chat**, not private one-to-one chat.
- The demo does not yet include image uploads, online presence, message deletion, reporting, or moderation dashboard.
- Do not invite the public until you have tested authentication and database rules.
- Add trusted moderators, reporting/blocking tools, rate limits and clear community rules before launch.
- Do not collect or publish personal phone numbers, addresses, passwords or other sensitive information in group chats.
- Firebase web config is designed to be included in a web app, but access must be protected by Authentication and Firestore Security Rules. Never put service-account private keys in frontend code.

## Local preview
You can preview the visual layout by hosting these files from a local web server. ES modules generally do not work when opening `index.html` directly with a `file://` URL.
