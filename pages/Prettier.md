- Prettier formats your code to a consistent style. To setup prettier just Run the below command:
  
  ```
  npm install --save-dev prettier eslint-config-prettier eslint-plugin-prettier prettier-plugin-tailwindcss
  ```
- Create a new file called **.prettierrc** in the root of your project with the following content:
  
  ```
  {
    "arrowParens": "avoid",
    "bracketSpacing": true,
    "htmlWhitespaceSensitivity": "css",
    "insertPragma": false,
    "jsxSingleQuote": true,
    "bracketSameLine": true,
    "printWidth": 80,
    "proseWrap": "always",
    "quoteProps": "as-needed",
    "requirePragma": false,
    "semi": false,
    "singleQuote": true,
    "tabWidth": 2,
    "trailingComma": "all",
    "useTabs": false
  }
  ```
- A **.prettierignore **file is used to tell Prettier to ignore specific files and directories in your project, similar to a `.gitignore` file. This is useful when you have certain files or directories that you don't want to be automatically formatted by Prettier.
  
  ```
  # Ignore node_modules directory (third-party dependencies)
  node_modules
  .npm
  npm-debug.log
  
  # Ignore build directories
  dist/**
  build/**
  
  # Ignore output from Next.js
  .next/**
  
  # Ignore TypeScript declaration files
  *.d.ts
  
  # Ignore environment files
  .env
  .env.local
  .env.production
  .env.*.local
  
  # Ignore lock files (if you don't want Prettier to format them)
  package-lock.json
  yarn.lock
  
  # Ignore coverage reports
  coverage
  
  # Ignore generated files from Prisma or other ORMs
  prisma/generated
  
  # Ignore public assets or static files
  public
  
  # Ignore logs
  *.log
  
  # Ignore markdown files (if you don't want them formatted)
  *.md
  
  # Ignore all files in a specific directory (e.g., assets)
  assets/
  
  # Ignore specific files (e.g., a custom configuration file)
  my-custom-config.js
  
  # Ignore specific file extensions (e.g., images, videos)
  *.png
  *.jpg
  *.jpeg
  *.gif
  *.mp4
  *.svg
  ```
- Add the following scripts to your **package.json** file:
- ```
  "format": "npx prettier --write .",
  "format-write": "npx prettier --write --all=true",
  "format-check": "npx prettier --check --all=true"
  ```
- To run prettier run the below command:
  ```
  npm run format
  ```
-