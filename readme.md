📌 README.md — Connecting Figma to Gemini CLI (Student Guide)

By Mohsin Raza

🔗 My Social Links

LinkedIn: https://www.linkedin.com/in/mohsin-raza-a514392b6

YouTube: (link dedo, main update kar dunga)

Facebook: (link dedo, main update kar dunga)

🚀 Connecting Figma to Gemini CLI

A step-by-step guide to convert your Figma designs into clean, production-ready code using Gemini CLI.

📍 Step 1: Generate Figma Personal Access Token (PAT)

Go to Figma.com and log in

Click your profile icon (top-right corner)

Select Settings

Go to the Account tab

Scroll down to Personal Access Tokens

Make sure all checkboxes are ticked (important!)

Click Generate new token

Give the token a name (e.g., "Gemini CLI Access")

Click Generate token

⚠️ Copy the token immediately — you won’t see it again!

Save it somewhere safe

📍 Step 2: Connect Figma MCP Server to Gemini CLI

Run this command in terminal:

gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN_HERE"


Replace:

YOUR_TOKEN_HERE


with your actual Figma token.

✔ Example
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_abc123xyz789"

📍 Step 3: Verify Connection

Check if Figma MCP connected successfully:

gemini mcp list


You should see:

🟢 figma - Ready (8 tools, 1 prompt)


If yes → You're all set! ✅

📍 Step 4: Prepare Your Figma File
Make Your File Accessible

Open your Figma design file

Click Share (top-right)

Set permissions to:

Anyone with the link can view


Copy the link

Copy Frame Link

Select your frame

Right-click

Click Copy link to selection

Save this link

Example format:

https://www.figma.com/design/abc123/MyProject?node-id=1-23&t=45567

📍 Step 5: Generate Code from Figma Design

Use this command:

gemini "Get the design context from [PASTE_YOUR_FIGMA_LINK] and generate HTML and CSS"

✔ Real Example:
gemini "Get the design context from https://www.figma.com/design/abRnucBMTsgblvDB6ymtd1/Hospital-Design?node-id=1-218 and generate HTML and CSS"

🔥 What Gemini Does:

Fetches design structure

Extracts colors, text, spacing, layout

Generates clean HTML and CSS

Displays code in your terminal

📍 Step 6: Customize Output (Optional)
🔹 For React Components:
gemini "Get design context from [YOUR_LINK] and generate React components with Tailwind CSS"

🔹 For Responsive HTML/CSS:
gemini "Use get_design_context on [YOUR_LINK] and create mobile-responsive HTML and CSS"

🚨 Quick Troubleshooting
❌ Problem: "This figma file could not be accessed"

✔ Solutions:

Ensure file is shared as "Anyone with the link can view"

Check PAT permissions

Try with your own file

Try a public Figma Community file

❌ Problem: Figma shows as "Disconnected"

Remove connection:

gemini mcp remove figma


Reconnect using Step 2 command
Verify:

gemini mcp list

❌ Problem: Token doesn’t work

✔ Generate a new token
✔ Remove spaces
✔ Reconnect again

📦 Summary Checklist

✔ Install Gemini CLI
✔ Create Figma PAT token
✔ Connect Figma to Gemini (gemini mcp add)
✔ Verify (gemini mcp list)
✔ Share Figma file publicly
✔ Copy frame link
✔ Run Gemini command
✔ Save and use generated code

🛠 Available Figma Tools
Tool	Purpose
get_design_context	Main tool – extracts design structure
get_screenshot	Gets visuals of design
get_metadata	Fetches file info, styles, variables
get_variable_defs	Extracts design tokens
get_code_connect_map	Connects components to code
get_figjam	Access FigJam content
whoami	Verify your Figma account
🌟 Tips for Best Results

Be specific about framework/language

Use clear prompts (responsive, Tailwind, etc.)

Convert one frame at a time

Refine output with iterative prompts

Ask Gemini CLI to save code to files

🧩 Example Prompts
🔹 HTML/CSS
gemini "Get design context from [LINK] and generate semantic HTML5 and modern CSS"

🔹 React + Tailwind
gemini "Convert this Figma frame to React: [LINK]. Use Tailwind CSS and make it responsive"

🔹 Next.js (TypeScript)
gemini "Create a Next.js component from [LINK] with TypeScript and Tailwind"

🔹 Vue 3
gemini "Generate a Vue 3 component with Composition API from [LINK]"

🎉 You're Ready!

You're now fully ready to convert Figma designs into production-ready code using Gemini CLI.git