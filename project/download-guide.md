# Survey Analysis Platform - Download Guide

## Project Structure
```
survey-analysis-platform/
├── package.json
├── tsconfig.json
├── tsconfig.app.json
├── tsconfig.node.json
├── vite.config.ts
├── tailwind.config.js
├── postcss.config.js
├── eslint.config.js
├── index.html
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

## Setup Instructions

1. Create a new directory: `mkdir survey-analysis-platform && cd survey-analysis-platform`

2. Initialize the project:
```bash
npm init -y
```

3. Install dependencies:
```bash
npm install react@^18.3.1 react-dom@^18.3.1 lucide-react@^0.344.0 papaparse@^5.5.3 react-dropzone@^14.3.8 recharts@^3.1.2 jspdf@^3.0.1 html2canvas@^1.4.1 lodash@^4.17.21

npm install -D @types/react@^18.3.5 @types/react-dom@^18.3.0 @types/papaparse@^5.3.16 @types/lodash@^4.17.20 @vitejs/plugin-react@^4.3.1 vite@^5.4.2 typescript@^5.5.3 tailwindcss@^3.4.1 autoprefixer@^10.4.18 postcss@^8.4.35 eslint@^9.9.1 typescript-eslint@^8.3.0 @eslint/js@^9.9.1 eslint-plugin-react-hooks@^5.1.0-rc.0 eslint-plugin-react-refresh@^0.4.11 globals@^15.9.0
```

4. Copy all the file contents from this conversation into their respective files

5. Run the development server:
```bash
npm run dev
```

## Key Features Implemented

- **File Upload**: Drag & drop CSV upload with validation
- **Data Preview**: Interactive table with column statistics
- **Data Cleaning**: 
  - Multiple imputation methods (mean, median, mode, forward/backward fill)
  - Outlier detection (IQR, Z-score, isolation forest)
  - Custom validation rules
- **Survey Weights**: Weight column selection and stratification
- **Statistical Analysis**: Confidence intervals, margins of error
- **Report Generation**: PDF and HTML reports with jsPDF
- **Responsive Design**: Professional UI with Tailwind CSS

## Technologies Used

- **Frontend**: React 18 + TypeScript
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Charts**: Recharts
- **File Processing**: PapaParse
- **PDF Generation**: jsPDF + html2canvas
- **Build Tool**: Vite
- **Data Processing**: Lodash

## File Upload Requirements

- CSV files only
- Maximum 10MB file size
- First row must contain headers
- Supports numeric and text data types

## Report Features

- Comprehensive statistical analysis
- Data quality metrics
- Processing step documentation
- Downloadable PDF and HTML formats
- Professional formatting suitable for presentations

## Deployment

The application is deployed at: https://playful-marigold-a8f56e.netlify.app

To deploy your own version:
1. Build the project: `npm run build`
2. Deploy the `dist` folder to any static hosting service