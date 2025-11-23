<div align="center">

# Figma → Code in Seconds
### The Ultimate Student Guide to Connect **Figma + Gemini CLI**

<img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" alt="Figma"/>
<img src="https://img.shields.io/badge/Gemini_CLI-8B5CF6?style=for-the-badge&logo=google-gemini&logoColor=white" alt="Gemini"/>
<img src="https://img.shields.io/badge/Made_for-Students-10B981?style=for-the-badge" alt="Students"/>

**Turn any Figma design into clean code in 10 seconds**  
HTML • React • Tailwind • Next.js • Vue

</div>

---

### Step 1: Figma Personal Access Token (PAT) Banaye

1. [figma.com](https://www.figma.com) pe login karo  
2 Avatar → Settings → Account tab  
3 Neeche **Personal access tokens** mein jao  
4 Saare checkboxes tick karo  
5 **Generate new token** → naam daalo → Generate  
6 Token **turant copy kar lo** (doosri baar nahi dikhega!)

---

### Step 2: Gemini CLI se Connect Karo (Ek Baar Ka Kaam)


gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN"

Step 3: Connection Check Karo
gemini mcp list
Yeh aana chahiye → figma - Ready

Step 4: Figma File Ready Karo

Share button → Anyone with the link can view
Frame select karo → Right click → Copy link to selection


Step 5: Code Generate Karo (Asli Mazaa Yahan Hai)
# Simple HTML + CSS
gemini "Convert this Figma frame to clean HTML and CSS: YOUR_LINK"

# React + Tailwind (Sabse Zyada Use Hota Hai)
gemini "Convert this to React with Tailwind CSS, fully responsive: YOUR_LINK"

# Next.js Component
gemini "Create Next.js 14 page with TypeScript and Tailwind from this frame: YOUR_LINK"

Sabse Best Prompt (Save Kar Lo)
gemini "Convert this Figma frame to pixel-perfect React component using Tailwind CSS. Make it fully responsive, accessible, and production ready: YOUR_LINK_HERE"

Common Errors & Fix





















ProblemSolutionFile not accessibleFile public karo + frame link use karoDisconnected ya red dotgemini mcp remove figma → Step 2 dobaraToken expire/invalidNaya token banao


Final Checklist

 Gemini CLI installed
 Figma token banaya & copy kiya
gemini mcp add kiya
gemini mcp list → green
 Frame link copy kiya
 Code generate → Done!




Made with ❤️ by Mohsin Raza
UI/UX + Frontend Student
LinkedIn
YouTube
Instagram
Ab design banane ke baad code likhne ki tension khatam!
Figma → Code → Ship → Get Hired
