# Contributing to IJORAS Citation Converter

Thank you for your interest in contributing to the IJORAS Citation Converter! We welcome contributions from the community.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Getting Started](#getting-started)
- [Development Guidelines](#development-guidelines)
- [Submitting Changes](#submitting-changes)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)

## Code of Conduct

This project adheres to a simple code of conduct:

- Be respectful and inclusive
- Welcome newcomers
- Focus on constructive criticism
- Help others learn and grow

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When creating a bug report, include:

- **Clear title** - Descriptive and specific
- **Steps to reproduce** - Detailed steps to recreate the issue
- **Expected behavior** - What should happen
- **Actual behavior** - What actually happens
- **Screenshots** - If applicable
- **Environment** - Browser, OS, version
- **Additional context** - Any other relevant information

**Example bug report:**

```markdown
**Title:** Dark mode toggle doesn't persist after refresh

**Steps to reproduce:**
1. Open index.html in Chrome
2. Toggle dark mode on
3. Refresh the page

**Expected:** Dark mode should remain enabled
**Actual:** Page returns to light mode

**Browser:** Chrome 120.0.6099.109
**OS:** Windows 11
```

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:

- **Clear title** - Descriptive feature name
- **Detailed description** - Explain the feature
- **Use cases** - Why would this be useful?
- **Examples** - Show how it would work
- **Alternatives** - Other solutions you've considered

**Example enhancement:**

```markdown
**Title:** Add BibTeX export format

**Description:**
Add ability to export references in BibTeX format alongside TXT and HTML.

**Use cases:**
- Researchers using LaTeX need BibTeX format
- Easy integration with reference managers
- Common academic format

**Example:**
Export button with options: TXT | HTML | BibTeX

**Alternatives:**
- Manual conversion tools
- Third-party services
```

## Getting Started

### Prerequisites

- A text editor (VS Code, Sublime Text, etc.)
- Git for version control
- A modern web browser
- Basic knowledge of HTML, CSS, and JavaScript

### Setup

1. **Fork the repository**
   ```bash
   # Click "Fork" on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR_USERNAME/IJORAS-citation-convertor.git
   cd IJORAS-citation-convertor
   ```

3. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```

4. **Make your changes**
   - Edit files as needed
   - Test thoroughly in multiple browsers

5. **Test your changes**
   - Open `index.html` in browsers (Chrome, Firefox, Safari)
   - Test all features
   - Check responsive design
   - Verify dark mode
   - Test keyboard shortcuts

## Development Guidelines

### Code Style

#### HTML
- Use 2 spaces for indentation
- Use semantic HTML5 elements
- Include proper ARIA labels for accessibility
- Keep structure clean and organized

```html
<!-- Good -->
<button class="btn-primary" onclick="convertReferences()">
  Convert References
</button>

<!-- Avoid -->
<div onclick="convertReferences()">Convert References</div>
```

#### CSS
- Use CSS custom properties (variables) for theming
- Follow BEM-like naming conventions
- Group related styles together
- Comment complex sections

```css
/* Good */
.button-group {
  display: flex;
  gap: 10px;
  margin-top: 15px;
}

/* Component-specific styles */
.btn-primary {
  background-color: var(--accent-color);
  color: white;
}
```

#### JavaScript
- Use descriptive function and variable names
- Add comments for complex logic
- Follow existing code patterns
- Use modern ES6+ features
- Handle errors gracefully

```javascript
// Good
async function convertReferences() {
  const apiKey = getApiKey();
  if (!apiKey) {
    showNotification('Please enter API key', 'error');
    return;
  }
  // ... rest of code
}

// Avoid
async function conv() {
  let k = document.getElementById('apiKeyInput').value;
  // ... unclear code
}
```

### File Structure

```
IJORAS-citation-convertor/
├── index.html                    # Main application
├── README.md                     # Documentation
├── CONTRIBUTING.md               # This file
├── LICENSE                       # MIT License
├── .gitignore                    # Git ignore rules
├── IJORAS converter stable version.html  # Legacy
└── IJORAS_convertor.html        # Legacy
```

### Features to Consider

When adding new features, consider:

1. **User Experience**
   - Is it intuitive?
   - Does it improve workflow?
   - Is it accessible?

2. **Performance**
   - Does it slow down the app?
   - Are API calls optimized?
   - Is it efficient?

3. **Compatibility**
   - Works on all major browsers?
   - Mobile responsive?
   - Backwards compatible?

4. **Security**
   - No XSS vulnerabilities?
   - API key properly handled?
   - Input properly validated?

### Testing Checklist

Before submitting, test:

- ✅ All buttons and interactions work
- ✅ Keyboard shortcuts function correctly
- ✅ Dark mode toggles properly
- ✅ API key saves and loads
- ✅ Reference conversion works
- ✅ Copy to clipboard works
- ✅ Export functions work (TXT, HTML)
- ✅ Notifications display correctly
- ✅ Responsive on mobile/tablet
- ✅ No console errors
- ✅ Works in Chrome, Firefox, Safari

## Submitting Changes

### Pull Request Process

1. **Update documentation**
   - Update README.md if needed
   - Add comments to complex code
   - Update CHANGELOG if applicable

2. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add BibTeX export functionality"
   ```

   **Commit message format:**
   - `feat:` - New feature
   - `fix:` - Bug fix
   - `docs:` - Documentation only
   - `style:` - Formatting, missing semicolons, etc.
   - `refactor:` - Code restructuring
   - `test:` - Adding tests
   - `chore:` - Maintenance tasks

3. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

4. **Create Pull Request**
   - Go to the original repository on GitHub
   - Click "New Pull Request"
   - Select your branch
   - Fill out the PR template:

   ```markdown
   ## Description
   Brief description of changes

   ## Type of Change
   - [ ] Bug fix
   - [ ] New feature
   - [ ] Documentation update
   - [ ] Refactoring

   ## Testing
   - [ ] Tested in Chrome
   - [ ] Tested in Firefox
   - [ ] Tested in Safari
   - [ ] Mobile responsive checked
   - [ ] Dark mode works

   ## Screenshots
   (if applicable)

   ## Additional Notes
   Any other relevant information
   ```

5. **Respond to feedback**
   - Address review comments
   - Make requested changes
   - Be respectful and constructive

## Common Contribution Ideas

### Easy (Good for beginners)
- Fix typos in documentation
- Improve error messages
- Add more example references
- Enhance keyboard shortcuts
- Improve accessibility

### Medium
- Add new export formats (BibTeX, RIS, EndNote)
- Implement drag-and-drop file upload
- Add citation style templates
- Improve prompt for better AI accuracy
- Add reference preview mode

### Advanced
- Implement batch processing for multiple files
- Add browser extension version
- Create API wrapper
- Implement offline mode with service workers
- Add automated testing suite

## Questions?

If you have questions:

1. Check existing issues and discussions
2. Read the documentation thoroughly
3. Open a new issue with the "question" label

## Recognition

Contributors will be recognized in:
- README.md contributors section
- Release notes
- Project acknowledgments

Thank you for contributing to make this tool better for the academic community!

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
