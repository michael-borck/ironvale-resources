# ironvale-resources

Manages and organizes game resources for Ironvale using Jinja templating to generate configuration files and asset definitions. This repository provides a comprehensive system for managing game assets, configurations, and documentation through template-based generation.

## Overview

Ironvale Resources is a resource management system designed for game development that leverages Jinja2 templating to dynamically generate configuration files and asset definitions. The project combines multiple technologies to create a streamlined workflow for managing complex game resources, employee data, documentation, and game assets.

## Features

- **Template-Based Generation**: Uses Jinja2 templating to create dynamic configuration files
- **Asset Management**: Organize and manage game assets efficiently
- **Configuration Management**: Centralized configuration file generation
- **Documentation System**: Integrated support for policy documentation and guides
- **Multi-Language Support**: Built with Jinja, Python, JavaScript, and CSS
- **Automated Workflows**: GitHub Actions integration for CI/CD processes

## Installation

### Prerequisites

- Python 3.8 or higher
- Jinja2 templating engine
- Git

### Setup

1. Clone the repository:
```bash
git clone https://github.com/michael-borck/ironvale-resources.git
cd ironvale-resources
```

2. Install Python dependencies:
```bash
pip install -r requirements.txt
```

3. Install Jinja2 (if not included in requirements):
```bash
pip install jinja2
```

4. Verify the installation:
```bash
python -m jinja2 --version
```

## Usage

### Basic Template Processing

1. Place your Jinja template files in the appropriate content directory:
```
content/
├── docs/
├── employees/
├── jobs/
└── ...
```

2. Create your data configuration in `brief.yaml`:
```yaml
project: ironvale
version: 1.0.0
resources:
  - name: asset_name
    type: game_asset
    config: path/to/config
```

3. Generate output files:
```bash
python scripts/generate_resources.py
```

### Project Structure

```
ironvale-resources/
├── .github/
│   └── workflows/
│       └── pages.yml              # GitHub Pages deployment
├── content/
│   ├── docs/
│   │   ├── policy/                # Organization policies
│   │   └── support/               # Support documentation
│   ├── employees/                 # Employee profiles and data
│   ├── jobs/                      # Job definitions
│   └── ...
├── dist/
│   └── assets/                    # Generated assets
├── brief.yaml                     # Main configuration file
├── LICENSE                        # MIT License
└── README.md
```

### Key Directories

- **content/docs/policy/**: Organization policies including diversity and inclusion, health and safety guidelines
- **content/docs/support/**: User support documentation and FAQs
- **content/employees/**: Employee profiles and associated templates
- **content/jobs/**: Job configuration and definitions
- **dist/**: Generated output files and compiled assets

### Configuration

Edit `brief.yaml` to configure resource generation:

```yaml
project: ironvale
description: Game resource management system
templates_dir: content/
output_dir: dist/
```

## Documentation

Comprehensive documentation is available in the `content/docs/` directory:

- **Policies**: Organizational policies covering diversity, inclusion, health, and safety
- **Support Guides**: User guides including FIFO roster information, environmental rehabilitation programs, and autonomous haulage FAQs

## Development

### Local Development

1. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install development dependencies:
```bash
pip install -r requirements-dev.txt
```

3. Run tests:
```bash
pytest
```

### Contributing

1. Create a feature branch:
```bash
git checkout -b feature/your-feature-name
```

2. Commit your changes:
```bash
git commit -m "Add your commit message"
```

3. Push to the branch:
```bash
git push origin feature/your-feature-name
```

4. Open a pull request

## Deployment

The project uses GitHub Actions for automated deployment. Configuration is defined in `.github/workflows/pages.yml` for GitHub Pages hosting.

To deploy:

1. Push changes to the main branch
2. GitHub Actions will automatically trigger the build and deployment
3. Output will be available on GitHub Pages

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support inquiries, documentation, and FAQs, please refer to the comprehensive guides in `content/docs/support/`.

For employee-specific information or organizational policies, consult the relevant documentation in `content/docs/policy/`.

## Author

Created and maintained by [michael-borck](https://github.com/michael-borck)

---

For more information about Ironvale Resources, please explore the documentation structure or open an issue on GitHub.