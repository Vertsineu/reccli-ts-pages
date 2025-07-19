# Installation

This page explains how to install RecCLI TypeScript in your project.

## Prerequisites

Before installing RecCLI TypeScript, make sure you have the following prerequisites:

- Node.js (version 14 or higher)
- npm or yarn

## Installing with npm

To install RecCLI TypeScript using npm, run the following command in your project directory:

```bash
npm install reccli-ts
```

## Installing with yarn

If you prefer yarn, you can install RecCLI TypeScript with:

```bash
yarn add reccli-ts
```

## TypeScript Configuration

RecCLI TypeScript works best with TypeScript projects. Make sure your `tsconfig.json` includes the following settings:

```json
{
  "compilerOptions": {
    "target": "ES2018",
    "module": "CommonJS",
    "moduleResolution": "node",
    "esModuleInterop": true,
    "lib": ["ES2018", "ESNext"],
    "declaration": true,
    "strict": true
  }
}
```

## Verifying Installation

To verify that RecCLI TypeScript has been installed correctly, you can create a simple TypeScript file:

```typescript
// test.ts
import { RecCLI } from 'reccli-ts';

console.log('RecCLI TypeScript installed successfully!');

const cli = new RecCLI()
  .name('test-cli')
  .version('0.0.1');

console.log(cli);
```

Then compile and run it:

```bash
npx tsc test.ts
node test.js
```

If everything is working correctly, you should see a success message and the CLI instance logged to the console.
