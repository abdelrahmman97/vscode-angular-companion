# 📦 Angular Companion 
**Your Angular Companion 😍**

A Visual Studio Code extension that helps you quickly generate Angular files like components, services, pipes, and more using pre-defined templates with extensive customization options.

Built with ❤️ for Angular 15 and later versions.

## ✨ Features

### Artifact Generation
Generate 13 different Angular artifact types:
- **Component** - With customizable options (standalone, inline styles/template, change detection, view encapsulation)
- **Service** - Injectable services with test files
- **Pipe** - Custom pipes with transform logic
- **Directive** - Attribute and structural directives
- **Guard** - Route guards (CanActivate, CanActivateChild, CanDeactivate, CanMatch, CanLoad)
- **Interceptor** - HTTP interceptors
- **Resolver** - Route resolvers
- **Module** - NgModules with optional routing
- **Feature** - Complete feature scaffolding (component + service + module + routing)
- **Store** - NgRx store files (actions, reducers, effects, selectors)
- **Enum** - TypeScript enums
- **Interface** - TypeScript interfaces
- **Class** - TypeScript classes

### Smart Features
- **Angular Project Detection** - Automatically detects Angular projects and validates configuration
- **Component Options** - Customize component generation with inline styles/templates, change detection strategy, view encapsulation
- **Test File Generation** - Automatically generates test files for all artifacts (Jasmine/Jest support)
- **Batch Generation** - Generate multiple artifacts in one go
- **Custom Templates** - Use your own Handlebars templates for complete customization
- **Smart Path Detection** - Intelligent directory suggestions based on Angular conventions
- **Generation History** - Tracks recently generated artifacts for quick access

## 🛠️ Usage

### Basic Generation

1. **Via Command Palette:**
   - Open the command palette (Ctrl+Shift+P / Cmd+Shift+P)
   - Run `Angular companion: Generate Template` or for short `Companion: Generate`
   - Select the artifact type you want to generate
   - Enter a name (letters, numbers, and hyphens only)
   - Select target directory (or use default)

2. **Via Context Menu:**
   - Right-click on any folder in the Explorer
   - Select `Angular companion: Generate Template`
   - Follow the prompts

### Component Generation Options

When generating a component, you'll be prompted for:

- **Inline Template** - Embed HTML directly in TypeScript or use separate file
- **Inline Styles** - Embed CSS directly in TypeScript or use separate file
- **Skip Tests** - Generate test file or skip it
- **Change Detection** - Default or OnPush strategy
- **View Encapsulation** - Emulated (default), None (global styles), or ShadowDom
- **Standalone** - Standalone component (Angular 14+) or module-based

Your choices are remembered for the next generation!

### Batch Generation

Generate multiple artifacts quickly:

1. Open command palette (Ctrl+Shift+P / Cmd+Shift+P)
2. Run `Angular companion: Batch Generate` or `Companion: Batch Generate`
3. Enter the number of items to generate (1-20)
4. Follow the prompts for each item

### Custom Templates

Use your own templates to customize generated code:

1. **Setup:**
   - Create a `.angular-companion/templates` folder in your workspace root (or configure custom path)
   - Mirror the structure: `templates/<artifact-type>/<template-file>.hbs`
   - Example: `templates/component/component.ts.hbs`

2. **Template Variables:**
   - `{{name}}` - Artifact name (kebab-case)
   - `{{className}}` - Class name (PascalCase)
   - `{{selector}}` - Component selector
   - `{{projectPrefix}}` - Project prefix from angular.json
   - `{{_generatedAt}}` - ISO timestamp of generation
   - Plus all component-specific options

3. **Configuration:**
   - Set `angularCompanion.templatesRoot` in VS Code settings to use a custom templates directory

4. **Template Marketplace:**
   - Run `Angular companion: Open Template Marketplace` to discover community templates

## ⚙️ Configuration

All settings are available in VS Code Settings (Preferences → Settings → Extensions → Angular Companion):

### Component Options
- `angularCompanion.component.standalone` - Default standalone option (default: `true`)
- `angularCompanion.component.inlineStyle` - Default inline style option (default: `false`)
- `angularCompanion.component.inlineTemplate` - Default inline template option (default: `false`)
- `angularCompanion.component.skipTests` - Default skip tests option (default: `false`)
- `angularCompanion.component.changeDetection` - Default change detection strategy: `Default` or `OnPush` (default: `OnPush`)
- `angularCompanion.component.viewEncapsulation` - Default view encapsulation: `Emulated`, `None`, or `ShadowDom` (default: `Emulated`)

### Test Framework
- `angularCompanion.testFramework` - Test framework: `Jasmine` or `Jest` (default: `Jasmine`)

### Paths
- `angularCompanion.defaultTargetDirectory` - Default target directory for generated files (relative to workspace root)
- `angularCompanion.templatesRoot` - Custom templates directory path (default: `.angular-companion/templates`)

### Project Settings
- `angularCompanion.projectPrefix` - Project prefix for component selectors (overrides angular.json prefix)

## 📋 Commands

- **`Angular companion: Generate Template`** - Generate a single Angular artifact
- **`Angular companion: Batch Generate`** - Generate multiple artifacts in sequence
- **`Angular companion: Open Template Marketplace`** - Open template marketplace in browser

## 🎯 Angular Project Detection

The extension automatically:
- Detects if your workspace is an Angular project (checks for `angular.json` and `package.json`)
- Validates Angular version and adjusts templates accordingly
- Auto-detects project prefix from `angular.json`
- Shows warnings if used outside Angular projects (with option to continue)

## 🙋‍♂️ Contributing

Contributions are welcome! Here's how you can help:

- Report bugs or suggest features by opening an issue.
- Submit pull requests to fix bugs or add new features.
- Share your custom templates with the community!

We appreciate your support!

**Enjoy! 😉**

📄 License
MIT License © [Abdelrahman Mahmoud](https://github.com/abdelrahmman97)
