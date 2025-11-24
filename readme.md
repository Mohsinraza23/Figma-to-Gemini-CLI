```markdown
# Figma → Code with Gemini CLI  
### Official Student Guide • 2025

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/figma/figma-original.svg" alt="Figma" width="60" align="right"/>

Instantly convert your Figma designs into **HTML • CSS • React • Tailwind • Next.js • Vue • TypeScript** using Google Gemini CLI.

---

## Prerequisites
- Gemini CLI installed → [Official Docs](https://ai.google.dev/gemini-api/docs/cli)
- Figma account (free tier is enough)
- Basic terminal access

---

## Step 1 → Generate Figma Personal Access Token (PAT)

1. Go to [figma.com](https://www.figma.com) → Login  
2. Avatar → **Settings** → **Account** → **Personal access tokens**  
3. **Check all permission boxes** (mandatory)  
4. Click **Generate new token** → Name it `Gemini CLI`  
5. **Copy the token immediately** (you won’t see it again)  
6. Save it securely (never commit to GitHub!)

---

## Step 2 → Connect Figma to Gemini CLI

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN_HERE"
```

Example:
```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_xxxxxxxxxxxxxxxxxx"
```

---

## Step 3 → Verify Connection

```bash
gemini mcp list
```

You should see:
```
figma - Ready (8 tools available)
```

---

## Step 4 → Prepare Your Figma File

### Share File
- Open file → **Share** → **Anyone with the link → Can view** → Copy link

### Get Exact Frame Link (Important!)
- Select the frame → Right-click → **Copy/Paste link to selection**  
Example:
```
https://www.figma.com/design/abc123/Project?node-id=45-678&t=xyz
```

---

## Step 5 → Generate Code (Magic!)

### HTML + CSS
```bash
gemini "Convert this Figma frame to clean semantic HTML and modern CSS: [FRAME_LINK]"
```

### React + Tailwind (Most Used)
```bash
gemini "Generate a fully responsive React component with Tailwind CSS from: [LINK]"
```

### Next.js 14 + TypeScript
```bash
gemini "Create a Next.js 14 page/component with TypeScript and Tailwind from this design: [LINK]"
```

### Vue 3
```bash
gemini "Build a Vue 3 component with Composition API and Tailwind from: [LINK]"
```

---

## Available Tools (After Connection)

| Tool                  | Purpose                                      |
|-----------------------|----------------------------------------------|
| get_design_context    | Full layout, colors, spacing, typography     |
| get_screenshot        | Image of the frame                           |
| get_metadata          | File info & styles                           |
| get_variable_defs     | Design tokens & variables                    |
| whoami                | Connected account info                       |

---

## Troubleshooting

| Problem                          | Solution                                                      |
|----------------------------------|---------------------------------------------------------------|
| "File could not be accessed"     | Share as **Anyone with link can view**                        |
| Token error / Unauthorized       | Regenerate PAT with **all boxes checked**                     |
| Figma disconnected               | `gemini mcp remove figma` → Re-add token                     |
| Wrong frame                      | Always use **Copy link to selection**                         |

---

## Pro Tips

- Convert one frame at a time  
- Be specific: “mobile-first”, “dark mode”, “ARIA labels”  
- Ask to save files: “…and save as `Component.tsx`”  

---

## Ready-to-Use Prompts

```bash
gemini "Create responsive React + Tailwind landing page from: https://www.figma.com/file/...&node-id=..."
```

```bash
gemini "Generate Next.js dashboard with dark mode from this frame: [LINK]"
```

---

## Final Checklist

- [ ] Gemini CLI installed  
- [ ] PAT generated & copied  
- [ ] Connected with `gemini mcp add`  
- [ ] Verified connection  
- [ ] File shared publicly  
- [ ] Used frame-specific link  
- [ ] Code generated!

---

**Resources**  
- Gemini CLI → https://ai.google.dev/gemini-api/docs/cli  
- Figma MCP → https://mcp.figma.com  

**Figma to Code in 10 seconds — not 10 hours.**  
Happy coding!
```

