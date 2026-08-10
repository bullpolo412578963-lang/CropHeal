# CropHeal
🌿 CropHeal — AI Crop Disease Detection
Empowering farmers with instant, AI-driven leaf disease diagnosis and multilingual treatment plans.
CropHeal is a fully functional, single-file AgriTech web application designed to bridge the gap between complex agricultural science and everyday farmers. Featuring a beautiful nature-inspired glassmorphism UI, ambient animations, and a comprehensive remedy knowledge base, it allows users to upload or capture leaf photos, receive an instant diagnosis, and download professional PDF treatment reports.
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![LocalStorage](https://img.shields.io/badge/Storage-LocalStorage-green?style=for-the-badge)
---
✨ Key Features
📸 AI Disease Detection
Multi-input Scanning: Drag-and-drop, file browse, or live device camera capture.
On-Device Inference Engine: Uses advanced color-histogram and pixel-sampling analysis to detect necrosis (brown), chlorosis (yellow), and health (green) to classify leaves into 12 PlantVillage crop conditions.
Top-3 Predictions: Returns the most likely disease alongside confidence scores and alternative possibilities.
📖 Comprehensive Remedy Dossier
Deep agricultural data for every detected condition including:
Disease Description & Symptoms
Possible Causes & Prevention Methods
Organic vs. Chemical Treatments
Fertilizer & Pesticide Recommendations
Recovery Timelines & Safety Precautions
🌐 Multilingual Support
Full UI and remedy translation support for English and हिन्दी (Hindi).
Language preference is saved per user and applied to generated PDF reports.
📊 Farmer Dashboard & Analytics
Visual Analytics: 7-day scan activity charts and Healthy vs. Diseased pie charts.
Live Weather Integration: Fetches real-time temperature, humidity, wind, and rain probability based on the farmer's registered district using the Open-Meteo API.
Scan History: Chronological log of all past predictions with one-click PDF generation.
🛡️ Admin Panel
User Management: View, toggle roles, or delete registered farmers.
Knowledge Base Editor: Admins can dynamically update symptoms, remedies, and organic treatments for all 12 crop classes without touching the source code.
Dataset Overview: Monitor the embedded PlantVillage classes.
🎨 Ambient Nature UI
Custom SVG cherry blossom trees with falling petals, swaying grass, floating pollen, and butterflies.
Glassmorphism cards, smooth scroll-reveal animations, and a calming green/cream color palette designed for outdoor visibility.
---
🚀 Getting Started
Because CropHeal is built as a single-file application, no build steps, npm installs, or backend servers are required to run the demo.
Save the Code: Save the provided HTML code as `index.html`.
Open in Browser: Double-click the file or open it in any modern web browser (Chrome, Safari, Edge, Firefox).
Select Language: Choose your preferred interface language (English or Hindi) on the welcome modal.
Start Scanning: Navigate to Disease Detection and upload a leaf photo!
🔑 Default Admin Credentials
To access the Admin Panel and edit the remedy knowledge base, log in with the pre-seeded admin account:
Email: `admin@cropheal.in`
Password: `Admin@123`
---
🗺️ Application Routes
The app uses a custom hash-based router (`#/route`):
Route	Description
`#/home`	Landing page with feature highlights and ambient background.
`#/detect`	The core AI scanner with drag-and-drop/camera upload.
`#/dashboard`	Farmer's personal analytics, weather widget, and quick actions.
`#/history`	Searchable log of past scans with PDF download links.
`#/profile`	Multi-step farmer registration and profile editing.
`#/admin`	Restricted area for managing users and the remedy database.
---
⚙️ Tech Stack & Architecture
Frontend: Vanilla ES6+ JavaScript, HTML5, CSS3.
Styling: Custom CSS variables, Glassmorphism (`backdrop-filter`), CSS Keyframe animations.
State Management: Custom `localStorage` wrapper (`DB` object) for persisting users, sessions, predictions, and admin overrides.
PDF Generation: `jsPDF` (loaded via CDN) with a print-window fallback.
APIs:
`Open-Meteo` (Geocoding & Weather Forecasting).
`Unsplash` (Ambient background imagery).
AI Engine: Note: As a single-file frontend demo, the AI relies on an on-device heuristic algorithm (evaluating RGB pixel ratios for brown/yellow/green dominance) mapped to a deterministic hash to simulate CNN inference.
---
🌱 The 12 Supported Crop Classes
The embedded knowledge base covers the following PlantVillage dataset classes:
Tomato (Late Blight, Early Blight, Leaf Mold, Healthy)
Potato (Late Blight, Early Blight)
Corn / Maize (Northern Leaf Blight, Common Rust)
Apple (Apple Scab, Black Rot)
Bell Pepper (Bacterial Spot)
Grape (Black Rot)
---
🔮 Production Vision (Full-Stack)
This single-file build serves as a fully interactive UI/UX prototype and frontend logic demonstration. A production deployment would involve:
Backend: Node.js/Express or Python/FastAPI for secure authentication and database management (PostgreSQL/MongoDB).
True AI Model: Replacing the heuristic color-analysis with a real MobileNetV2 or ResNet TensorFlow.js/ONNX model trained on the PlantVillage dataset for actual image classification.
Cloud Storage: AWS S3 or Firebase for storing user leaf images.
---
📄 License
This project is a conceptual AgriTech prototype. Feel free to fork, modify, and use it for agricultural hackathons, school projects, or open-source AgriTech initiatives.
Grown with 💚 for farmers.
