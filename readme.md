
## 🚀 Connecting Figma to Gemini CLI - Student Guide  
A step-by-step guide to convert your Figma designs into code using Gemini CLI.

---

## ⭐ Step 1: Generate Figma Personal Access Token (PAT)

- Go to Figma.com and log in  
- Click your profile icon (top-right corner)  
- Select **Settings**  
- Click on the **Account** tab  
- Scroll down to **Personal Access Tokens** section  
- **Make Sure to tick on all the checkboxes. If not you won't be able to access Figma**  
- Click **Generate new token**  
- Give your token a name (e.g., "Gemini CLI Access")  
- Click **Generate token**  

⚠️ **Copy the token immediately — you won't be able to see it again!**  
Save it somewhere safe.

---

## ⭐ Step 2: Connect Figma MCP Server to Gemini CLI

Open your terminal and run:

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer YOUR_TOKEN_HERE"
```

⚠️ Replace **YOUR_TOKEN_HERE** with your actual Figma token.

### Example:

```bash
gemini mcp add --transport http figma https://mcp.figma.com/mcp --header "Authorization: Bearer figd_abc123xyz789"
```

---

## ⭐ Step 3: Verify Connection

```bash
gemini mcp list
```

You should see:

```
🟢 figma - Ready (8 tools, 1 prompt)
```

If you see this — **you're all set! ✅**

---

## ⭐ Step 4: Prepare Your Figma File

### Make Your File Accessible:

- Open your Figma design file in the browser  
- Click **Share** (top-right)  
- Change to **"Anyone with the link can view"**  
- Click **Copy link**

### Copy Frame Link:

- Select the frame  
- Right-click → **Copy link to selection**  
- Save this link  

Example format:

```
https://www.figma.com/design/abc123/MyProject?node-id=1-23&t=45567
```

---

## ⭐ Step 5: Generate Code from Figma Design

Run this:

```bash
gemini "Get the design context from [PASTE_YOUR_FIGMA_LINK] and generate HTML and CSS"
```

### Real Example:

```bash
gemini "Get the design context from https://www.figma.com/design/abRnucBMTsgblvDB6ymtd1/Hospital-Design?node-id=1-218 and generate HTML and CSS"
```

### What happens:

- Gemini fetches your design  
- Extracts layout, colors, spacing  
- Generates clean HTML & CSS  
- Displays code in terminal  

---

## ⭐ Step 6: Customize Output (Optional)

### For React Components

```bash
gemini "Get design context from [YOUR_LINK] and generate React components with Tailwind CSS"
```

### For Responsive Design

```bash
gemini "Use get_design_context on [YOUR_LINK] and create mobile-responsive HTML and CSS"
```

---

# 🔧 Quick Troubleshooting

### ❌ **Problem:** "This figma file could not be accessed"  
**Fixes:**

- Ensure file is **Anyone with link can view**  
- PAT must have permissions  
- Try file you own  
- Test using a public Figma Community file  

---

### ❌ Figma shows **"Disconnected"**

Remove:

```bash
gemini mcp remove figma
```

Re-add connection, then verify:

```bash
gemini mcp list
```

---

### ❌ Token not working  
**Fix:**

- Create new token  
- Copy exactly  
- Reconnect using Step 3  

---

# ✅ Summary Checklist

- Install Gemini CLI  
- Create Figma PAT token  
- Connect Figma MCP  
- Verify connection  
- Share Figma file publicly  
- Copy frame link  
- Run prompt to generate code  
- Save/output your code  

---

# 🛠 Available Figma Tools

| Tool | Purpose |
|------|---------|
| get_design_context | Main tool – extracts design structure |
| get_screenshot | Gets frame screenshot |
| get_metadata | Gets file info & styles |
| get_variable_defs | Extracts design tokens |
| get_code_connect_map | Links components to code |
| get_figjam | FigJam content |
| whoami | Verify account |

---

# 🎯 Tips for Best Results

- Be specific in your prompts  
- Mention framework & libraries  
- Convert one frame at a time  
- Iterate & refine  
- Ask Gemini to save files  

---

# 💡 Example Prompts

### Basic HTML/CSS
```bash
gemini "Get design context from [LINK] and generate semantic HTML5 and modern CSS"
```

### React + Tailwind
```bash
gemini "Convert this Figma frame to React: [LINK]. Use Tailwind CSS and make it responsive"
```

### Next.js Component
```bash
gemini "Create a Next.js component from [LINK] with TypeScript and Tailwind"
```

### Vue 3
```bash
gemini "Generate a Vue 3 component with Composition API from [LINK]"
```

---

# ❓ Need Help?

- Check **Figma MCP Documentation**  
- Visit **Gemini CLI Docs**  
- Ask instructor  

---

# 🎉 Happy Coding!  
You're now ready to convert designs to code seamlessly!

---

## 👤 Author — **Mohsin Raza**

### 🔗 Connect With Me  
**LinkedIn:** https://www.linkedin.com/in/mohsin-raza-a514392b6  
**YouTube:** *https://www.youtube.com/@TechMohsin581*  
**Facebook:** *https://www.facebook.com/profile.php?id=61578455632342*  
