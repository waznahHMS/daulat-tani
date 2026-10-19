# 🌾 Daulat Tani
**Live Demo:** [https://daulat-tani-farming-2f7k.bolt.host](https://daulat-tani-farming-2f7k.bolt.host)

Daulat Tani (Blessed Farmer) is an offline-first, zero-backend Progressive Web App designed to be a "plant doctor in the pocket" for smallholder padi (rice) farmers in Brunei. 

## 1. Problem Statement and Solution
**Problem:** Smallholder farmers in Brunei lose up to 30% of their harvest to preventable crop diseases (like Padi Blast). The nearest agricultural expert is often hours away, and rural farms lack reliable 4G internet to use cloud-based farming apps. By the time a farmer visually identifies a disease, the crop is lost.
**Solution:** Daulat Tani is a fully client-side PWA. Farmers can scan a leaf with their camera to get an instant diagnosis with organic remedy dosages, ask a voice/text AI advisor questions in English or Malay, and export PDF reports—all 100% offline, with data kept privately on their device.

## 2. Technology Stack
* **Framework:** React 18 + Vite
* **Language:** TypeScript (Strict mode)
* **Styling:** Tailwind CSS (using explicit hex arbitrary values for the NYLP Hackathon theme)
* **Icons:** Lucide-React
* **PDF Generation:** jsPDF
* **Hosting:** Bolt.host
* **Database/Backend:** None. All state is managed locally via `localStorage`.

## 3. Setup and Installation Instructions
To run this project locally:
1. Clone the repository: `git clone <your-repo-url>`
2. Navigate into the directory: `cd daulat-tani`
3. Install dependencies: `npm install`
4. Start the development server: `npm run dev`
5. Open `http://localhost:5173` in your browser. *(Note: Camera features require HTTPS or localhost).*

## 4. AI Methodology and Implementation
The app features **Two AI Cores** designed to run with zero external API dependencies:
* **Padi Sense (Multi-Modal Diagnostic Engine):** Instead of a simple image classifier, it uses a deterministic weighted scoring algorithm. It combines the image capture data with the user's selected district (e.g., Tutong vs. Temburong) and micro-climate data to output a severity score and region-specific organic remedy. 
* **Suara Tani (Offline NLP):** A lightweight, browser-based natural language intent classifier. It normalizes text (English/Malay), strips stopwords, and matches user queries (e.g., "How to stop leaf blight?") against a pre-defined agricultural corpus to generate localized advice offline.

## 5. AI Model Names and API Usage
**There are NO external AI APIs (like OpenAI, Gemini, or Anthropic) used in this project.** 
To ensure the app works in zero-connectivity rural areas, all "AI" logic is executed locally in the browser using pure TypeScript algorithms (TF-IDF matching and weighted multi-modal scoring). There are zero API keys exposed.

## 6. Product Screenshots
*Please see the main dashboard in Guest Mode:*
*(Add 2-3 screenshots here showing the Camera, the Diagnosis Card, and the PDF Export)*

## 7. Team Member Contributions
**Waznah binti Haji Mohd Sallehin - Solo Developer**
* Conceptualized the "Pak Haji Rosli" user story and SDG alignment (SDG 2 & 13).
* Designed the "Daulat Tani" brand identity and NYLP-aligned UI design system.
* Engineered the entire React frontend, local authentication system, and offline AI algorithms.
* Built the jsPDF export functionality and integrated the camera media streams.
