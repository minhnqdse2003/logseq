- Lint-staged ensures that only staged files are linted and formatted.Run below to install it.
- ```
  npm install lint-staged @commitlint/cli @commitlint/config-conventional --save-dev
  ```
- Lint-staged and Husky will work together to run Prettier and ESLint on staged files before each commit.
- In your root directory, create a file **.lintstagedrc.json**
- ```
  {
    "*.js": ["eslint --fix", "prettier --write"],
    "*.jsx": ["eslint --fix", "prettier --write"],
    "*.ts": ["eslint --fix", "prettier --write"],
    "*.tsx": ["eslint --fix", "prettier --write"],
    "*.json": ["prettier --write"],
    "*.md": ["prettier --write"]
  }
  ```
- try to verify it by running **npx lint-staged.**
- Create a new file **commit-msg** file inside the **.husky folder**. and add the below content to it
- ```
  npx --no-install commitlint --edit
  ```
- Create a new file .**commitlint.config.js** and the below content to it
- ```
  @commitlint/config-workspace-scopes
  ```