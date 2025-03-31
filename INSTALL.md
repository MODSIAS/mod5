# Installation Guide for My Web Project

This document provides detailed instructions for setting up and running the web project.

## Prerequisites

Before installing, make sure you have the following:

- [Node.js](https://nodejs.org/) (v14.0.0 or higher)
- npm (usually comes with Node.js)
- Git (for cloning the repository)

## Basic Installation

### 1. Clone the Repository

```bash
git clone <repository-url>
cd my-web-project
```

### 2. Install Dependencies

```bash
npm install
```

This will install all required packages defined in `package.json`.

### 3. Start Development Server

```bash
npm start
```

This will start a local development server at http://localhost:3000.

## Manual Installation (No npm)

If you prefer not to use npm, you can simply:

1. Download the project files
2. Open `index.html` directly in your browser

Note: Some features like the resource connector may not work without a proper server.

## Production Build

To create an optimized production build:

```bash
npm run build
```

This will create a `dist` directory with minified and optimized files ready for deployment.

## Advanced Configuration

### Custom Port

To start the development server on a custom port:

```bash
npx http-server -p <your-port-number>
```

### Environment Variables

Create a `.env` file in the project root to configure:

```
PORT=3000
NODE_ENV=development
```

## Troubleshooting

### Common Issues

1. **EADDRINUSE error when starting the server**  
   This means the port is already in use. Try using a different port:
   ```bash
   npm start -- --port 3001
   ```

2. **Missing dependencies errors**  
   Try removing the node_modules folder and reinstalling:
   ```bash
   rm -rf node_modules
   npm install
   ```

3. **Build process fails**  
   Make sure you have all required dependencies:
   ```bash
   npm install --save-dev clean-css terser html-minifier fs-extra
   ```

### Still Having Problems?

Run the automated setup script:

```bash
node tools/setup.js
```

## Next Steps

After installation:

1. Review the project structure to familiarize yourself with the files
2. Check out the documentation in `docs/documentation.md`
3. Try customizing the CSS and JavaScript to fit your needs

## Updating

To update to the latest version:

```bash
git pull
npm install
```
