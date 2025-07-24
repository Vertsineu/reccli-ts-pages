# RecCLI TypeScript Documentation

This repository contains the documentation for RecCLI TypeScript, hosted at [vertsineu.github.io/reccli-ts-pages](https://vertsineu.github.io/reccli-ts-pages).

## Development

### Prerequisites

- Python 3.x
- pip

### Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/Vertsineu/reccli-ts-pages.git
   cd reccli-ts-pages
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

### Local Development

To serve the documentation locally:

```bash
mkdocs serve
```

This will start a local development server at [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

### Building

To build the static site:

```bash
mkdocs build
```

This will create a `site` directory with the built documentation.

### Deployment

The documentation is automatically deployed to GitHub Pages when changes are pushed to the `master` branch. The GitHub Actions workflow handles the build and deployment process.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0) - see the [LICENSE](LICENSE) file for details.

[![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
