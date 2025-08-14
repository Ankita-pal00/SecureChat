# End to End Encrypted Chat Application 

A modern web application built with **TypeScript**, **Tailwind CSS**, and **shadcn/ui** components, configured for clean architecture and scalable development.

---

## 🚀 Features

- **TypeScript** for type safety
- **Tailwind CSS** for utility-first styling
- **shadcn/ui** for beautiful prebuilt components (`new-york` style)
- **PostCSS + Autoprefixer** for CSS compatibility
- **Path Aliases** for cleaner imports
- **Vite**-compatible configuration

---

## 📂 Project Structure

```
.
├── client/
│   └── src/          # Frontend source code
│       ├── components/ # Reusable UI components
│       ├── hooks/      # Custom React hooks
│       ├── lib/        # Utility functions
│       ├── index.css   # Tailwind base styles
├── shared/           # Shared code between client and server
├── server/           # Backend code
├── components.json   # shadcn/ui configuration
├── postcss.config.js # PostCSS setup
├── tailwind.config.ts# Tailwind CSS config
├── tsconfig.json     # TypeScript compiler settings
```

---

## ⚙️ Installation

```bash
# Install dependencies
npm install

# Or with yarn
yarn install

# Or with pnpm
pnpm install
```

---

## 🛠 Development

```bash
# Start development server
npm run dev
```

The project will be available at:

```
http://localhost:5173
```

---

## 🏗 Build

```bash
npm run build
```

The built files will be in the `/dist` folder.

---

## 🧪 Lint & Type Check

```bash
# Run ESLint
npm run lint

# Type checking
npm run type-check
```

---

## 🎨 Styling

This project uses **Tailwind CSS** with `neutral` as the base color.  
CSS variables are enabled, and styles are defined in:

```
client/src/index.css
```

---

## 📦 Aliases

The following aliases are configured in `tsconfig.json` and `components.json`:

| Alias        | Path                  |
|--------------|-----------------------|
| `@/`         | `client/src/*`        |
| `@shared/*`  | `shared/*`             |
| `components` | `@/components`        |
| `utils`      | `@/lib/utils`         |
| `ui`         | `@/components/ui`     |
| `lib`        | `@/lib`               |
| `hooks`      | `@/hooks`              |

---

## 📜 License

This project is licensed under the MIT License.
