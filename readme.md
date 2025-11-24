# 🔗 Connecting Figma to Gemini CLI  
### Turn Your Figma Designs into Production-Ready Code in Seconds! ⚡

[![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)](https://figma.com)
[![Gemini CLI](https://img.shields.io/badge/Gemini_CLI-8B3EFF?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev/gemini-api)
[![Made for Students](https://img.shields.io/badge/Made_for-Students-10B981?style=for-the-badge)](https://github.com)

A complete **step-by-step student guide** to connect Figma with Gemini CLI and convert any design frame into clean HTML, CSS, React, Tailwind, Next.js, Vue — you name it! 🚀

---

## 🚀 Step 1: Generate Figma Personal Access Token (PAT)

1. Go to [Figma.com](https://www.figma.com) and log in  
2. Click your **profile icon** (top-right) → **Settings**  
3. Go to **Account** tab  
4. Scroll to **Personal access tokens**  
5. ✅ **Tick all checkboxes** (very important!)  
6. Click **Generate new token**  
7. Name it (e.g., `Gemini CLI Access`)  
8. Click **Generate token**  
9. ⚠️ **Copy the token immediately** — you won’t see it again!  
10. Store it safely (password manager recommended)

---

## 🔌 Step 2: Connect Figma MCP Server to Gemini CLI

Open a new terminal and run:

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN_HERE"

Replace YOUR_TOKEN_HERE with your actual token.
Example:

gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_abc123xyz789"

✅ Step 3: Verify Connection

gemini mcp list

Success looks like this:
🟢 figma - Ready (8 tools, 1 prompt)

You’re connected! 🎉
🖼️ Step 4: Prepare Your Figma File
Make File Accessible

Open your design file
Click Share (top-right)
Set to "Anyone with the link can view"
Copy the link

Get Frame Link

Select the frame you want to convert
Right-click → Copy link to selection
Save this link

Example link:
https://www.figma.com/design/abc123/MyProject?node-id=1-23&t=45567

