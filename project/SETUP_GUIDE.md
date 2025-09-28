# VS Code Setup Guide for Survey Analysis Platform

## Quick Setup Commands

Run these commands in VS Code terminal:

```bash
# 1. Create project directory
mkdir survey-analysis-platform
cd survey-analysis-platform

# 2. Initialize project
npm init -y

# 3. Install dependencies
npm install react@^18.3.1 react-dom@^18.3.1 lucide-react@^0.344.0 papaparse@^5.5.3 react-dropzone@^14.3.8 recharts@^3.1.2 jspdf@^3.0.1 html2canvas@^1.4.1 lodash@^4.17.21 @types/lodash@^4.17.20 @types/papaparse@^5.3.16

npm install -D @types/react@^18.3.5 @types/react-dom@^18.3.0 @vitejs/plugin-react@^4.3.1 vite@^5.4.2 typescript@^5.5.3 tailwindcss@^3.4.1 autoprefixer@^10.4.18 postcss@^8.4.35 eslint@^9.9.1 typescript-eslint@^8.3.0 @eslint/js@^9.9.1 eslint-plugin-react-hooks@^5.1.0-rc.0 eslint-plugin-react-refresh@^0.4.11 globals@^15.9.0

# 4. Create directory structure
mkdir src
mkdir src/components
mkdir src/utils
mkdir src/types

# 5. Initialize Tailwind CSS
npx tailwindcss init -p
```

## File Structure to Create

```
survey-analysis-platform/
├── package.json
├── index.html
├── vite.config.ts
├── tailwind.config.js
├── postcss.config.js
├── tsconfig.json
├── tsconfig.app.json
├── tsconfig.node.json
├── eslint.config.js
├── src/
│   ├── main.tsx
│   ├── App.tsx
│   ├── index.css
│   ├── vite-env.d.ts
│   ├── types/
│   │   └── survey.ts
│   ├── utils/
│   │   ├── dataProcessor.ts
│   │   ├── statisticalAnalysis.ts
│   │   └── reportGenerator.ts
│   └── components/
│       ├── FileUpload.tsx
│       ├── DataPreview.tsx
│       ├── CleaningConfiguration.tsx
│       ├── WeightConfiguration.tsx
│       ├── AnalysisConfiguration.tsx
│       ├── ProcessingStatus.tsx
│       └── ResultsDisplay.tsx
```

## Step-by-Step File Creation

### 1. Root Configuration Files

Create `package.json`:
```json
{
  "name": "survey-analysis-platform",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "lint": "eslint .",
    "preview": "vite preview"
  },
  "dependencies": {
    "@types/lodash": "^4.17.20",
    "@types/papaparse": "^5.3.16",
    "html2canvas": "^1.4.1",
    "jspdf": "^3.0.1",
    "lodash": "^4.17.21",
    "lucide-react": "^0.344.0",
    "papaparse": "^5.5.3",
    "react": "^18.3.1",
    "react-dom": "^18.3.1",
    "react-dropzone": "^14.3.8",
    "recharts": "^3.1.2"
  },
  "devDependencies": {
    "@eslint/js": "^9.9.1",
    "@types/react": "^18.3.5",
    "@types/react-dom": "^18.3.0",
    "@vitejs/plugin-react": "^4.3.1",
    "autoprefixer": "^10.4.18",
    "eslint": "^9.9.1",
    "eslint-plugin-react-hooks": "^5.1.0-rc.0",
    "eslint-plugin-react-refresh": "^0.4.11",
    "globals": "^15.9.0",
    "postcss": "^8.4.35",
    "tailwindcss": "^3.4.1",
    "typescript": "^5.5.3",
    "typescript-eslint": "^8.3.0",
    "vite": "^5.4.2"
  }
}
```

### 2. Copy All Source Files

Copy the content from each file shown in the project files above into their respective locations.

### 3. Run the Application

```bash
# Start development server
npm run dev
```

## VS Code Extensions (Recommended)

Install these VS Code extensions for better development experience:

1. **ES7+ React/Redux/React-Native snippets**
2. **Tailwind CSS IntelliSense**
3. **TypeScript Importer**
4. **Auto Rename Tag**
5. **Bracket Pair Colorizer**
6. **GitLens**
7. **Prettier - Code formatter**
8. **ESLint**

## VS Code Settings

Add this to your VS Code settings.json for better formatting:

```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "typescript": "typescriptreact"
  },
  "tailwindCSS.includeLanguages": {
    "typescript": "typescript",
    "typescriptreact": "typescriptreact"
  }
}
```

## Troubleshooting

### Common Issues:

1. **Module not found errors**: Run `npm install` again
2. **TypeScript errors**: Make sure all `.ts` and `.tsx` files are created
3. **Tailwind not working**: Ensure `src/index.css` contains the Tailwind directives
4. **Port already in use**: Use `npm run dev -- --port 3001` to use a different port

### Testing the Application:

1. Upload a CSV file with headers
2. Configure data cleaning options
3. Set up analysis parameters
4. Run the analysis
5. Download PDF/HTML reports

The application should be accessible at `http://localhost:5173` (or the port shown in terminal).