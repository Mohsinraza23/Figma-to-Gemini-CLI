# 🎨✨ Connecting Figma to Gemini CLI — Student Guide

A **complete step-by-step guide** to convert your Figma designs into clean, production-ready code using **Gemini CLI**.

---

## 🔑 Step 1: Generate Figma Personal Access Token (PAT)

1. Go to [figma.com](https://www.figma.com) and log in  
2. Click your **Profile Icon** → **Settings**  
3. Open the **Account** tab  
4. Scroll down to **Personal access tokens**  
5. Tick **all checkboxes** (required for full access)  
6. Click **Generate new token**  
7. Name it (e.g. `Gemini CLI Access`)  
8. Click **Generate token**  
9. ⚠️ **Copy the token immediately** — you won’t see it again!

---

## 🔗 Step 2: Connect Figma MCP Server to Gemini CLI

Open your terminal and run:

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN_HERE"
Example:
Bashgemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_abc123xyz789"

🟢 Step 3: Verify the Connection
Bashgemini mcp list
You should see:
Bash🟢 figma - Ready (8 tools, 1 prompt)

📁 Step 4: Prepare Your Figma File
Make the file public

Open your file → Click Share (top-right)
Set to “Anyone with the link can view”
Copy the link

Copy the exact Frame link

Select the frame you want to convert
Right-click → Copy link to selection

Example link:
texthttps://www.figma.com/design/abc123/MyProject?node-id=1-23&t=45567

🧩 Step 5: Generate Code from Figma
Just run this command (replace the link with yours):
Bashgemini "Get the design context from [PASTE_YOUR_FIGMA_LINK_HERE] and generate HTML and CSS"
Real example:
Bashgemini "Get the design context from https://www.figma.com/design/abRnucBMTsgblvDB6ymtd1/Hospital-Design?node-id=1-218 and generate HTML and CSS"
Gemini will automatically:

Fetch layout, colors, typography, spacing, shadows, etc.
Output clean, production-ready code directly in your terminal


🎛️ Step 6: Optional — Customize the Output

























GoalPrompt ExampleReact + Tailwindgemini "Get design context from [LINK] and generate React components with Tailwind CSS"Responsive HTML/CSSgemini "Use get_design_context on [LINK] and create mobile-responsive HTML and CSS"Next.js + TypeScriptgemini "Create a Next.js page/component from [LINK] using TypeScript and Tailwind"Vue 3gemini "Generate a Vue 3 component with Composition API from [LINK]"

🧰 Quick Troubleshooting





















ProblemSolution“This figma file could not be accessed”• Set file to Anyone with the link can view
• Use a file you own
• Test with a public Community fileFigma shows “Disconnected”bash<br>gemini mcp remove figma<br>
then re-run Step 2Token issuesGenerate a new token → copy without spaces → reconnect

✅ Summary Checklist

 Install Gemini CLI
 Create Figma Personal Access Token
 Connect Figma MCP (gemini mcp add …)
 Verify: gemini mcp list shows figma - Ready
 Make Figma file public + copy frame link
 Run the magic command:Bashgemini "Get design context from [LINK] and generate code"
 Save & use your code!


🛠️ Available Figma Tools (for advanced prompts)





































ToolPurposeget_design_contextExtract full design structureget_screenshotCapture design previewget_metadataGet variables + stylesget_variable_defsExtract design tokensget_code_connect_mapMap components to codeget_figjamAccess FigJam contentwhoamiVerify account

💡 Tips for Best Results

Be very specific in your prompts
Mention the framework/library you want (Tailwind, React, Next.js, etc.)
Convert one frame at a time
Ask Gemini to make the code responsive, accessible, etc.
You can even say: “also save the code as index.html and style.css”


🚀 Ready-to-Use Example Prompts
Bash# Simple HTML + CSS
gemini "Get design context from [LINK] and generate semantic HTML5 with modern CSS"

# React + Tailwind (responsive)
gemini "Convert this Figma frame to React: [LINK]. Use Tailwind CSS and make it fully responsive"

# Next.js + TypeScript
gemini "Create a Next.js component from [LINK] with TypeScript and Tailwind CSS"

# Vue 3
gemini "Generate a Vue 3 component with Composition API and Tailwind from [LINK]"

📬 Need Help?

Figma MCP Docs → https://mcp.figma.com
Gemini CLI Docs → (ask your instructor)
Just ping your instructor!


🌐 My Socials
🔗 LinkedIn: https://www.linkedin.com/in/mohsin-raza-a514392b6
▶️ YouTube: https://youtube.com/@YourChannel
📘 Facebook: https://facebook.com/yourpage

🎉 Happy Coding!
You’re now ready to turn any Figma design → production-ready code in seconds!
Figma → Code → Ship it! 🚀
textCopy-paste kar do ye pura content apne `README.md` mein — bilkul clean aur professional dikhega GitHub par
