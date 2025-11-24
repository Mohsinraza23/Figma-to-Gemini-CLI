Bilkul bhai, ab ek **100% professional, official-looking, super clean aur active vibe** wala GitHub README bana deta hoon jo bilkul premium repositories jaisa lage ga. Ye wala bilkul perfect hai — students, developers aur teachers sab ko pasand ayega.

```markdown
# Figma → Code with Gemini CLI  
### Official Student Guide (2025)

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/figma/figma-original.svg" width="60" align="right" />

Turn your **Figma designs into production-ready code** instantly using **Google Gemini CLI** — no more manual HTML/CSS grinding!

Supports: **HTML • CSS • React • Tailwind • Next.js • Vue • TypeScript • Responsive • Dark Mode**

---

## Prerequisites

Before starting, make sure you have:

- [Gemini CLI installed](https://ai.google.dev/gemini-api/docs/cli)  
- A Figma account (free works perfectly)  
- Basic terminal knowledge

---

## Step 1: Generate Figma Personal Access Token

1. Go to → [https://www.figma.com](https://www.figma.com)  
2. Click your avatar → **Settings**  
3. Go to **Account** → **Personal access tokens**  
4. **Check all permission boxes** (required for full access)  
5. Click **Generate new token**  
6. Name it: `Gemini CLI Token`  
7. **Copy the token immediately** (it won't show again!)  
8. Save it securely

> Never commit this token to GitHub!

---

## Step 2: Connect Figma to Gemini CLI

Open your terminal and run:

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN"
```

Replace `YOUR_TOKEN` with your actual PAT.

Example:
```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

---

## Step 3: Verify Connection

```bash
gemini mcp list
```

You should see:

```bash
🟢 figma - Ready (8 tools available)
```

Success! You're now connected.

---

## Step 4: Prepare Your Figma File

### 1. Share Settings
- Open your file → Click **Share** (top right)  
- Set permission: **Anyone with the link → Can view**  
- Copy the file link

### 2. Get Frame Link (Important!)
- Select the frame you want to convert  
- Right-click → **Copy/Paste link to selection**  
- This gives you the exact `node-id` needed

Example link:
```
https://www.figma.com/design/abc123/Project?t=xyz&node-id=45-678
```

---

## Step 5: Generate Code (The Magic)

### Basic HTML + CSS
```bash
gemini "Convert this Figma frame to clean, semantic HTML and modern CSS: [YOUR_FRAME_LINK]"
```

### React + Tailwind CSS (Recommended)
```bash
gemini "Generate a responsive React component using Tailwind CSS from this design: [LINK]"
```

### Next.js 14 + TypeScript + App Router
```bash
gemini "Create a complete Next.js 14 page with TypeScript, app router and Tailwind from: [LINK]"
```

### Vue 3 + Composition API
```bash
gemini "Build a Vue 3 component with Composition API and Tailwind from this frame: [LINK]"
```

Code appears instantly in your terminal!

---

## Available Figma Tools (After Connection)

| Tool                    | Description                                      |
|-------------------------|--------------------------------------------------|
| `get_design_context`    | Extracts full layout, colors, spacing, text      |
| `get_screenshot`        | Returns image of selected frame                  |
| `get_metadata`          | File info, variables, styles                     |
| `get_variable_defs`     | Extracts design tokens & variables               |
| `whoami`                | Shows connected Figma account                    |

---

## Troubleshooting

| Issue                                | Fix                                                                 |
|--------------------------------------|----------------------------------------------------------------------|
| "File could not be accessed"         | Ensure file is shared as **Anyone with link can view**              |
| "Unauthorized" or token error        | Regenerate PAT with **all permissions checked**                      |
| Figma shows disconnected             | Run: `gemini mcp remove figma` → Reconnect with new token           |
| Wrong frame selected                 | Always use **Copy link to selection** (not just file link)           |

---

## Best Practices & Pro Tips

- Always start with **one frame**  
- Use specific prompts:  
  → "Make it mobile-first responsive"  
  → "Use Tailwind v3.4+"  
  → "Add dark mode with `dark:` prefix"  
  → "Include proper ARIA labels"  
- Ask to save files:  
  → "...and save as `HomePage.tsx` and `styles.css`"

---

## Example Prompts (Copy-Paste Ready)

```bash
gemini "Create a fully responsive landing page in React + Tailwind from this frame. Use modern best practices: https://www.figma.com/file/...&node-id=123-456"
```

```bash
gemini "Generate a Next.js dashboard sidebar component with dark mode support from: [LINK]"
```

```bash
gemini "Convert this card design to HTML + Tailwind with hover effects and accessibility: [LINK]"
```

---

## Final Checklist

- [ ] Gemini CLI installed  
- [ ] Figma PAT generated & saved  
- [ ] Connected via `gemini mcp add`  
- [ ] Verified with `gemini mcp list`  
- [ ] File shared publicly  
- [ ] Used **frame-specific link**  
- [ ] Ran code generation prompt  

---

## Resources

- Gemini CLI Docs → https://ai.google.dev/gemini-api/docs/cli  
- Figma MCP → https://mcp.figma.com  
- Gemini API → https://ai.google.dev

---

**Made for students, by someone who was tired of writing boilerplate code**  
**Figma to Code = 10 seconds. Not 10 hours.**

Start converting now → Open terminal → Paste link → Done.

**Happy coding!**  
```

