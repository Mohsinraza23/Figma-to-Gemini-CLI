🎨✨ Connecting Figma to Gemini CLI — Student Guide

A complete step-by-step guide to convert your Figma designs into clean, production-ready code using Gemini CLI.

🔑 Step 1: Generate Figma Personal Access Token (PAT)

Go to Figma.com and log in

Click your Profile Icon → Settings

Open the Account tab

Scroll to Personal Access Tokens

Tick all checkboxes (required for access)

Click Generate new token

Name it (Example: Gemini CLI Access)

Click Generate token

⚠️ Copy the token immediately — you won’t see it again!

🔗 Step 2: Connect Figma MCP Server to Gemini CLI

Open your terminal and run:

gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN_HERE"


Example:

gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_abc123xyz789"

🟢 Step 3: Verify Connection
gemini mcp list


You should see:

🟢 figma - Ready (8 tools, 1 prompt)

📁 Step 4: Prepare Your Figma File
Make File Public:

Open your file

Click Share

Set to “Anyone with the link can view”

Copy the link

Copy Frame Link:

Select your frame

Right-click → Copy link to selection

Example:

https://www.figma.com/design/abc123/MyProject?node-id=1-23&t=45567

🧩 Step 5: Generate Code from Figma

Run:

gemini "Get the design context from [PASTE_YOUR_FIGMA_LINK] and generate HTML and CSS"


Real example:

gemini "Get the design context from https://www.figma.com/design/abRnucBMTsgblvDB6ymtd1/Hospital-Design?node-id=1-218 and generate HTML and CSS"

What Gemini does:

Fetches Figma layout

Reads colors, text, spacing, shadows

Generates clean HTML + CSS

Shows code in terminal

🎛️ Step 6: Optional — Customize Output

React + Tailwind:

gemini "Get design context from [LINK] and generate React components with Tailwind CSS"


Responsive HTML:

gemini "Use get_design_context on [LINK] and create mobile-responsive HTML and CSS"

🧰 Quick Troubleshooting
❌ Problem: “This figma file could not be accessed”

✔ Set file to Anyone can view
✔ Correct PAT permissions
✔ Try with file you own
✔ Test with a public Figma Community file

❌ Figma shows “Disconnected”

Fix:

gemini mcp remove figma


Re-add using Step 2
Verify again:

gemini mcp list

❌ Token issues

✔ Generate new token
✔ Copy correctly (no spaces)
✔ Reconnect

✅ Summary Checklist

Install Gemini CLI

Create Figma PAT Token

Connect Figma MCP

Verify connection: gemini mcp list

Share Figma file

Copy frame link

Run:

gemini "Get design context from [LINK] and generate code"


Save and use your code

🛠️ Available Figma Tools
Tool	Purpose
get_design_context	Extract full design structure
get_screenshot	Capture design preview
get_metadata	Get variables + styles
get_variable_defs	Extract design tokens
get_code_connect_map	Map components to code
get_figjam	Access FigJam content
whoami	Verify account
💡 Tips for Best Results

Be specific in prompts

Mention UI libraries (Tailwind, React, Next.js)

Convert one frame at a time

Refine output with better instructions

Ask Gemini to save code in files

🚀 Example Prompts

HTML + CSS:

gemini "Get design context from [LINK] and generate semantic HTML5 and modern CSS"


React + Tailwind:

gemini "Convert this Figma frame to React: [LINK]. Use Tailwind CSS and make it responsive"


Next.js + TypeScript:

gemini "Create a Next.js component from [LINK] with TypeScript and Tailwind"


Vue 3:

gemini "Generate a Vue 3 component with Composition API from [LINK]"

📬 Need Help?

Figma MCP Docs

Gemini CLI Docs

Ask your instructor

🌐 My Social Links

🔗 LinkedIn:
https://www.linkedin.com/in/mohsin-raza-a514392b6

▶️ YouTube:
https://youtube.com

📘 Facebook:
https://facebook.com

🎉 Happy Coding!

You're now ready to convert Figma designs → Production Code effortlessly!
