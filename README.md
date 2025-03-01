# Create a Vite/React/Tailwind Project

## Step 1: Create the Vite Project

### If you're already in the project directory:

Run the following command:

```bash
npm init
```

```bash
npm install
```

```bash
npm create vite@latest . -- --template react
```

### If you're not in the project directory:

Replace `my-project` with your desired project name:

```bash
npm create vite@latest my-project -- --template react
```

### Follow the prompts:

-   Select **React** as the template.
-   Choose **JavaScript** or **TypeScript**, and optionally enable **SWC (Speedy Web Compiler)** for faster compilation.

---

## Step 2: Navigate to the Project Directory

If you haven't already, move into your project folder:

```bash
cd my-project
```

---

## Step 3: Install Tailwind CSS via Vite Plugin

Run:

```bash
npm install tailwindcss @tailwindcss/vite
```

---

## Step 4: Configure Vite to Use Tailwind

Modify `vite.config.js` to include the Tailwind plugin:

```javascript
// https://tailwindcss.com/docs/installation/using-vite

import { defineConfig } from "vite";
import react from "@vitejs/plugin-react"; // This is already present; it may change if you chose SWC
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
    plugins: [react(), tailwindcss()], // Add the Tailwind plugin
});
```

---

## Step 5: Add Tailwind to Your Styles

Include the following in your `index.css` file:

```css
@import "tailwindcss";
```

---

## Auto-Generated README.md Content

### React + Vite

This template provides a minimal setup for using **React with Vite**, including **Hot Module Replacement (HMR)** and some **ESLint rules**.

### Available Plugins:

-   [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) – Uses [Babel](https://babeljs.io/) for Fast Refresh.
-   [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) – Uses [SWC](https://swc.rs/) for Fast Refresh.
