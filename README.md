# vite-react
### *src*
- assets -/img -/svg
- components / ui
- lib / utils
- style/ *.css (global.css)
- pages / router.jsx & -/docs -/contact
- anyDir
- main.jsx

#### react router dom
#### tailwindcss
#### base vite

[Shadcn UI](https://ui.shadcn.com/)

- ```npm create vite@latest```

- ```npm install -D tailwindcss postcss autoprefixer```

- ```npx tailwindcss init -p```

create jsconfig.json
```
{
  "compilerOptions": {
    // ...
    "baseUrl": ".",
    "paths": {
      "@/*": [
        "./src/*"
      ]
    }
    // ...
  }
}
```

- ```npm i -D @types/node```

edit vite.config.js
```
import path from "path"
import react from "@vitejs/plugin-react"
import { defineConfig } from "vite"

export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: {
      "@": path.resolve(__dirname, "./src"),
    },
  },
})
```

- ```npx shadcn-ui@latest init```

no (js)
default
src/style/global.css
yes
enter default tailwindcss
src/components
src/lib/utils
no
