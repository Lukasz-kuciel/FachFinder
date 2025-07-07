# FachFinder

A simple web application for posting and finding freelance jobs.  
Clients can post job offers, and professionals (fachowcy) can apply.

Built using HTML, JavaScript and Firebase.

Features

- Firebase Authentication (email & password)
- Job posting form (title, description, location)
- Stores jobs in Firestore database
- Only logged-in users can post jobs
- Works locally via simple HTTP server

---------------------------------------

This project does NOT include the real firebase-config.js file (on purpose, for security reasons).
You need to create it yourself based on the example provided.
Create a file called firebase-config.js in the root directory and paste your own Firebase config like this:

import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-app.js";
import { getAuth } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js";
import { getFirestore } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-firestore.js";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "your-app.firebaseapp.com",
  projectId: "your-app",
  storageBucket: "your-app.appspot.com",
  messagingSenderId: "YOUR_MSG_ID",
  appId: "YOUR_APP_ID"
};

const app = initializeApp(firebaseConfig);
const auth = getAuth(app);
const db = getFirestore(app);

export { auth, db };

Use firebase-config.example.js as a reference.

TODO:
	•	Job filtering & search
	•	User profiles
	•	Job application system
	•	Notifications
	•	Mobile responsive layout
	•	Hosting + Deployment
