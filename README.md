# 📌 AI Post Generator Agent

## 🔹 Project Title
AI‑Based Social Media Post Generator with Google Gemini Integration

## 🔹 Problem Statement
Brands and individuals spend significant time creating social media content. Posts often become repetitive and inconsistent across platforms. This project automates content generation using AI.

## 🔹 Objective
Generate platform‑specific posts (LinkedIn, Twitter, Instagram) from a single topic input, with summaries, captions, hashtags, and polished outputs.

## 🔹 AI Agent Explanation
The agent uses Google Gemini APIs to:
- Summarize input topics
- Generate draft posts for multiple platforms
- Polish posts to match platform tone and style

## 🔹 Features
- Topic‑based content generation
- Research summary
- LinkedIn, Twitter, Instagram posts
- Copy‑to‑clipboard functionality
- Avoids repetitive content

## 🔹 How the Agent Works
1. User enters a topic in the frontend UI.  
2. Backend (`/generate-posts`) processes the topic.  
3. Gemini API generates summary + raw posts.  
4. Posts are polished and returned to frontend.  
5. UI displays results with copy buttons.

## 🔹 Architecture / Workflow
- **Frontend:** HTML/JS interface (`frontend/index.html`)  
- **Backend:** Node.js + Express (`agent/index.js`)  
- **API:** Google Gemini (Generative Language API)  
- **Flow:** Input → Backend → Gemini → Output → UI  

## 🔹 Technology Stack
- Node.js  
- Express.js  
- Axios  
- Google Gemini API  
- HTML/CSS/JavaScript  

## 🔹 Folder Structure
```
Ai-Post-Generator-Agent-master/
│
├── agent/                         # Backend folder
│   ├── node_modules/              # Installed dependencies
│   ├── .env                       # Environment variables (GOOGLE_API_KEY, PORT)
│   ├── .gitignore                 # Ignored files for Git
│   ├── index.js                   # Main backend server file
│   ├── package.json               # Project metadata and dependencies
│   ├── package-lock.json          # Dependency lock file
│
├── frontend/                      # Frontend folder
│   ├── index.html                 # Main UI file (HTML, CSS, JS)
│
├── Screenshots/                   # Output examples folder
│   ├── Output1.jpeg               # Complete UI layout with results
│   ├── Output2.jpeg               # Topic input and Generate button
│   ├── Output3.jpeg               # AI-generated research summary
│   ├── Output4.jpeg               # LinkedIn, Twitter, Instagram post outputs
│
└── README.md                      # Project documentation

```

## 🔹 Prerequisites
- Node.js v18+  
- npm (comes with Node.js)  
- Google Gemini API key  

## 🔹 Node.js Installation
Download from [Node.js official site](https://nodejs.org).

## 🔹 Project Installation
```bash
cd agent
npm install
```

## 🔹 .env Creation
Create `.env` inside `agent/`:
```env
GOOGLE_API_KEY=your_api_key_here
PORT=3000
```

## 🔹 API‑Key Configuration
Generate your Gemini API key from Google Cloud console and paste into `.env`.

## 🔹 Exact Commands to Start Backend
```bash
cd agent
npm start
```
Backend runs at: `http://localhost:3000`

## 🔹 Exact Steps to Open Frontend
```bash
cd frontend
start index.html
```
Frontend opens in your default browser.

## 🔹 How to Use the UI
- Enter a topic in the input box.  
- Click **Generate Posts ✨**.  
- View summary + posts for LinkedIn, Twitter, Instagram.  
- Copy posts using the provided buttons.

## 🔹 Input Format
```json
{
  "topic": "Artificial Intelligence in Healthcare"
}
```

## 🔹 API Endpoint
`POST http://localhost:3000/generate-posts`

## 🔹 Request / Response Flow
- **Request:** `{ "topic": "your subject" }`  
- **Response:**  
  ```json
  {
    "summary": "...",
    "rawPosts": { "linkedin": "...", "twitter": "...", "instagram": "..." },
    "polishedPosts": "..."
  }
  ```

## 🔹 Sample Input
```
Topic: Sustainable Fashion
```

## 🔹 Sample Output
```
Summary: 4–5 bullet points
LinkedIn: Professional post
Twitter: Punchy <280 characters
Instagram: Friendly caption with emojis
```

## 🔹 Expected Screenshots / Placeholders
- Input form screenshot  
- Output posts screenshot  

## 🔹 Error Handling
- Invalid API key → error message  
- Empty topic → prompt user  
- Server errors → JSON `{ "error": "Something went wrong" }`

## 🔹 Design Decisions
- No database → lightweight setup  
- Tavily removed → simplified workflow  
- Gemini chosen → strong text generation

## 🔹 Limitations
- No persistent storage  
- Limited to text generation only  

## 🔹 Future Improvements
- Database integration  
- Auto‑posting to platforms  
- Analytics dashboard  

## 🔹 Testing
Run backend with sample topics, verify outputs in UI.

## 🔹 Troubleshooting
- Ensure Node.js v18+ installed  
- Verify `.env` API key  
- Run `npm install` before `npm start`  

## 🔹 Challenge‑Specific Deliverables
- Working backend + frontend  
- Clear documentation  
- Screenshots of execution  

## 🔹 Trade‑offs
- Simplicity vs scalability  
- No DB → faster setup but limited persistence  

## 🔹 Submission Checklist
✅ README updated  
✅ Backend runs with `npm start`  
✅ Frontend opens with `index.html`  
✅ Gemini API integrated  
✅ Sample input/output tested  
✅ Screenshots included  
```
## 📸 Screenshots

All output examples are available in the `Screenshots/` folder.

- `Screenshots/Output1.jpeg` → Complete UI layout with results
- `Screenshots/Output2.jpeg` → Topic input and Generate button  
- `Screenshots/Output3.jpeg` → AI‑generated summary section  
- `Screenshots/Output4.jpeg` → LinkedIn, Twitter, and Instagram post outputs  
