# Contributing

Thank you for your interest in contributing to RecCLI TypeScript! This document provides guidelines and instructions for contributing to the project.

## Code of Conduct

Please read and follow our [Code of Conduct](https://github.com/Vertsineu/reccli-ts-pages/blob/master/CODE_OF_CONDUCT.md) to ensure a positive and inclusive community.

## How to Contribute

There are many ways to contribute to RecCLI TypeScript:

- Reporting bugs
- Suggesting enhancements
- Writing documentation
- Submitting code changes
- Reviewing pull requests

## Development Setup

To set up the project for development:

1. Fork the repository
2. Clone your fork:
   ```bash
   git clone https://github.com/your-username/reccli-ts.git
   cd reccli-ts
   ```
3. Install dependencies:
   ```bash
   npm install
   ```
4. Build the project:
   ```bash
   npm run build
   ```

## Development Workflow

1. Create a new branch for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```
2. Make your changes
3. Run tests:
   ```bash
   npm test
   ```
4. Commit your changes using conventional commit messages:
   ```bash
   git commit -m "feat: add new feature"
   ```
5. Push your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
6. Create a pull request

## Pull Request Guidelines

- Fill in the required template
- Include tests for new features
- Update documentation as needed
- Follow the coding style
- Make sure all tests pass

## Commit Message Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/) for commit messages:

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code changes that neither fix bugs nor add features
- `perf`: Performance improvements
- `test`: Adding or fixing tests
- `chore`: Changes to the build process or tools

## Documentation

If you're updating documentation, you can preview the changes locally:

```bash
npm run docs:serve
```

This will start a local server with the documentation site.

## License

By contributing to RecCLI TypeScript documentation, you agree that your contributions will be licensed under the project's Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0). See the [License](license.md) page for more details.
