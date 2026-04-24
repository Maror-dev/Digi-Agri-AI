# 🤝 Contributing to Digi-Agri AI

Thank you for your interest in contributing to Digi-Agri AI! This document provides guidelines and instructions for contributing.

## Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inspiring community for all. We treat all members with respect and dignity, regardless of their experience level, background, or identity.

### Expected Behavior
- Be respectful and inclusive
- Use welcoming and inclusive language
- Focus on constructive criticism
- Respect differing opinions and experiences

### Unacceptable Behavior
- Harassment, discrimination, or exclusion
- Offensive comments or unwelcome attention
- Trolling or disruptive behavior
- Publishing private information without consent

## How to Contribute

### 1. **Reporting Bugs**

Before submitting a bug report, check if it's already been reported. When creating a bug report:

- Use a clear, descriptive title
- Describe the exact steps to reproduce the problem
- Provide specific examples to demonstrate those steps
- Describe the observed behavior
- Explain the expected behavior and why
- Include screenshots if applicable
- Include device/environment information (OS, Flutter version, etc.)

**Example Bug Report:**
```
Title: Chat responses not showing in Dinka language

Description:
- When user selects Dinka as language and asks "How much fertilizer?"
- Response appears in English instead of Dinka
- Tested on Android 11 with Flutter 3.0

Steps to Reproduce:
1. Install app
2. Complete onboarding, select Dinka language
3. Open Chat tab
4. Ask any question
5. See response in English

Expected: Response in Dinka
Actual: Response in English
```

### 2. **Suggesting Features**

Feature suggestions should:
- Have a clear title describing the enhancement
- Provide a step-by-step description of the suggested enhancement
- Explain why this enhancement would be useful
- List alternative solutions or features already considered

**Example Feature Request:**
```
Title: Add reminder notifications for fertilizer application

Description:
When farmer sets fertilizer application schedule, app should send
notifications 1 day before application is due.

Use Case:
Many farmers forget scheduled applications. Reminders would improve
adherence to recommendations and yield outcomes.

Alternative Solutions:
- Weekly digest email (less effective for low-literacy users)
- Chat-based reminders (harder to implement offline)
```

### 3. **Pull Requests**

#### Before You Start
1. **Fork the repository**
   ```bash
   git clone https://github.com/Maror-dev/digi-agri-ai.git
   cd digi-agri-ai
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Set up development environment**
   ```bash
   bash scripts/setup.sh
   ```

#### Making Changes

1. **Follow code style guidelines** (See REPOSITORY_GUIDE.md)
   - Run linters: `bash scripts/lint.sh`
   - Format code: `dart format`, `black`, etc.

2. **Write tests for new features**
   ```bash
   bash scripts/test.sh
   ```

3. **Update documentation**
   - Add docstrings to functions/classes
   - Update README if needed
   - Update API docs if API changes

4. **Commit with clear messages**
   ```bash
   git commit -m "feat(pest-detector): Add new pest classification model
   
   - Integrated EfficientNet-B2 model
   - Achieved 92% accuracy on test set
   - Model size: 18MB (optimized for mobile)
   
   Closes #123"
   ```

5. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

#### Creating the PR

1. Go to GitHub and create a Pull Request
2. Use the PR template (auto-fills when you create PR)
3. Fill in all sections:
   - **Description:** What does this PR do?
   - **Type:** feat/fix/docs/test/refactor/perf/chore
   - **Related Issue:** Link issue being addressed
   - **Testing:** How was this tested?
   - **Checklist:** Confirm all items are complete

**Example PR Template:**
```markdown
## Description
Implements computer vision pest detection using EfficientNet model.

## Type of Change
- [x] New feature (non-breaking change)
- [ ] Bug fix (non-breaking change)
- [ ] Breaking change
- [ ] Documentation update

## Related Issues
Closes #42
Related to #38

## Testing
- [x] Unit tests written and passing
- [x] Widget tests passing
- [x] Tested on Android and iOS
- [x] Tested on devices with <2GB RAM

## Screenshots (if applicable)
[Add screenshots here]

## Checklist
- [x] Code follows style guidelines
- [x] Self-review completed
- [x] Comments added for complex code
- [x] Documentation updated
- [x] No new warnings generated
- [x] Tests added and passing
- [x] No breaking changes
```

#### PR Review Process

1. **Automated Checks**
   - CI/CD pipeline runs tests
   - Linters check code style
   - Coverage is checked

2. **Code Review**
   - At least 2 maintainers review
   - Address feedback constructively
   - Update PR as needed

3. **Approval & Merge**
   - Get 2+ approvals
   - Resolve conflicts if any
   - Merge to develop

## Development Setup

### Prerequisites
- Git
- Flutter 3.x+
- Python 3.8+
- Node.js 16+
- Firebase account

### Quick Start

```bash
# Clone repository
git clone https://github.com/Maror-dev/digi-agri-ai.git
cd digi-agri-ai

# Run setup
bash scripts/setup.sh

# Configure environment
cp .env.example .env
# Edit .env with your API keys

# Run tests
bash scripts/test.sh

# Start development
cd mobile_app
flutter run
```

## Coding Standards

### Dart/Flutter
- Follow [Effective Dart](https://dart.dev/guides/language/effective-dart)
- Use `dart analyze` for static analysis
- Use `dart format` for formatting
- Write comprehensive dartdoc comments
- Aim for 80%+ test coverage

### Python
- Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/)
- Use `pylint` and `flake8` for linting
- Use `black` for formatting
- Write comprehensive docstrings
- Aim for 80%+ test coverage

### TypeScript
- Follow [Google TypeScript Style Guide](https://google.github.io/styleguide/tsguide.html)
- Use `eslint` for linting
- Use `prettier` for formatting
- Write TSDoc comments
- Aim for 80%+ test coverage

## Documentation

### Writing Documentation

1. **In-Code Comments**
   - Explain the "why", not the "what"
   - Use clear, concise language
   - Keep comments up-to-date

2. **README Files**
   - Add README.md to new directories
   - Include purpose, quick start, and key info

3. **API Documentation**
   - Update API_REFERENCE.md for API changes
   - Include request/response examples
   - Document error codes

4. **Architecture Documentation**
   - Update ARCHITECTURE.md for major changes
   - Use diagrams where helpful
   - Document design decisions

## Community

### Communication Channels
- **GitHub Issues:** Bug reports and feature requests
- **GitHub Discussions:** Architecture and design discussions
- **Slack:** Real-time communication (if team member)

### Getting Help

- Check existing issues and discussions
- Read REPOSITORY_GUIDE.md and APP_BLUEPRINT.md
- Ask questions in GitHub Discussions
- Reach out to maintainers on Slack

## Recognition

We recognize and appreciate all contributions! Contributors are:
- Added to CONTRIBUTORS.md
- Thanked in release notes
- Recognized in project documentation

## Questions?

Feel free to open a GitHub Discussion or reach out to maintainers.

Thank you for contributing to Digi-Agri AI! 🌾
