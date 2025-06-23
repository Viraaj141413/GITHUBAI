✅ GOAL: Full In-Browser Replit-Like AI IDE (Single HTML)
The IDE should:

Run fully in-browser (index.html)

Support creating/editing any file type: .ts, .tsx, .js, .jsx, .html, .css, .py, etc.

Let users describe what they want to build

Auto-create starter projects based on the description

Use Claude 3 Sonnet API as the assistant agent

Have an AI-only console (hidden from users)

Auto-detect and load JS/Python libraries dynamically

Show live previews for frontend code

🧾 FINAL AI PROMPT (Use This With Claude or ChatGPT)
Build a complete in-browser AI IDE like Replit as a single HTML file (index.html).

🔧 Core Requirements:
The entire app should run in-browser with React 18 + Babel (via CDN).

Include a project description input where the user describes what they want to build (e.g. “Todo app in React with local storage”).

Based on the description, the AI assistant should:

Detect the project type (React, Node, Python, Static Site, etc.)

Generate a file tree with appropriate starter files (index.html, App.tsx, main.py, etc.)

Build a file explorer with create/edit/delete support for any file type:

Support .js, .jsx, .ts, .tsx, .html, .css, .py, .json, etc.

Add a code editor (can use CodeMirror, Ace, or simple textarea) that supports syntax highlighting.

Include a live preview pane for frontend projects that auto-reloads on file save.

🧠 AI Assistant (Claude 3 Sonnet):
Include an AI chat sidebar powered by the Claude API (use a placeholder for the API key).

When the user asks for changes (e.g. “add a new React component”), the AI should:

Read all files and the console log

Reply with explanations and full code updates or new file contents

Wire AI responses to modify the actual file content in the IDE.

Claude should only see the console log internally.

🖥 Console (Hidden from User):
Hijack all console.log, console.error, etc., and store them in a hidden buffer.

This console output is not shown to users, but should be visible to the AI when it generates a response.

📦 Dependency Installation:
For JS/TS/React:

Detect import or require statements in JS/TS files.

Auto-inject <script src="https://unpkg.com/[pkg]"> for each package.

For Python:

Use Pyodide to run Python in the browser.

Use micropip to install packages (e.g., pandas, requests).

Console output from Pyodide should also be sent to the AI.

💡 Supported Languages:
JavaScript (.js)

TypeScript (.ts)

React (.jsx, .tsx)

HTML/CSS

Python (.py)

JSON, text, config files

⚙️ Technologies to Use:
React 18 via CDN

Babel for JSX/TSX

Lucide or Heroicons for icons

Pyodide for Python runtime

CodeMirror or Ace Editor (optional)

Modern responsive layout with Tailwind or vanilla CSS

🧪 Testing:
All code runs in-browser

No backend/server required

Claude modifies files, adds new features, and can read logs

Keep everything in one single HTML file. No external servers or Node.js required.
