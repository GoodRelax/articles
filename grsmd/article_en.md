VS Code's `Ctrl+Shift+V` works.  
But you can't keep rendered previews open in separate browser tabs, and you can't view multiple documents side by side without splitting editor windows.

**GRSMD** (GoodRelax Simple Markdown Renderer & Viewer) is a single `index.html` file that opens in your browser.

### **Just drop a `.md` file onto it or paste with `Ctrl+V`**

#### **— it renders immediately.**

- **Live:** https://goodrelax.github.io/gr-simple-md-renderer/
- **Source:** https://github.com/GoodRelax/gr-simple-md-renderer

#### Press `[New Tab]` for multiple documents.

---

## What it renders

| Feature             | Library              | Processed locally? |
| ------------------- | -------------------- | ------------------ |
| Markdown            | marked.js 17.0.1     | Yes                |
| Mermaid diagrams    | Mermaid.js 11.12.2   | Yes                |
| Syntax highlighting | highlight.js 11.11.1 | Yes                |
| LaTeX math          | KaTeX 0.16.28        | Yes                |
| PlantUML            | plantuml.com         | Consent required   |

All rendering exept for PlantUML happens in your local browser.  
No npm. No build. Just load libraries from CDN.

---

## Why it works better than VS Code preview for some workflows

- **Multiple tabs** — open several documents at once in separate browser tabs
- **Drag and drop** — drop `.md` or `.txt` files directly onto the editor or preview area
- **Paste** — `Ctrl+V` drops Markdown straight into the editor
- **New Tab button** — clones the renderer into a fresh browser tab in one click
- **Zoom and pan** — `Ctrl+Scroll` to zoom any diagram (0.5x to 5.0x), drag to pan, double-click to reset
- **Scroll preserved** — re-rendering does not jump you back to the top
- **Copy diagrams to clipboard** — press `[Copy SVG]` / `[Copy PNG]` and paste it into PowerPoint etc.

---

## Privacy model

Nothing leaves your browser unless you allow it.
Here's how the security model works:

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/6298et8yqc7ii80go7k7.png)

PlantUML is the only exception — it requires the official PlantUML server to render.  
A confirmation dialog appears before any data is sent.  
Cancel it and everything else renders fine.

---

## Special tip

Long press the **`[?]`** button to improve your productivity with AI.

---

## Try it

- **Live:** https://goodrelax.github.io/gr-simple-md-renderer/
- **Quick sample:** https://goodrelax.github.io/gr-simple-md-renderer/sample-data.txt
- **Full sample (Mermaid + PlantUML + LaTeX):** https://goodrelax.github.io/gr-simple-md-renderer/sample-data-2.md

Drop one of the sample files onto the live page.
