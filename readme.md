<!-- Banner -->
<p align="center">
  <img src="https://i.ibb.co/8xDjH3P/figma-gemini-banner.png" width="100%" />
</p>

<h1 align="center">🎨 Figma → Code with Gemini CLI  
<br>⚡ Official Student Guide (2025)</h1>

<p align="center">
  Convert your <b>Figma designs → HTML, CSS, React, Tailwind, Next.js, Vue, TypeScript</b> instantly using <b>Google Gemini CLI</b>.
  <br>No more manual coding — just select → paste link → generate code.
</p>

---

## 🚀 Tech Supported

<p align="center">
  <img src="https://skillicons.dev/icons?i=figma,html,css,react,tailwind,nextjs,ts,js,vscode,github" />
</p>

---

## 🛠 Prerequisites

- Install **Gemini CLI**  
- Have a free **Figma account**  
- Basic knowledge of terminal  

---

# 🥇 Step 1 — Generate Figma Personal Access Token (PAT)

1. Open **Figma → Settings**  
2. Scroll to **Account**  
3. Go to **Personal Access Tokens**  
4. Click **Generate new token**  
5. Check **all permissions**  
6. Copy token safely!

> ⚠ WARNING: Never upload your token to GitHub!

---

# 🔗 Step 2 — Connect Figma → Gemini CLI

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN"
✔ Replace YOUR_TOKEN with your actual PAT.

Example:

bash
Copy code
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_xxxxxxxxxxxxx"
💡 Step 3 — Verify Connection
bash
Copy code
gemini mcp list
You should see:

bash
Copy code
🟢 figma – Ready (8 tools available)
📝 Step 4 — Prepare Figma File
✔ Share Permissions
Set → Anyone with the link → Can view

✔ Correct Link (IMPORTANT!)
Right-click your Frame →
Copy link to selection (this adds node-id)

Example:

ruby
Copy code
https://www.figma.com/design/abc123/Project?node-id=45-678
⚡ Step 5 — Convert Figma → Code (MAGIC ✨)
🔵 HTML + CSS
bash
Copy code
gemini "Convert this Figma frame to clean HTML + modern CSS: [LINK]"
🟣 React + Tailwind (Best)
bash
Copy code
gemini "Generate a responsive React + Tailwind component from this design: [LINK]"
🟢 Next.js 14 + TypeScript
bash
Copy code
gemini "Create a full Next.js TS page with Tailwind from: [LINK]"
🔥 Vue 3 + Composition API
bash
Copy code
gemini "Build a Vue 3 component using Tailwind from this frame: [LINK]"
🧩 Available Figma Tools
Tool	Purpose
get_design_context	Colors, spacing, layout, typography
get_screenshot	Image of frame
get_metadata	File + styles info
get_variable_defs	Design tokens & variables
whoami	Connected account info

🔧 Common Errors & Fixes
Error	Solve it by…
File not accessible	Set Figma → Anyone with link can view
Token error	Generate PAT with all permissions
Wrong frame	Use Copy link to selection only
Connection issue	gemini mcp remove figma → reconnect

💎 PRO Tips for Best Output
Always use single frame

Add this in prompts:

“Make it responsive mobile-first”

“Use Tailwind dark mode classes”

“Add aria-label accessibility”

Save with file names:
→ “…and save as Header.tsx + styles.css”

📌 Ready-To-Use Prompts
bash
Copy code
gemini "Create a responsive landing page in React + Tailwind using modern UI patterns from this frame: [LINK]"
bash
Copy code
gemini "Convert this card UI into HTML + Tailwind with hover animations: [LINK]"
bash
Copy code
gemini "Generate a complete Next.js 14 TS page with App Router from: [LINK]"
🧾 Final Checklist (Do This!)
✔ Gemini CLI installed
✔ Figma PAT generated
✔ Connected via MCP command
✔ File shared publicly
✔ Frame link copied
✔ Code generated successfully

🔗 Resources
Gemini CLI → https://ai.google.dev/gemini-api/docs/cli

Figma MCP → https://mcp.figma.com

Gemini API → https://ai.google.dev

👨‍💻 Author – Mohsin Raza
<p align="center"> <img src="https://i.ibb.co/m5Lq88V/programmer.gif" width="320" /> </p>
📫 Connect With Me
<p align="left"> <a href="https://www.linkedin.com/in/mohsin-raza-a514392b6"> <img src="https://img.shields.io/badge/LinkedIn-Mohsin%20Raza-blue?style=for-the-badge&logo=linkedin" /> </a> <a href="https://youtube.com/@yourchannel"> <img src="https://img.shields.io/badge/YouTube-Subscribe-red?style=for-the-badge&logo=youtube" /> </a> <a href="https://facebook.com/yourprofile"> <img src="https://img.shields.io/badge/Facebook-Profile-blue?style=for-the-badge&logo=facebook" /> </a> </p>
<p align="center"><b>⚡ Figma → Code in 10 seconds. Not 10 hours. ⚡</b></p> <p align="center">Built with ❤️ for Developers & Students</p> ```
