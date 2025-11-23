<div align="center">

# Figma → Code in Seconds  
### The Ultimate Student Guide to Connect **Figma + Gemini CLI**

[![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)](https://figma.com)
[![Gemini](https://img.shields.io/badge/Gemini_CLI-8B5CF6?style=for-the-badge&logo=google-gemini&logoColor=white)](https://ai.google.dev)
[![Made for Students](https://img.shields.io/badge/Made_for-Students-10B981?style=for-the-badge)](https://github.com)

Turn any Figma design into **clean, production-ready code** — HTML, React, Tailwind, Next.js — in just one command!

</div>

---

### Step 1: Get Your Figma Personal Access Token (PAT)

1. Login → [figma.com](https://www.figma.com)
2. Click your avatar → **Settings**
3. Go to **Account** tab → Scroll to **Personal access tokens**
4. Tick **all permissions**
5. Click **Generate new token**
6. Name it → `Gemini CLI Access`
7. Generate → **COPY THE TOKEN RIGHT NOW** (no second chance!)

> Save it somewhere safe (like a notes app)

---

### Step 2: Connect Figma to Gemini CLI (One-Time Setup)

Open terminal and paste:

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN_HERE"
Example:
Bashgemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_x7k9p2m..."

Step 3: Verify Connection (Must Show Green)
Bashgemini mcp list
Success output:
BashConnected figma - Ready (8 tools available)

Step 4: Prepare Your Figma File (Super Important)

Open your design
Click Share → Anyone with the link can view
Select the frame you want → Right click → Copy link to selection

Example link:
texthttps://www.figma.com/design/xyz123/Dashboard?node-id=45-789

Step 5: Generate Code (The Magic Part!)
Basic HTML + CSS
Bashgemini "Convert this Figma frame to clean HTML and CSS: https://www.figma.com/design/xyz123/Dashboard?node-id=45-789"
React + Tailwind (Most Popular)
Bashgemini "Convert this frame to React with Tailwind CSS and make it fully responsive: [YOUR_LINK]"
Next.js + TypeScript
Bashgemini "Create a Next.js 14 component with TypeScript and Tailwind from this Figma frame: [LINK]"
Gemini automatically reads:
Colors • Spacing • Typography • Shadows • Layout • Images

Pro Example Prompts (Copy-Paste Ready)
Bash# React + Tailwind + Responsive + Dark Mode
gemini "Turn this Figma design into a beautiful React component using Tailwind CSS. Make it mobile-responsive and support dark mode: [LINK]"

# Full Landing Page (HTML)
gemini "Generate a complete responsive landing page with semantic HTML5 and modern CSS from this Figma file: [LINK]"

# Save files directly
gemini "Generate React + Tailwind code from [LINK] and save as Home.jsx and page.tsx"

Troubleshooting (Common Fixes)





















IssueFix"File could not be accessed"Make file public + use frame link (not file link)"Disconnected" or red dotRun: gemini mcp remove figma → redo Step 2Token not workingGenerate new token → copy without spaces

Final Checklist (Tick Karo!)

 Gemini CLI installed
 Figma PAT generated & copied
gemini mcp add command chalaya
gemini mcp list → green tick
 Figma file public + frame link copied
 Code generate kiya → boss level complete!


Bonus: Best Prompt Template (Save This!)
Bashgemini "Convert this Figma frame to [React/Next.js/HTML] using [Tailwind/Bootstrap/plain CSS]. Make it pixel-perfect, responsive, accessible, and production-ready: [PASTE_LINK_HERE]"


Made with love by
Mohsin Raza
Student • UI/UX + Frontend Ninja
LinkedIn
YouTube
Instagram
Figma → Code → Ship Fast → Get Hired
Ab design banane ke baad code likhne ki tension khatam!
