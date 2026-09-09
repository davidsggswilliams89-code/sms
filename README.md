# SHTMS Firebase-Connected Portal Package

## Firebase project
Project ID: `smsh-282c0`

The shared Firebase configuration is in `shared/firebase-config.js`.

## Before login can work
1. Enable **Email/Password** in Firebase Authentication.
2. Create each user in Firebase Authentication.
3. Create a Firestore collection named `users`.
4. Create a document whose document ID exactly matches the user's Firebase UID.
5. Add a `role` field using one of:
   `student`, `lecturer`, `hod`, `registrar`, `bursary`, `admissions`, `admin`.

Example Firestore document:
```json
{ "role": "student", "name": "Student Name", "active": true }
```

## Important
The API key identifies the Firebase project for web clients; access control must still be enforced with Firebase Authentication, Firestore Security Rules, and role checks. Do not rely only on hidden pages or JavaScript for security.

## Running locally
Because this project uses JavaScript modules, run it through a local web server or deploy it to Firebase Hosting/another HTTPS host. Do not rely on opening the HTML files directly with `file://`.
