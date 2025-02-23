# ts-npm-starter

**A starter template for creating npm packages with TypeScript.**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

---

## 🌟 Why Use This Starter?

`ts-npm-starter` is designed to provide a robust and optimized foundation for developing npm modules in TypeScript. It includes:

- **Ready-to-use TypeScript configuration**: Get started quickly with pre-configured settings.
- **Automated testing with Vitest**: Ensure your code works as expected with fast and reliable tests.
- **Code formatting with Prettier**: Maintain consistent and clean code across your project.
- **Version management with Changesets**: Simplify the process of managing and publishing new versions.
- **Optimized compatibility**: Ensure seamless usage in both Node.js and browser environments.

With this starter, you can focus on building your module without worrying about repetitive setup tasks.

---

## 📦 Installation

To get started, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/JKS9/ts-npm-starter.git my-module
   ```

2. Navigate to the project directory:
   ```bash
   cd my-module
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

---

## ⚙️ Configuration

Before starting development, make sure to configure the following in your `package.json` file:

- **Package Name**: Replace `"name": "ts-npm-starter"` with your module's name.
- **Author**: Add your name under the `"author"` field.
- **Description**: Provide a brief description of your module.
- **Module Entry Point**: Ensure that `"main"` is set to `"dist/index.js"`, and include the `dist/` folder in the `"files"` array.

Example:
```json
{
  "name": "my-module",
  "version": "1.0.0",
  "description": "A brief description of your module",
  "author": "Your Name",
  "main": "dist/index.js",
  "files": ["dist"]
}
```

---

## 🚀 Development Workflow

### 1. Compile TypeScript Code

Compile your TypeScript code into JavaScript:
```bash
npm run build
```

### 2. Run Tests

Execute automated tests using Vitest:
```bash
npm test
```

### 3. Check Code Formatting

Ensure your code adheres to the project's formatting standards:
```bash
npm run format
```

Alternatively, check for formatting issues without applying changes:
```bash
npm run check-format
```

### 4. Verify Package Exports

Validate that your package exports are correctly configured:
```bash
npm run check-exports
```

---

## 🔗 Testing Your Module Locally

You can test your module locally without publishing it to npm by using `npm link`. Here's how:

### Steps to Link Your Module Locally

1. In your module's directory, create a global symlink:
   ```bash
   npm link
   ```

2. In your project (where you want to test the module), link the globally symlinked module:
   ```bash
   npm link <your-module-name>
   ```
   For example, if your module's name is `my-module`, run:
   ```bash
   npm link my-module
   ```

3. Any changes you make to your module will now be reflected immediately in the linked project.

### Unlinking Your Module

If you no longer need the local version of your module:

1. Unlink it in your project:
   ```bash
   npm unlink <your-module-name>
   ```

2. Remove the global symlink in your module's directory:
   ```bash
   npm unlink
   ```

---

## 🛠 Publishing to NPM

Follow these steps to publish your module to npm:

1. Log in to your npm account:
   ```bash
   npm login
   ```

2. Publish your package:
   ```bash
   npm publish --access public
   ```

---

## 🚀 Deploying a New Version to NPM

Use Changesets to manage version updates and releases:

1. Add a changeset file describing the changes:
   ```bash
   npx changeset add
   ```

2. Update the `package.json` version based on the changeset:
   ```bash
   npx changeset version
   ```

3. Commit the changes:
   ```bash
   git add .
   git commit -m "Apply changeset version"
   ```

4. Push the changes to your branch:
   ```bash
   git push origin your-branch
   ```

5. Merge the changes into the `main` branch:
   ```bash
   git checkout main
   git pull origin main
   ```

6. Publish the new version:
   ```bash
   npx changeset publish
   ```

---

## 🛠 Available Scripts

Here are the scripts available in this project:

- **`build`**: Compiles TypeScript code.
- **`test`**: Runs tests with Vitest.
- **`format`**: Formats code using Prettier.
- **`check-format`**: Checks code formatting without applying changes.
- **`check-exports`**: Verifies package exports compatibility.
- **`local-release`**: Manages versioning and local publishing with Changesets.
- **`update`**: Updates dependencies and the project.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE). Feel free to adapt it to your needs!

---

## 📌 Useful Links

- **Homepage**: [GitHub Repository](https://github.com/JKS9/ts-npm-starter#readme)
- **Report an Issue**: [Issue Tracker](https://github.com/JKS9/ts-npm-starter/issues)