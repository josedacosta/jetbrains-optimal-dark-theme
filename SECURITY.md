# Security Policy

## Scope

This repository contains a color scheme file (`.icls`) for JetBrains IDEs. The theme file is a static XML configuration that:

- Does **not** execute any code
- Does **not** collect, transmit, or store any user data
- Does **not** modify system files
- Only changes the visual appearance of the IDE editor

## Reporting a Vulnerability

If you discover a security issue in the theme file, please report it by:

1. **Do NOT** open a public issue
2. Use GitHub's private vulnerability reporting feature
3. Include:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

## Security Considerations

### What This Theme Does

- Defines colors for syntax highlighting
- Defines colors for IDE interface elements
- Uses standard JetBrains color scheme format

### What This Theme Does NOT Do

- Execute any code or scripts
- Access the filesystem
- Make network requests
- Collect any user data
- Modify IDE settings beyond colors

## Best Practices

1. **Download from official sources** - Only use the theme from this repository
2. **Verify file integrity** - The `.icls` file should only contain XML color definitions
3. **Review before importing** - You can open the theme file in a text editor to verify its contents
