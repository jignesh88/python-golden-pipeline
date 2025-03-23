# Python Golden Pipeline

A comprehensive CI/CD pipeline template for Python applications, following modern best practices.

## Features

- **Comprehensive Testing**: Unit tests with pytest and coverage reporting
- **Code Quality**: Style checking with Black, isort, Flake8, and static type checking with MyPy
- **Security Scanning**: Vulnerability and code security scanning with Bandit and Safety
- **Containerization**: Multi-stage Docker builds with security best practices
- **CI/CD Pipeline**: GitHub Actions workflow for automated testing, building, and deployment
- **Multi-Environment Deployment**: Separate staging and production deployment pipelines

## Pipeline Stages

1. **Lint**: Code quality checks
2. **Test**: Run tests on multiple Python versions
3. **Security Scan**: Check for vulnerabilities and security issues
4. **Build**: Build Python package
5. **Docker**: Build and push container image
6. **Deploy**: Deploy to staging (from develop branch) or production (from main/master)

## Getting Started

### Prerequisites

- Python 3.8+ installed
- Docker installed (for local container testing)
- Git

### Installation

1. Clone this repository
2. Install development dependencies:

```bash
pip install -r requirements-dev.txt
```

### Local Development

```bash
# Run the application locally
python -m src.main

# Run tests
pytest

# Check code style
black --check .
isort --check .
flake8 .
mypy .

# Format code
black .
isort .
```

### Docker

```bash
# Build the Docker image
docker build -t python-app .

# Run the Docker container
docker run -p 8000:8000 python-app
```

## GitHub Actions Setup

To use this pipeline with GitHub Actions, you need to configure the following secrets:

- `CODECOV_TOKEN`: Token for uploading coverage reports to Codecov
- `KUBE_CONFIG_STAGING`: Kubernetes configuration for staging environment
- `KUBE_CONFIG_PRODUCTION`: Kubernetes configuration for production environment