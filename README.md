# 🌾 AgriVision AI — AI Farmer Assistant

> **Smart Farming • Early Detection • Better Decisions**

AgriVision AI is an AI-powered agricultural assistant designed to help farmers identify crop diseases, understand possible treatments, access agricultural knowledge, and discover relevant government schemes through a simple and farmer-friendly web platform.

---

## 🚜 Problem Statement

Farmers may face difficulties in:

* 🌱 Identifying crop diseases at an early stage
* 📷 Understanding symptoms from crop/leaf images
* 💊 Finding reliable treatment information
* 🏛️ Discovering suitable government schemes and subsidies
* 📚 Accessing agricultural information from different sources
* 🗂️ Maintaining records of previous crop scans

These challenges can result in delayed decisions and potential crop losses.

---

## 💡 Our Solution

**AgriVision AI** brings multiple agricultural services together in one platform.

Farmers can:

* 📸 Upload a crop/leaf image
* 🤖 Get AI-assisted disease screening
* 📊 View prediction confidence and severity
* 📚 Access relevant disease knowledge
* 💊 View treatment/pesticide references
* 🏛️ Search government schemes and subsidies
* 🤝 Ask questions using the AI Farmer Assistant
* 👨‍🌾 Maintain a farmer profile
* 🗂️ View previous scan history

---

## ✨ Key Features

### 🌿 AI Crop Disease Detection

Upload a crop or leaf image and receive an AI-assisted prediction containing:

* Crop name
* Disease prediction
* Confidence score
* Severity information
* Alternative predictions

The system includes a confidence check so uncertain predictions can be flagged for confirmation.

### 🤖 AI Farmer Assistant

Farmers can ask questions related to:

* Crop diseases
* Symptoms
* Prevention
* Treatment
* Pest management
* Agricultural practices
* Scan results

### 📚 Agricultural Knowledge

The platform provides relevant information about detected diseases, including:

* Symptoms
* Causes
* Prevention
* Recommended next steps

### 💊 Treatment & Pesticide References

The platform provides available pesticide/product references and encourages farmers to verify current product labels and local agricultural guidance before application.

### 🏛️ Government Schemes

Farmers can search for agricultural schemes and support based on factors such as:

* State
* Crop
* Search keywords

### 🗂️ Scan History

Previous crop scans can be stored and reviewed by the farmer.

### 👨‍🌾 Farmer Profile

Users can maintain their agricultural profile and field/crop information.

### 🔐 Authentication

The application supports secure user authentication features including:

* Registration
* Login
* OTP verification
* Password recovery
* JWT-based authentication
* Password hashing

---

## 🏗️ System Architecture

```text
                 👨‍🌾 FARMER
                     │
                     ▼
          ┌─────────────────────┐
          │  AgriVision Frontend│
          │    HTML / CSS / JS  │
          └──────────┬──────────┘
                     │
                  REST API
                     │
                     ▼
          ┌─────────────────────┐
          │   Node.js + Express │
          │      Backend        │
          └───────┬───────┬─────┘
                  │       │
          ┌───────┘       └────────┐
          ▼                        ▼
 ┌─────────────────┐      ┌─────────────────┐
 │     Database    │      │   AI Inference  │
 │ SQLite / SQL    │      │ Plant Disease   │
 └─────────────────┘      │      Model      │
                          └─────────────────┘
```

---

## 🛠️ Technology Stack

### Frontend

* HTML5
* CSS3
* JavaScript

### Backend

* Node.js
* Express.js
* REST API

### Database

* SQLite

### AI

* Hugging Face Inference
* MobileNetV2-based plant disease identification model

### Security

* JWT
* bcrypt
* Helmet
* Rate limiting
* Input validation

### Communication

* Nodemailer
* Twilio (where configured)

---

## 📁 Project Structure

```text
AgriVision-AI/
│
├── frontend/
│   ├── index.html
│   ├── hack.html
│   └── ...
│
├── backend/
│   ├── src/
│   │   ├── server.js
│   │   ├── auth.js
│   │   ├── ai.js
│   │   ├── db.js
│   │   ├── knowledge.js
│   │   ├── mailer.js
│   │   └── seed.js
│   │
│   ├── data/
│   ├── uploads/
│   ├── package.json
│   ├── Dockerfile
│   └── .env.example
│
├── docs/
├── tests/
├── docker-compose.yml
└── README.md
```

---

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/AgriVision-AI.git
cd AgriVision-AI
```

### 2. Install Backend Dependencies

```bash
cd backend
npm install
```

### 3. Create Environment File

Copy `.env.example` to `.env`.

Windows:

```bash
copy .env.example .env
```

Linux/macOS:

```bash
cp .env.example .env
```

### 4. Configure Environment Variables

Example:

```env
JWT_SECRET=your-secure-secret
HF_TOKEN=your-huggingface-token
HF_MODEL=linkanjarad/mobilenet_v2_1.0_224-plant-disease-identification
```

Add email/SMS credentials if those services are enabled.

### 5. Seed Database

```bash
npm run seed
```

### 6. Start Backend

```bash
npm start
```

The backend will run locally at:



## 🌐 Deployment

AgriVision AI can be deployed using a separate frontend and backend hosting architecture.

```text
GitHub
   │
   ├── Frontend ──► Vercel
   │
   └── Backend ───► Render
                         │
                         ▼
                    AI + Database
```

### Production Configuration

The frontend should use the deployed backend API instead of:

```text
http://localhost:4000/api
```

Example:

```text
https://your-backend-url.onrender.com/api
```

---

## 🎯 Hackathon Demo Flow

```text
Farmer Login
     ↓
Farmer Profile
     ↓
Upload Crop Image
     ↓
AI Disease Screening
     ↓
Confidence + Severity
     ↓
Disease Knowledge
     ↓
Treatment References
     ↓
Government Schemes
     ↓
AI Farmer Assistant
     ↓
Scan History
```

---

## 🌍 Impact

AgriVision AI aims to make agricultural technology:

* **Accessible** — simple and farmer-friendly
* **Intelligent** — AI-assisted crop screening
* **Informative** — centralized agricultural knowledge
* **Action-oriented** — useful next-step guidance
* **Scalable** — expandable to more crops and diseases
* **Connected** — government-support discovery in one platform

---

## 🔮 Future Scope

* 📱 Android/iOS application
* 🌐 Regional Indian language support
* 🌦️ Real-time weather integration
* 🛰️ Satellite-based crop monitoring
* 🐛 Advanced pest detection
* 📈 Crop yield prediction
* 💰 Agricultural market-price information
* 📍 Location-based recommendations
* 👨‍🌾 Agronomist consultation
* 🧠 Models trained on more real-world Indian crop images

---

## ⚠️ Disclaimer

AgriVision AI provides **AI-assisted agricultural information and disease screening**.

AI predictions may not always be accurate, especially with real-world field images. Farmers should verify important disease diagnoses and treatment decisions with qualified agricultural experts and follow current product labels and applicable local regulations.

Government scheme information and agricultural product information may change and should be verified through official sources.



### Team :HEXANOVA




