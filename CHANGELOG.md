## 📄 `CHANGELOG.md`

All notable changes to will be documented in this file.

## [0.0.3] - 2025-06-12
Bug Fixes:
- Name Validation: Enforced stricter validation rules to ensure names only contain letters, numbers, and hyphens. An appropriate error message is displayed for invalid inputs.
- Directory Structure: Adjusted logic for non-component artifacts to prevent unnecessary directory creation.

## [0.0.2] - 2025-05-17
Bug Fixes:
- Fixed target directory issue: Generated files now correctly respect the selected output path instead of always defaulting to src/app.

New Features
- Directive
- Guard – includes type selection (CanActivate, CanActivateChild, CanDeactivate, CanMatch)
- Interceptor
- Resolver
- Enum
- Interface
- Class 

## [0.0.1] - 2025-05-17

### Initial release
- Initial version of Angular Code Generator
- Command: `Angular: Generate Template`
- Generator support for:
  - Component
  - Service
  - Pipe
