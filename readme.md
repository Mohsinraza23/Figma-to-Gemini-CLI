# 🎨 Connecting Figma to Gemini CLI  
A clean and simple guide to help you convert your **Figma designs into production-ready code** using **Gemini CLI**.

---

## 📌 Overview  
This guide walks you through generating a Figma Personal Access Token (PAT), installing Gemini CLI, and connecting both tools to automatically generate code from your UI designs.

---

## 🚀 Step 1: Generate Figma Personal Access Token (PAT)

1. Go to **figma.com**
2. Log in to your account  
3. Click your **Profile Icon** (top-right)
4. Select **Settings**
5. Scroll to **Personal Access Tokens**
6. Click **Create new token**
7. Copy and save your PAT safely

---

## 🛠 Step 2: Install Gemini CLI

Run the following command in your terminal:

```bash
npm install -g @google/gemini-cli
```

Check installation:

```bash
gemini --version
```

---

## 🔗 Step 3: Connect Figma to Gemini CLI

Use your PAT to connect Figma:

```bash
gemini figma login
```

Enter your **Figma Personal Access Token** when asked.

---

## 🧩 Step 4: Convert Figma Design to Code

Run:

```bash
gemini figma pull <FIGMA_FILE_URL>
```

And Gemini CLI will generate:

- Components  
- Layouts  
- Styles  
- Responsive code  
- Assets  

All automatically based on your design.

---

## 🧪 Helpful Gemini CLI Commands

```bash
gemini models             # List Gemini models
gemini figma pull URL    # Convert Figma file to code
gemini help              # View all commands
```

---

## 🔗 Connect With Me

**LinkedIn:** https://www.linkedin.com/in/mohsin-raza-a514392b6  
**YouTube:** https://www.youtube.com/  
**Facebook:** https://www.facebook.com/

---

### ✨ Made with ❤️ by Mohsin Raza
