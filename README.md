# Python Golden Pipeline

A comprehensive CI/CD pipeline template for Python applications, following modern best practices.

## Repository Structure

All pipeline files are located in the `python-pipeline` directory and include:

- **GitHub Actions Workflow**: Comprehensive CI/CD pipeline definition
- **Docker Configuration**: Optimized multi-stage Dockerfile
- **Testing Setup**: pytest configuration with coverage reporting
- **Code Quality Tools**: Black, isort, Flake8, and MyPy configuration
- **Security Scanning**: Bandit and Safety setup
- **Sample Application**: A minimal FastAPI application

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

See the README.md file in the `python-pipeline` directory for detailed instructions on how to use this template.