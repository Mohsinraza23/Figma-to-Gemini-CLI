# 🎨 Figma → Code with Gemini CLI  
### Official Student Guide (2025)

Turn your **Figma designs into production-ready code** instantly using **Google Gemini CLI**.

Supported Output:
**HTML • CSS • React • Tailwind • Next.js • Vue • TypeScript • Responsive • Dark Mode**

---

## 🚀 Prerequisites

- Gemini CLI installed  
- Figma account (Free works great)  
- Basic Terminal knowledge  

---

# 🥇 Step 1 — Generate Figma Personal Access Token (PAT)

1. Open Figma → Settings  
2. Go to **Account**  
3. Open **Personal Access Tokens**  
4. Click **Generate new token**  
5. Enable **all permissions**  
6. Copy your PAT safely  

⚠️ **Never upload your PAT to GitHub.**

---

# 🔗 Step 2 — Connect Figma to Gemini CLI

Run this in your terminal:

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN"
Example:

bash
Copy code
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_xxxxxxxx"
🧪 Step 3 — Verify Connection
bash
Copy code
gemini mcp list
Output should be:

arduino
Copy code
🟢 figma - Ready (8 tools available)
📝 Step 4 — Prepare Your Figma File
✔ Give Permission
Set → Anyone with the link · Can view

✔ Copy Frame Link (IMPORTANT)
Right-click your design frame →
Copy link to selection

Example:

ruby
Copy code
https://www.figma.com/design/abc123/Project?node-id=45-678
This ensures Gemini gets the exact frame.

⚡ Step 5 — Convert Figma Design to Code
HTML + CSS
bash
Copy code
gemini "Convert this Figma frame to clean HTML + modern CSS: [LINK]"
React + Tailwind
bash
Copy code
gemini 'Generate a responsive React + Tailwind component from this design: [LINK]'
Next.js + TypeScript + Tailwind
bash
Copy code
gemini 'Create a full Next.js 14 page (TS + Tailwind + App Router) from: [LINK]'
Vue 3 + Tailwind
bash
Copy code
gemini 'Build a Vue 3 component using Tailwind from this frame: [LINK]'
🔧 Figma Tools Available
Tool	Purpose
get_design_context	Extract layout, colors, spacing
get_screenshot	Capture frame screenshot
get_metadata	File info + styles
get_variable_defs	Design tokens
whoami	Connected account details

🐞 Troubleshooting
Problem	Fix
File not accessible	Set sharing: Anyone with link → Can view
Token error	Generate PAT with all permissions
Wrong frame	Always copy link to selection
Connection broken	gemini mcp remove figma → reconnect

💡 Best Practices
Select single frame

Use mobile-first instructions

Add in prompts:

"Make it responsive"

"Use Tailwind dark mode classes"

"Add accessibility (aria-labels)"

Ask Gemini to save files with names:
→ Create Header.tsx and styles.css

📌 Ready-To-Use Prompts
bash
Copy code
gemini "Create a responsive landing page in React + Tailwind using modern UI patterns from this frame: [LINK]"
bash
Copy code
gemini "Convert this card UI into HTML + Tailwind with hover animations: [LINK]"
bash
Copy code
gemini "Generate a complete Next.js 14 TS page with App Router from this frame: [LINK]"
📑 Final Checklist
 Gemini CLI installed

 Figma PAT generated

 Connected via MCP

 File shared publicly

 Correct frame link copied

 Code generated successfully

🔗 Resources
Gemini CLI Docs → https://ai.google.dev/gemini-api/docs/cli

Figma MCP Docs → https://mcp.figma.com

Gemini API → https://ai.google.dev

👤 Author — Mohsin Raza
Connect With Me
LinkedIn: https://www.linkedin.com/in/mohsin-raza-a514392b6

⚡ Figma → Code in 10 seconds. Not 10 hours.
yaml
Copy code

---
