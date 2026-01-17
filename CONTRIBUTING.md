# Contributing

Thank you for your interest in contributing to JetBrains Optimal Dark! Here's how you can help.

## How to Contribute

### Reporting Issues

1. Check if the issue already exists in [Issues](../../issues)
2. If not, create a new issue with:
   - Your JetBrains IDE and version
   - The language/file type affected
   - Screenshots showing the issue
   - Description of the expected vs actual behavior

### Suggesting Improvements

1. Open an issue with the `enhancement` label
2. Describe the color change and why it would improve readability
3. Reference the design hierarchy (CRITICAL, IMPORTANT, DATA, STRUCTURE, METADATA, FEEDBACK)

### Submitting Changes

1. Fork the repository
2. Create a new branch (`git checkout -b feature/my-feature`)
3. Make your changes
4. Test the theme in a JetBrains IDE
5. Commit with a clear message (`git commit -m "Add feature X"`)
6. Push to your fork (`git push origin feature/my-feature`)
7. Open a Pull Request

## Guidelines

### Language

- All code, comments, and documentation must be in **American English**
- Exception: `jose/` folder (personal notes)

### Theme Modifications

When proposing color changes, follow the design hierarchy:

| Level | Elements | Treatment |
|-------|----------|-----------|
| **CRITICAL** | Keywords, errors, functions | Vivid saturated colors |
| **IMPORTANT** | Numbers, parameters, escapes | Distinctive colors |
| **DATA** | Strings, comments | Soft desaturated colors |
| **STRUCTURE** | Operators, punctuation | Neutral gray |
| **METADATA** | Annotations, tags | Tertiary colors |
| **FEEDBACK** | Warnings, TODO, deprecated | Semantic colors |

### Testing

Before submitting:

1. Import the theme in a JetBrains IDE
2. Test with multiple languages (Java, Python, JavaScript, HTML/CSS, etc.)
3. Verify the visual hierarchy is maintained
4. Check for accessibility (sufficient contrast)

## Questions?

Feel free to open an issue if you have questions about contributing.
