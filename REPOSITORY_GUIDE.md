# 📂 Digi-Agri AI Repository Guide

## Repository Structure

```
digi-agri-ai/
├── mobile_app/                     # Flutter frontend application
│   ├── lib/
│   │   ├── main.dart               # App entry point
│   │   ├── screens/                # UI screens
│   │   │   ├── auth/
│   │   │   ├── onboarding/
│   │   │   ├── dashboard/
│   │   │   ├── features/           # Feature screens
│   │   │   │   ├── fertilizer/
│   │   │   │   ├── pest_identifier/
│   │   │   │   ├── chat/
│   │   │   │   ├── progress_tracker/
│   │   │   │   └── marketplace/
│   │   │   └── common/
│   │   ├── providers/              # Riverpod state management
│   │   │   ├── auth_provider.dart
│   │   │   ├── crop_provider.dart
│   │   │   └── ...
│   │   ├── models/                 # Data models
│   │   │   ├── user_model.dart
│   │   │   ├── crop_model.dart
│   │   │   └── ...
│   │   ├── services/               # Business logic
│   │   │   ├── auth_service.dart
│   │   │   ├── firebase_service.dart
│   │   │   ├── ml_service.dart
│   │   │   └── ...
│   │   ├── widgets/                # Reusable UI components
│   │   │   ├── buttons/
│   │   │   ├── cards/
│   │   │   ├── inputs/
│   │   │   └── ...
│   │   ├── utils/                  # Helper functions
│   │   │   ├── constants.dart
│   │   │   ├── validators.dart
│   │   │   └── ...
│   │   └── config/
│   │       └── routes.dart
│   ├── assets/
│   │   ├── images/
│   │   ├── icons/
│   │   ├── models/                 # TensorFlow Lite models
│   │   │   ├── pest_detector.tflite
│   │   │   ├── soil_analyzer.tflite
│   │   │   └── ...
│   │   └── fonts/
│   ├── test/                       # Unit & widget tests
│   │   ├── unit/
│   │   ├── widget/
│   │   └── integration/
│   ├── pubspec.yaml                # Flutter dependencies
│   ├── pubspec.lock
│   ├── README.md
│   └── .gitignore
│
├── backend/                        # Backend services
│   ├── functions/                  # Firebase Cloud Functions
│   │   ├── index.ts                # Entry point
│   │   ├── fertilizer.ts           # Fertilizer recommendations
│   │   ├── pest.ts                 # Pest detection API
│   │   ├── chat.ts                 # Chat API
│   │   ├── predictions.ts          # Yield predictions
│   │   └── ...
│   ├── ml_models/                  # ML model training
│   │   ├── pest_classifier/
│   │   │   ├── train.py
│   │   │   ├── evaluate.py
│   │   │   ├── requirements.txt
│   │   │   └── ...
│   │   ├── soil_analyzer/
│   │   ├── yield_predictor/
│   │   └── chatbot/
│   ├── api/                        # REST API (if separate from functions)
│   │   ├── app.py
│   │   ├── routes/
│   │   ├── models/
│   │   └── ...
│   ├── scripts/                    # Utility scripts
│   │   ├── generate_models.py
│   │   ├── upload_models.py
│   │   └── ...
│   ├── requirements.txt            # Python dependencies
│   ├── package.json                # Node.js dependencies
│   ├── .env.example
│   ├── README.md
│   └── .gitignore
│
├── design/                         # UI/UX Design Assets
│   ├── wireframes/                 # Figma exports
│   │   ├── dashboard.png
│   │   ├── pest_identifier.png
│   │   └── ...
│   ├── colors/                     # Color palette
│   │   └── colors.json
│   ├── typography/                 # Font specifications
│   │   └── typography.json
│   ├── components/                 # Design system
│   │   ├── buttons.md
│   │   ��── cards.md
│   │   └── ...
│   └── README.md
│
├── docs/                           # Documentation
│   ├── APP_BLUEPRINT.md            # Complete specification (400+ pages)
│   ├── ROADMAP.md                  # 16-week development timeline
│   ├── REPOSITORY_GUIDE.md         # This file
│   ├── API_REFERENCE.md            # API documentation
│   ├── DATABASE_SCHEMA.md          # Firestore schema
│   ├── AI_MODELS.md                # ML model documentation
│   ├── DEPLOYMENT.md               # Deployment instructions
│   ├── CONTRIBUTING.md             # Contribution guidelines
│   ├── ARCHITECTURE.md             # System architecture
│   ├── SECURITY.md                 # Security guidelines
│   └── README.md
│
├── scripts/                        # Utility scripts
│   ├── setup.sh                    # Environment setup
│   ├── deploy.sh                   # Deployment script
│   ├── test.sh                     # Run all tests
│   ├── lint.sh                     # Code linting
│   └── generate_models.py          # Generate ML models
│
├── tests/                          # Integration tests
│   ├── e2e/                        # End-to-end tests
│   │   ├── auth.test.ts
│   │   ├── features.test.ts
│   │   └── ...
│   ├── api/                        # API tests
│   │   ├── fertilizer.test.ts
│   │   ├── pest.test.ts
│   │   └── ...
│   └── ml/                         # Model validation tests
│       ├── pest_detector.test.py
│       └── ...
│
├── .github/                        # GitHub configuration
│   ├── workflows/                  # GitHub Actions CI/CD
│   │   ├── ci.yml                  # Continuous Integration
│   │   ├── deploy.yml              # Deploy to production
│   │   ├── test.yml                # Run tests
│   │   └── lint.yml                # Code quality checks
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   ├── feature_request.md
│   │   └── ...
│   ├── pull_request_template.md    # PR template
│   └── README.md
│
├── README.md                       # Project overview
├── APP_BLUEPRINT.md                # Complete specification
├── ROADMAP.md                      # Development timeline
├── REPOSITORY_GUIDE.md             # This file
├── LICENSE                         # MIT License
├── .gitignore                      # Git ignore rules
├── .env.example                    # Environment template
└── CONTRIBUTING.md                 # Contribution guidelines
```

## File Naming Conventions

### Dart (Flutter)
- **Files:** `snake_case.dart`
  ```
  ✅ pest_detector.dart
  ✅ fertilizer_advisor.dart
  ❌ PestDetector.dart
  ```
- **Classes:** `PascalCase`
  ```dart
  class PestDetector { }
  ```
- **Functions/Variables:** `camelCase`
  ```dart
  void detectPest() { }
  var isLoading = false;
  ```
- **Constants:** `UPPER_SNAKE_CASE`
  ```dart
  const int MODEL_INPUT_SIZE = 224;
  ```

### Python
- **Files:** `snake_case.py`
  ```
  ✅ pest_classifier.py
  ✅ soil_analyzer.py
  ❌ PestClassifier.py
  ```
- **Classes:** `PascalCase`
  ```python
  class PestClassifier:
      pass
  ```
- **Functions/Variables:** `snake_case`
  ```python
  def detect_pest(image):
      pass
  ```
- **Constants:** `UPPER_SNAKE_CASE`
  ```python
  MODEL_INPUT_SIZE = 224
  ```

### TypeScript
- **Files:** `camelCase.ts` or `PascalCase.ts` (for classes)
  ```
  ✅ pestDetector.ts
  ✅ FertilizerAdvisor.ts
  ```
- **Classes:** `PascalCase`
  ```typescript
  class PestDetector { }
  ```
- **Functions/Variables:** `camelCase`
  ```typescript
  function detectPest() { }
  const isLoading = false;
  ```
- **Interfaces:** `PascalCase` (often with `I` prefix)
  ```typescript
  interface IPestDetectionResult { }
  ```

## Git Branch Strategy

### Branch Naming
```
main              # Production (stable releases)
develop           # Staging (integration branch)
feature/*         # New features
  feature/pest-detector
  feature/chat-assistant
bugfix/*          # Bug fixes
  bugfix/chat-crashes
  bugfix/offline-sync
docs/*            # Documentation
  docs/api-reference
refactor/*        # Refactoring
  refactor/state-management
test/*            # Testing improvements
  test/add-e2e-tests
```

### Branch Flow
```
┌─────────────────────────────────────────┐
│           main (production)             │ ← Stable releases only
└────────────────┬────────────────────────┘
                 │ (merge from develop)
┌────────────────▼────────────────────────┐
│           develop (staging)             │ ← Integration branch
└────────────────┬────────────────────────┘
         ┌───────┼───────┐
         │       │       │
    feature/ bugfix/ docs/
```

### Commit Message Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `style:` Code style (formatting, semicolons, etc.)
- `refactor:` Code refactoring
- `test:` Adding tests
- `chore:` Build, dependencies, CI/CD
- `perf:` Performance improvements

**Examples:**
```
feat(pest-detector): Add computer vision model for leaf spot detection

Implement EfficientNet-based pest detection with 92% accuracy.
Model size reduced to 18MB via quantization.

Closes #42

fix(chat): Resolve language encoding issue in Dinka responses

docs(readme): Update setup instructions for Python 3.8+

test(api): Add integration tests for fertilizer endpoint
```

## Pull Request Process

1. **Create Feature Branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make Changes**
   - Write clean, well-documented code
   - Follow code style guidelines
   - Add tests for new features
   - Update documentation

3. **Create Pull Request**
   - Use the PR template
   - Provide clear description
   - Link related issues (#42)
   - Request reviewers

4. **Pass Checks**
   - ✅ CI/CD tests pass
   - ✅ Code quality checks pass
   - ✅ No merge conflicts

5. **Code Review**
   - Address reviewer comments
   - Update PR based on feedback
   - Get approval from 2+ reviewers

6. **Merge**
   - Squash commits if needed
   - Merge to `develop`
   - Delete feature branch

7. **Release to Main**
   - Create release PR from `develop` to `main`
   - Tag version (semantic versioning)
   - Deploy to production

## Code Style Guidelines

### Dart (Flutter)
Follow [Effective Dart](https://dart.dev/guides/language/effective-dart)

```dart
// ✅ Good
class PestDetector {
  Future<PestDetectionResult> detectPest(String imagePath) async {
    // Implementation
  }
}

// ❌ Bad
class PestDetector{
  Future<PestDetectionResult> detectPest(String imagePath)async{
    // Implementation
  }
}
```

### Python
Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/)

```python
# ✅ Good
def detect_pest(image_path: str) -> PestDetectionResult:
    """Detect pests in the given image."""
    pass

# ❌ Bad
def detect_pest(imagePath):
    pass
```

### TypeScript
Follow [Google TypeScript Style Guide](https://google.github.io/styleguide/tsguide.html)

```typescript
// ✅ Good
export class PestDetector {
  async detectPest(imagePath: string): Promise<PestDetectionResult> {
    // Implementation
  }
}

// ❌ Bad
export class PestDetector {
  async detectPest(imagePath){return null;}
}
```

## Testing

### Running Tests

**Flutter Tests:**
```bash
cd mobile_app
flutter test
flutter test --coverage  # Generate coverage report
```

**Python Tests:**
```bash
cd backend
python -m pytest
python -m pytest --cov=.  # Generate coverage report
```

**All Tests:**
```bash
bash scripts/test.sh
```

### Test Structure

```
test/
├── unit/
│   ├── models/
│   ├── providers/
│   └── services/
├── widget/
│   └── screens/
└── integration/
    └── features/
```

### Test Coverage Targets
- **Unit Tests:** 80%+ coverage
- **Widget Tests:** 60%+ coverage
- **Integration Tests:** Key user flows

## Code Quality

### Linting

**Dart:**
```bash
cd mobile_app
dart analyze
```

**Python:**
```bash
cd backend
pylint *.py
flake8 .
```

**TypeScript:**
```bash
cd backend
npm run lint
```

### Code Formatting

**Dart:**
```bash
cd mobile_app
dart format .
```

**Python:**
```bash
cd backend
black .
```

**TypeScript:**
```bash
cd backend
npm run format
```

## Development Workflow

### Daily Workflow

1. **Start Day**
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/your-feature
   ```

2. **Development**
   - Write code
   - Test locally
   - Commit regularly with meaningful messages

3. **Before Pushing**
   ```bash
   bash scripts/test.sh          # Run tests
   bash scripts/lint.sh          # Lint code
   git push origin feature/your-feature
   ```

4. **Create PR**
   - Go to GitHub
   - Create PR from feature branch to develop
   - Fill in PR template

5. **Code Review**
   - Address feedback
   - Update PR
   - Get approvals

### Deployment Workflow

1. **Create Release Branch**
   ```bash
   git checkout -b release/v1.0.0 develop
   ```

2. **Update Version**
   - Update `pubspec.yaml` (Flutter)
   - Update `package.json` (Backend)
   - Update `CHANGELOG.md`

3. **Test Release**
   ```bash
   bash scripts/test.sh
   ```

4. **Merge to Main**
   ```bash
   git checkout main
   git merge --no-ff release/v1.0.0
   git tag -a v1.0.0 -m "Release version 1.0.0"
   git push origin main --tags
   ```

5. **Back to Develop**
   ```bash
   git checkout develop
   git merge --no-ff release/v1.0.0
   git push origin develop
   ```

6. **Deploy**
   - GitHub Actions automatically deploys from main
   - Monitor deployment in Actions tab

## CI/CD Pipelines

### Continuous Integration (On Every Push)
- Run tests
- Code linting
- Code coverage
- Security scanning

### Continuous Deployment (On Main Branch)
- Build Docker images
- Deploy to Firebase
- Deploy to App Stores
- Notify team

## Documentation Standards

### Code Documentation

**Dart:**
```dart
/// Detects pests in the provided image using ML model.
///
/// [imagePath] is the path to the image file.
/// Returns a [PestDetectionResult] with pest name and confidence.
Future<PestDetectionResult> detectPest(String imagePath) async {
  // Implementation
}
```

**Python:**
```python
def detect_pest(image_path: str) -> PestDetectionResult:
    """Detect pests in the provided image.
    
    Args:
        image_path: Path to the image file.
    
    Returns:
        PestDetectionResult with pest name and confidence.
    """
    pass
```

### README Files

Every major directory should have a README.md explaining:
- Purpose
- Quick start
- File structure
- Key classes/functions
- Development notes

## Communication

### Team Channels
- **Daily Standups:** 9 AM on Slack #digi-agri-standups
- **Issues:** GitHub Issues for feature requests & bugs
- **Discussions:** GitHub Discussions for architecture decisions
- **Documentation:** Notion for design docs & meeting notes

### Escalation Process

1. **Blocker:** Post in Slack #incidents immediately
2. **P1 Bug:** Create issue, assign to team lead
3. **P2 Bug:** Create issue for next sprint
4. **Architecture Question:** Start GitHub Discussion

## Additional Resources

- [Flutter Documentation](https://flutter.dev/docs)
- [Firebase Documentation](https://firebase.google.com/docs)
- [TensorFlow Lite Guide](https://www.tensorflow.org/lite)
- [Hugging Face API](https://huggingface.co/docs/api-inference)
- [GitHub Actions](https://docs.github.com/en/actions)

---

**Last Updated:** 2026-04-24
