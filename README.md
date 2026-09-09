# SHTMS Version 2 — GitHub Pages Ready

## IMPORTANT: Upload structure
Upload the CONTENTS of this folder to the root of your GitHub repository:

index.html
admin.html
student.html
...all other HTML files...
shared/
  styles.css
  firebase-config.js
  auth.js

Do NOT upload only index.html.
Do NOT place the entire project inside an extra folder unless GitHub Pages is configured to publish from that folder.

## Firebase setup
1. Firebase Console → Authentication → Sign-in method.
2. Enable Email/Password.
3. Firebase Console → Firestore Database → Create database.
4. For every Firebase Authentication user, create:

Collection: users
Document ID: THE USER'S FIREBASE AUTH UID

Example:
{
  "role": "student"
}

Supported roles:
student
lecturer
hod
registrar
bursary
admissions
admin

## Important
The portals use Firebase Authentication and Firestore role lookup.
The HTML pages are protected using Firebase auth.js.
Do not use the old localStorage protection script from Version 1.

## GitHub Pages
Repository → Settings → Pages → Deploy from branch.
Select the branch and the folder containing index.html.
After publishing, open the generated GitHub Pages address.
