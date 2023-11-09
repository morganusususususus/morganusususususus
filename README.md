"name": "github-script",
  "description": "A GitHub action for executing a simple script",
  "version": "5.0.0",
  "version": "5.0.1",
  "author": "GitHub",
  "license": "MIT",
  "main": "dist/index.js",
@@ -14,12 +14,8 @@
    "style:check": "run-p --continue-on-error --aggregate-output format:check lint",
    "style:write": "run-p --continue-on-error --aggregate-output format:write lint",
    "pre-commit": "run-s style:write test build",
    "test": "jest"
  },
  "husky": {
    "hooks": {
      "pre-commit": "npm run pre-commit && git add dist/"
    }
    "test": "jest",
    "prepare": "husky install"
  },
  "jest": {
    "preset": "ts-jest",
@@ -45,17 +41,17 @@
    "@octokit/plugin-rest-endpoint-methods": "^5.11.1"
  },
  "devDependencies": {
    "@types/jest": "^26.0.24",
    "@types/jest": "^27.0.2",
    "@typescript-eslint/eslint-plugin": "^3.10.1",
    "@typescript-eslint/parser": "^3.10.1",
    "@vercel/ncc": "^0.23.0",
    "eslint": "^7.32.0",
    "eslint-config-prettier": "^6.15.0",
    "husky": "^4.2.5",
    "jest": "^26.6.3",
    "husky": "^7.0.0",
    "jest": "^27.2.5",
    "npm-run-all": "^4.1.5",
    "prettier": "^2.0.5",
    "ts-jest": "^26.5.6",
    "ts-jest": "^27.0.5",
    "typescript": "^4.3.5"
