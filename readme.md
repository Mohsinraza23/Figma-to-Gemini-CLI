
Markdown<div align="center">

# Connecting Figma to Gemini CLI  
### Student Guide 2025 — Turn Designs into Code in Seconds!

<img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white" alt="Figma"/>
<img src="https://img.shields.io/badge/Gemini_CLI-8B5CF6?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini"/>
<img src="https://img.shields.io/badge/Status-Working_%E2%9C%85-10B981?style=for-the-badge" alt="Working"/>

**No more manual coding from designs**  
Figma → One Command → Clean HTML / React / Tailwind Code

</div>

---

### Step 1: Generate Figma Personal Access Token (PAT)

1. Go to [figma.com](https://www.figma.com) → Login  
2. Click your **profile icon** (top-right)  
3. → **Settings**  
4. → **Account** tab  
5. Scroll down → **Personal access tokens**  
6. **Tick all checkboxes** (super important!)  
7. Click **Generate new token**  
8. Name it → `Gemini CLI Access`  
9. Click **Generate token**  
10. **COPY THE TOKEN IMMEDIATELY**  
11. Save it somewhere safe (Notes, password manager)

---

### Step 2: Connect Figma to Gemini CLI (One-Time Setup)

Terminal mein ye command chalao:


gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN_HERE"

Example:

gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_abc123xyz789"

Step 3: Verify Connection

gemini mcp list

Success dekhna chahiye:

textConnected figma - Ready (8 tools, 1 prompt)

Step 4: Prepare Your Figma File
A) Make file public

Open file → Click Share (top right)
Set to "Anyone with the link can view"
Click Copy link

B) Copy Frame Link (Sabse Zaroori!)

Select the frame you want to convert
Right click → Copy link to selection

Example Frame Link:
texthttps://www.figma.com/design/abRnucBMTsgblvDB6ymtd1/Hospital-Design?node-id=1-218

Step 5: Generate Code (The Real Magic!)
gemini "Get the design context from [PASTE_FRAME_LINK] and generate HTML and CSS"

Real Example:

gemini "Get the design context from https://www.figma.com/design/abRnucBMTsgblvDB6ymtd1/Hospital-Design?node-id=1-218 and generate HTML and CSS"
Gemini automatically fetches:
→ Layout, colors, text, spacing, shadows, fonts
→ Outputs clean, working code in terminal
text---

### Step 6: Customize Output (Pro Level)

| Want This                     | Use This Prompt                                                                                   |
|-----------------------------|----------------------------------------------------------------------------------------------------|
| React + Tailwind            | `gemini "Convert this frame to React with Tailwind CSS and make it responsive: [LINK]"`           |
| Next.js + TypeScript        | `gemini "Create a Next.js component with TypeScript and Tailwind from [LINK]"`                    |
| Mobile Responsive HTML      | `gemini "Make mobile-first responsive HTML + CSS from this design: [LINK]"`                       |
| Save as files               | `gemini "Generate code from [LINK] and save as index.html and style.css"`                         |

---

### Quick Troubleshooting

| Problem                              | Solution                                                                 |
|--------------------------------------|--------------------------------------------------------------------------|
| "File could not be accessed"         | → File public hai? <br>→ Frame link use kiya? <br>→ Token me all permissions? |
| Figma shows "Disconnected"           | Run: `gemini mcp remove figma` → Phir Step 2 dobara                     |
| Token not working                    | Naya token banao → bina space copy karo                                  |

---

<div align="center">

### Final Checklist

- [ ] Gemini CLI installed  
- [ ] Figma PAT token banaya & copy kiya  
- [ ] `gemini mcp add` command chalaya  
- [ ] `gemini mcp list` → green tick  
- [ ] Frame ka link copy kiya  
- [ ] Code generate kiya → Done!

</div>

---

### Available Tools (Advanced)

| Tool                     | Kaam Kya Karta Hai                         |
|--------------------------|--------------------------------------------|
| `get_design_context`     | Pura design structure deta hai             |
| `get_screenshot`         | Design ka photo leta hai                   |
| `get_metadata`           | Colors, fonts, variables deta hai          |
| `get_variable_defs`      | Design tokens extract karta hai            |

---

### Pro Tips for Best Results

- Ek frame ek baar mein convert karo
- Prompt mein clearly bolo: "React + Tailwind + responsive"
- Agar code perfect na ho to prompt refine karo
- Bol do: "Save kar do files mein bhi"

---

<div align="center">

### Made with Love by Mohsin Raza  
Frontend + UI/UX Student

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mohsin-raza-a514392b6)  
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com)  
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com)

**Ab design banaya → code ready → project submit → full marks!**

Happy Coding Bro!

</div>
