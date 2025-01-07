- ```
  npm install --save-dev husky
  ```
- To automatically have Git hooks enabled after install, edit **package.json**
- ```
  npm pkg set scripts.prepare="husky install"
  ```
- After running this you should have this in your **package.json**
- ```
  {
    "scripts": {
      "prepare": "husky install" 
    }
  }
  ```
- The `init` command simplifies setting up husky in a project. It creates a `pre-commit` script in `.husky/` and updates the `prepare` script in `package.json.`
- ```
  npx lint-staged -r -p false
  ```