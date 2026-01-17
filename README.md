# JetBrains Optimal Dark Theme

<div align="center">

![JetBrains Optimal Dark Theme Header](assets/header.jpeg)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![JetBrains IDEs](https://img.shields.io/badge/JetBrains-All%20IDEs-000000?logo=jetbrains)](https://www.jetbrains.com/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Optimized dark syntax highlighting theme for JetBrains IDEs**

*AI-designed for maximum readability and reduced eye strain*

</div>

---

## Introduction

**JetBrains Optimal Dark** is a syntax highlighting theme optimized for JetBrains IDEs (IntelliJ IDEA, WebStorm, PyCharm, PHPStorm, etc.). This theme was designed using artificial intelligence (LLM) to **maximize code readability** and **reduce eye strain** during long development sessions.

### Theme Goals

- **Improve visibility** of critical code elements (keywords, errors, functions)
- **Help developers** focus on what really matters
- **Reduce eye strain** with a comfortable dark background and balanced colors
- **Maximize clarity** by using distinctive colors for each element type

Every color choice was **analyzed and refined by AI** to optimize development efficiency.

---

## Installation

### Method 1: Direct Import (Recommended)

1. Open your JetBrains IDE
2. Press `Ctrl+Alt+S` (Windows/Linux) or `Cmd+,` (macOS) to open Settings
3. Navigate to `Editor` → `Color Scheme`
4. Click the gear icon (⚙️) → `Import Scheme...`
5. Select the `theme/Optimal_Dark.icls` file
6. Click `OK` to apply

### Method 2: Manual Copy

1. Copy the `theme/Optimal_Dark.icls` file to your IDE's configuration folder:
   - **Windows**: `%APPDATA%\JetBrains\<product><version>\colors\`
   - **macOS**: `~/Library/Application Support/JetBrains/<product><version>/colors/`
   - **Linux**: `~/.config/JetBrains/<product><version>/colors/`

   > **Examples**: `IntelliJIdea2025.3`, `WebStorm2025.3`, `PyCharm2025.3`

2. Restart the IDE
3. Go to `Settings` → `Editor` → `Color Scheme` and select "Optimal Dark"

> 📖 **Documentation**: [JetBrains - Colors and Fonts](https://www.jetbrains.com/help/idea/configuring-colors-and-fonts.html) | [Configuration Directories](https://www.jetbrains.com/help/idea/directories-used-by-the-ide-to-store-settings-caches-plugins-and-logs.html)

---

## Theme Origin

**JetBrains Optimal Dark** is the result of an **in-depth analysis of three popular themes**:

| Theme                | Description                                                        |
| -------------------- | ------------------------------------------------------------------ |
| **Islands Dark**     | Base theme - very dark background, soft and balanced colors        |
| **Darcula Contrast** | Classic JetBrains theme - traditional orange/blue colors, high contrast |
| **Monokai**          | Iconic theme - vivid and distinctive colors (pink, green, purple)  |

### Concept

The **starting theme** is **Islands Dark**, which offers the best dark background to reduce eye fatigue.

Then, for **each color parameter**, the best color was selected among the three themes:

- **Islands Dark**
- **Darcula Contrast**
- **Monokai**

This approach combines the strengths of each theme: the comfortable background of Islands Dark, the vivid colors of Monokai for critical elements, and the classic tones of Darcula Contrast where they excel.

---

## Design Philosophy

### Fundamental Principle

> **Critical elements must be immediately visible. Secondary elements must be discreet.**

---

## Color Selection Rules

For each color parameter, the color is selected from the three source themes (Islands Dark, Darcula Contrast, Monokai) according to the following criteria:

### Criterion 1: Visibility and Contrast

- The color must offer **sufficient contrast** on the dark background (`#191a1c`)
- Critical elements require **saturated and vivid** colors
- Secondary elements use **desaturated or grayed** colors

### Criterion 2: Element Distinction

- Each element type must have a **distinct** color from others
- Two elements of the same importance but different nature must be distinguishable
- Example: Function declaration (green) ≠ Function call/method (cyan)

### Criterion 3: Universal Semantics

Colors respect universal psychological associations:

| Color            | Meaning                | Usage                          |
| ---------------- | ---------------------- | ------------------------------ |
| **Red**          | Danger, error, urgency | Errors, invalid escapes        |
| **Yellow/Orange** | Attention, warning     | Warnings, parameters           |
| **Green**        | Success, validation, data | Strings, VCS additions, functions |
| **Blue/Cyan**    | Information, navigation | Calls, links, references       |
| **Purple**       | Special, unique        | Numbers, constants             |
| **Gray**         | Neutral, secondary     | Comments, punctuation          |

### Criterion 4: Eye Strain

- **Frequent** elements (operators, punctuation, identifiers) use **low saturation** colors
- **Rare but critical** elements (errors, keywords) can use **highly saturated** colors
- The background remains **very dark** to reduce strain during long sessions

### Criterion 5: Accessibility (Color Blindness)

- Avoid distinguishing elements only by red/green (8% of men are color blind)
- Use additional cues: **italic**, **bold**, **underline**
- Favor **luminosity** contrasts in addition to hue

---

## Typography Style Rules

| Style             | Usage                   | Examples                       |
| ----------------- | ----------------------- | ------------------------------ |
| **Normal**        | Standard elements       | Variables, operators, text     |
| **Italic**        | Special or modified elements | Parameters, static fields, constants |
| **Wavy underline** | Errors and problems     | Syntax errors, warnings        |
| **Strikethrough** | Obsolete elements       | Deprecated code                |

---

## Complete Visual Hierarchy

| Level         | Elements                                      | Visual Treatment            | Frequency   |
| ------------- | --------------------------------------------- | --------------------------- | ----------- |
| **CRITICAL**  | Keywords, errors, functions                   | Vivid saturated colors      | Medium      |
| **IMPORTANT** | Numbers, parameters, escapes, constants       | Distinctive colors          | Low         |
| **DATA**      | Strings, comments, documentation              | Soft desaturated colors     | High        |
| **STRUCTURE** | Operators, punctuation, braces, parentheses   | Neutral gray                | Very high   |
| **METADATA**  | Annotations, decorators, tags                 | Tertiary colors             | Low         |
| **FEEDBACK**  | Errors, warnings, TODO, deprecated            | Strong semantic colors      | Variable    |

---

## Reasoning by Element Type

### Critical Elements

1. **Keywords (if, else, for, class, function...)**
   - Control program flow
   - MUST stand out immediately
   - Allow understanding the logical structure at a glance

2. **Function/method declarations**
   - Fundamental blocks of logic
   - Facilitate code navigation
   - Entry points of the architecture

3. **Function calls**
   - Indicate where code "jumps" to other parts
   - Distinct from declarations to trace flow
   - Allow following execution

4. **Errors**
   - MUST be immediately alarming
   - Color universally associated with danger
   - Impossible to miss

### Important Elements

5. **Numbers**
   - Can be critical "magic numbers"
   - Timeouts, limits, important indices
   - Must be spotted quickly

6. **Function parameters**
   - Define a function's interface
   - Distinguished from local variables
   - Italic reinforces the distinction

7. **Constants**
   - Special immutable values
   - Italic indicates their fixed nature

8. **String escapes**
   - Modify string behavior
   - Can cause subtle bugs or injections
   - Must attract attention

### Data Elements

9. **Strings**
   - Are data, not logic
   - Should not distract from active code
   - Soothing color for text content

10. **Comments**
    - Secondary contextual information
    - Should NEVER dominate visually
    - Allow focus on active code

11. **Documentation**
    - More important than simple comments
    - But remains secondary to code

### Structure Elements

12. **Operators (+, -, \*, /, =, ==...)**
    - Omnipresent in code
    - Coloring them would be too distracting
    - Must remain neutral

13. **Punctuation (commas, semicolons, dots)**
    - Pure syntax with no semantics
    - Should not attract attention

14. **Braces, brackets, parentheses**
    - Delimit structure
    - Neutral at rest, but colored background on hover (matching)

### Metadata Elements

15. **Annotations/Decorators (@Override, @param...)**
    - Important but secondary metadata
    - Distinctive but not loud color

16. **HTML/XML tags**
    - Document structure
    - Distinct from logical code (keywords)

### Feedback Elements

17. **Warnings**
    - Attention required but not critical
    - Less alarming than error red

18. **TODO**
    - Must stand out from normal comments
    - Distinctive without being alarming

19. **Unused code**
    - Dimmed to suggest removal

20. **Deprecated code**
    - Strikethrough clearly indicates obsolescence

---

## Compatibility

This theme is compatible with all JetBrains IDEs:

- IntelliJ IDEA (Community & Ultimate)
- WebStorm
- PyCharm
- PHPStorm
- RubyMine
- GoLand
- CLion
- DataGrip
- Rider
- Android Studio

---

## License

This theme is distributed under the MIT license. You are free to use, modify, and redistribute it.

---

---

# JetBrains Optimal Dark Theme - Configuration Details

## Color Palette

> **Note**: This palette is automatically generated from the choices made during theme generation.

### Main Colors Used

| Color                                                               | Hex       | Usage                              | Origin       |
| ------------------------------------------------------------------- | --------- | ---------------------------------- | ------------ |
| ![#f92672](https://readme-swatches.vercel.app/f92672) Vivid pink    | `#f92672` | Keywords, directives, !important   | Monokai      |
| ![#a6e22e](https://readme-swatches.vercel.app/a6e22e) Vivid green   | `#a6e22e` | Function declarations, attributes  | Monokai      |
| ![#66d9ef](https://readme-swatches.vercel.app/66d9ef) Cyan          | `#66d9ef` | Function calls, methods, CSS props | Monokai      |
| ![#ae81ff](https://readme-swatches.vercel.app/ae81ff) Purple        | `#ae81ff` | Numbers, escapes                   | Monokai      |
| ![#fd971f](https://readme-swatches.vercel.app/fd971f) Orange        | `#fd971f` | Parameters                         | Monokai      |
| ![#6aab73](https://readme-swatches.vercel.app/6aab73) Soft green    | `#6aab73` | Strings                            | Islands Dark |
| ![#7a7e85](https://readme-swatches.vercel.app/7a7e85) Gray          | `#7a7e85` | Comments                           | Islands Dark |
| ![#bcbec4](https://readme-swatches.vercel.app/bcbec4) Light gray    | `#bcbec4` | Text, operators, punctuation       | Islands Dark |
| ![#d5b778](https://readme-swatches.vercel.app/d5b778) Gold          | `#d5b778` | HTML/XML tags                      | Islands Dark |
| ![#c77dbb](https://readme-swatches.vercel.app/c77dbb) Mauve pink    | `#c77dbb` | Constants, fields                  | Islands Dark |
| ![#ff0000](https://readme-swatches.vercel.app/ff0000) Vivid red     | `#ff0000` | Errors                             | Monokai      |
| ![#f2c55c](https://readme-swatches.vercel.app/f2c55c) Yellow        | `#f2c55c` | Warnings                           | Islands Dark |
| ![#191a1c](https://readme-swatches.vercel.app/191a1c) Deep black    | `#191a1c` | Background                         | Islands Dark |

---

## Complete Configuration Tables

> **Note**: The tables below are automatically generated during execution of the generation prompt (`builder/prompt.md`). They reflect the choices made for each parameter.

### Legend

| Symbol | Meaning                                            |
| ------ | -------------------------------------------------- |
| ✏️     | **MODIFIED** - Color changed from Islands Dark     |
| ➕     | **ADDED** - Configuration absent in Islands Dark   |
| ✅     | **KEPT** - Color kept from Islands Dark            |

### `<colors>` Section - Interface Colors

| Element                           | XML Path                                                    | Color         | Name            | Source          | Description                                     | Short Justification                          |
| --------------------------------- | ----------------------------------------------------------- | ------------- | --------------- | --------------- | ----------------------------------------------- | -------------------------------------------- |
| ADDED_LINES_COLOR                 | `colors > ADDED_LINES_COLOR`                                | `#549159`     | Green           | ✅ Islands Dark | Color of added lines in VCS diff                | Green = positive addition, universal convention |
| ANNOTATIONS_COLOR                 | `colors > ANNOTATIONS_COLOR`                                | `#8D9199`     | Gray            | ✅ Islands Dark | VCS annotations color (blame)                   | Discreet gray for secondary info             |
| ANNOTATIONS_LAST_COMMIT_COLOR     | `colors > ANNOTATIONS_LAST_COMMIT_COLOR`                    | `#CED0D6`     | Light gray      | ✅ Islands Dark | Last commit color in annotations                | More visible as recent info                  |
| CARET_COLOR                       | `colors > CARET_COLOR`                                      | `#CED0D6`     | Off-white       | ✅ Islands Dark | Text cursor color                               | Visible on dark background                   |
| CARET_ROW_COLOR                   | `colors > CARET_ROW_COLOR`                                  | `#1F2024`     | Very dark gray  | ✅ Islands Dark | Current line highlight color                    | Subtle to avoid distraction                  |
| CONSOLE_BACKGROUND_KEY            | `colors > CONSOLE_BACKGROUND_KEY`                           | `#191A1C`     | Deep black      | ✅ Islands Dark | Console background                              | Very dark to reduce strain                   |
| DELETED_LINES_COLOR               | `colors > DELETED_LINES_COLOR`                              | `#868A91`     | Gray            | ✅ Islands Dark | Color of deleted lines in diff                  | Gray = deletion, less alarming than red      |
| DIFF_SEPARATORS_BACKGROUND        | `colors > DIFF_SEPARATORS_BACKGROUND`                       | `#2B2D30`     | Dark gray       | ✅ Islands Dark | Diff separators background                      | Discreet but visible                         |
| DOCUMENTATION_COLOR               | `colors > DOCUMENTATION_COLOR`                              | `#27282B`     | Dark gray       | ✅ Islands Dark | Documentation popup background                  | Consistent dark background                   |
| DOC_COMMENT_GUIDE                 | `colors > DOC_COMMENT_GUIDE`                                | `#394D3F`     | Dark green      | ✅ Islands Dark | Visual guide for doc comments                   | Subtle, related to comments                  |
| DOC_COMMENT_LINK                  | `colors > DOC_COMMENT_LINK`                                 | `#3887A1`     | Blue-green      | ✅ Islands Dark | Links in documentation comments                 | Standard link color                          |
| ERROR_HINT                        | `colors > ERROR_HINT`                                       | `#402929`     | Dark red        | ✅ Islands Dark | Error hint background                           | Red = error, but subtle                      |
| FILESTATUS_ADDED                  | `colors > FILESTATUS_ADDED`                                 | `#73BD79`     | Light green     | ✅ Islands Dark | Added files in VCS                              | Green = new/positive                         |
| FILESTATUS_COPIED                 | `colors > FILESTATUS_COPIED`                                | `#73BD79`     | Light green     | ✅ Islands Dark | Copied files in VCS                             | Same logic as ADDED                          |
| FILESTATUS_DELETED                | `colors > FILESTATUS_DELETED`                               | `#6F737A`     | Gray            | ✅ Islands Dark | Deleted files in VCS                            | Gray = inactive/deleted                      |
| FILESTATUS_IGNORED                | `colors > FILESTATUS_IDEA_FILESTATUS_IGNORED`               | `#D69A6B`     | Orange          | ✅ Islands Dark | Files ignored by VCS                            | Orange = attention/ignored                   |
| FILESTATUS_MERGED_CONFLICTS       | `colors > FILESTATUS_IDEA_FILESTATUS_MERGED_WITH_CONFLICTS` | `#DE6A66`     | Light red       | ✅ Islands Dark | Files with merge conflicts                      | Red = conflict to resolve                    |
| FILESTATUS_MERGED                 | `colors > FILESTATUS_MERGED`                                | `#CF84CF`     | Purple          | ✅ Islands Dark | Merged files                                    | Purple = fusion                              |
| FILESTATUS_MODIFIED               | `colors > FILESTATUS_MODIFIED`                              | `#70AEFF`     | Light blue      | ✅ Islands Dark | Modified files                                  | Blue = modification                          |
| FILESTATUS_UNKNOWN                | `colors > FILESTATUS_UNKNOWN`                               | `#E88F89`     | Pale pink       | ✅ Islands Dark | Untracked files                                 | Pink = unrecognized                          |
| FOLDED_TEXT_BORDER_COLOR          | `colors > FOLDED_TEXT_BORDER_COLOR`                         | `#2B2D30`     | Dark gray       | ✅ Islands Dark | Folded text border                              | Discreet                                     |
| HINT_BORDER                       | `colors > HINT_BORDER`                                      | `#393B40`     | Gray            | ✅ Islands Dark | Hint border                                     | Subtle                                       |
| INDENT_GUIDE                      | `colors > INDENT_GUIDE`                                     | `#323438`     | Dark gray       | ✅ Islands Dark | Indentation guides                              | Very discreet                                |
| LINE_NUMBERS_COLOR                | `colors > LINE_NUMBERS_COLOR`                               | `#4B5059`     | Gray            | ✅ Islands Dark | Line numbers                                    | Discreet but readable                        |
| LINE_NUMBER_ON_CARET_ROW_COLOR    | `colors > LINE_NUMBER_ON_CARET_ROW_COLOR`                   | `#A1A3AB`     | Light gray      | ✅ Islands Dark | Current line number                             | More visible                                 |
| LOOKUP_COLOR                      | `colors > LOOKUP_COLOR`                                     | `#27282B`     | Dark gray       | ✅ Islands Dark | Autocomplete background                         | Consistent with interface                    |
| MATCHED_BRACES_INDENT_GUIDE_COLOR | `colors > MATCHED_BRACES_INDENT_GUIDE_COLOR`                | `#4E5157`     | Gray            | ✅ Islands Dark | Matching braces indent guide                    | Subtle                                       |
| METHOD_SEPARATORS_COLOR           | `colors > METHOD_SEPARATORS_COLOR`                          | `#43454A`     | Gray            | ✅ Islands Dark | Method separators                               | Discreet                                     |
| MODIFIED_LINES_COLOR              | `colors > MODIFIED_LINES_COLOR`                             | `#375FAD`     | Blue            | ✅ Islands Dark | Modified lines indicator                        | Blue = modification                          |
| NOTIFICATION_BACKGROUND           | `colors > NOTIFICATION_BACKGROUND`                          | `#25324D`     | Dark blue       | ✅ Islands Dark | Notification background                         | Consistent with theme                        |
| RIGHT_MARGIN_COLOR                | `colors > RIGHT_MARGIN_COLOR`                               | `#323438`     | Dark gray       | ✅ Islands Dark | Right margin line (80 chars)                    | Discreet                                     |
| SELECTED_INDENT_GUIDE             | `colors > SELECTED_INDENT_GUIDE`                            | `#4E5157`     | Gray            | ✅ Islands Dark | Selected indent guide                           | Visible but discreet                         |
| VCS_ANNOTATIONS_COLOR_1-5         | `colors > VCS_ANNOTATIONS_COLOR_*`                          | Blue gradient | -               | ✅ Islands Dark | VCS annotations by age                          | Temporal gradient                            |
| VISUAL_INDENT_GUIDE               | `colors > VISUAL_INDENT_GUIDE`                              | `#2B2D30`     | Dark gray       | ✅ Islands Dark | Visual indent guide                             | Very discreet                                |
| WHITESPACES                       | `colors > WHITESPACES`                                      | `#6F737A`     | Gray            | ✅ Islands Dark | Visible whitespace characters                   | Discreet                                     |

### `<attributes>` Section - Syntax Highlighting

#### MODIFIED Elements (from Monokai)

| Element                          | XML Path                                                             | Color                   | Name           | Source  | Description                                                              | Short Justification                                | Full Justification                                                                                                                                                                                                                                                                                                                                |
| -------------------------------- | -------------------------------------------------------------------- | ----------------------- | -------------- | ------- | ------------------------------------------------------------------------ | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ✏️ DEFAULT_KEYWORD               | `attributes > DEFAULT_KEYWORD > FOREGROUND`                          | `#f92672`               | Monokai Pink   | Monokai | Language keywords (if, else, for, while, class, function, return, etc.)  | Keywords = program flow, MUST stand out            | Keywords control the logical structure of the program. They determine branches, loops, definitions. Monokai's vivid pink makes them immediately identifiable, allowing the developer to understand code flow at a glance. Islands Dark's orange was too close to strings and less impactful.                                                      |
| ✏️ DEFAULT_NUMBER                | `attributes > DEFAULT_NUMBER > FOREGROUND`                           | `#ae81ff`               | Monokai Purple | Monokai | Numeric values (42, 3.14, 0xFF, etc.)                                    | Numbers = potentially critical values              | Numbers can represent "magic numbers": timeouts, loop limits, critical indices, important constants. Monokai's purple clearly distinguishes them from the rest of the code, allowing them to be spotted and questioned. Islands Dark's cyan was confused with links and references.                                                               |
| ✏️ DEFAULT_FUNCTION_DECLARATION  | `attributes > DEFAULT_FUNCTION_DECLARATION > FOREGROUND`             | `#a6e22e`               | Monokai Green  | Monokai | Function names during declaration                                        | Declarations = logic entry points                  | Function declarations are fundamental code blocks. Monokai's vivid green makes them very visible, facilitating navigation and architecture understanding. Islands Dark's blue was less distinctive and confused with calls.                                                                                                                       |
| ✏️ DEFAULT_FUNCTION_CALL         | `attributes > DEFAULT_FUNCTION_CALL > FOREGROUND`                    | `#66d9ef`               | Monokai Cyan   | Monokai | Function calls                                                           | Calls = trace execution flow                       | Function calls indicate where code "jumps" to other parts of the program. Monokai's cyan distinguishes them from normal text while being different from declarations (green), allowing visual execution flow tracing. Islands Dark left them in gray, losing this information.                                                                    |
| ✏️ DEFAULT_INSTANCE_METHOD       | `attributes > DEFAULT_INSTANCE_METHOD > FOREGROUND`                  | `#66d9ef`               | Monokai Cyan   | Monokai | Instance methods                                                         | Match function calls, distinct from declarations   | Instance method calls are invocations, not declarations. Cyan matches function calls to indicate execution flow, while green is reserved for declarations. This distinction helps developers trace where code jumps during execution.                                                                                                              |
| ✏️ DEFAULT_STATIC_METHOD         | `attributes > DEFAULT_STATIC_METHOD > FOREGROUND`                    | `#66d9ef`               | Monokai Cyan   | Monokai | Static methods (+ italic)                                                | Match calls with italic for static distinction     | Static methods are calls, not declarations, so they use cyan like other calls. Italic distinguishes them as static. This maintains the declaration (green) vs call (cyan) distinction.                                                                                                                                                            |
| ✏️ DEFAULT_VALID_STRING_ESCAPE   | `attributes > DEFAULT_VALID_STRING_ESCAPE > FOREGROUND`              | `#ae81ff`               | Monokai Purple | Monokai | Valid escape characters (\n, \t, \\, etc.)                               | Escapes = potentially critical behavior            | Escape characters modify string behavior: newline, tab, or worse, can cause injections. Purple distinguishes them from string content, drawing attention to these special characters.                                                                                                                                                             |
| ✏️ DEFAULT_INVALID_STRING_ESCAPE | `attributes > DEFAULT_INVALID_STRING_ESCAPE > FOREGROUND/BACKGROUND` | `#f8f8f0` on `#f92672`  | White on pink  | Monokai | Invalid escape characters                                                | Error = very visible                               | An invalid escape is an error. Monokai's pink background makes it impossible to miss, much more effective than a simple underline.                                                                                                                                                                                                                |
| ✏️ MATCHED_BRACE_ATTRIBUTES      | `attributes > MATCHED_BRACE_ATTRIBUTES > BACKGROUND`                 | `#3a6da0`               | Monokai Blue   | Monokai | Matching braces/parentheses background                                   | Block navigation                                   | Finding the matching brace is crucial for understanding code structure. Monokai's blue background is much more visible than Islands Dark's dark gray, facilitating navigation in nested blocks.                                                                                                                                                   |
| ✏️ ERRORS_ATTRIBUTES             | `attributes > ERRORS_ATTRIBUTES > EFFECT_COLOR/ERROR_STRIPE_COLOR`   | `#ff6767` / `#ff0000`   | Vivid red      | Monokai | Error underline and stripe                                               | Errors = MUST be alarming                          | Compilation errors are critical. Monokai's pure red (`#ff0000`) is universally associated with danger and impossible to ignore. Islands Dark's pink was less alarming.                                                                                                                                                                            |
| ✏️ HTML_ATTRIBUTE_NAME           | `attributes > HTML_ATTRIBUTE_NAME > FOREGROUND`                      | `#a6e22e`               | Monokai Green  | Monokai | HTML attribute names (class, id, href, etc.)                             | Attributes = important properties                  | HTML attributes define element behavior and style. Monokai's green makes them visible as important properties, rather than leaving them in gray.                                                                                                                                                                                                  |
| ✏️ XML_ATTRIBUTE_NAME            | `attributes > XML_ATTRIBUTE_NAME > FOREGROUND`                       | `#a6e22e`               | Monokai Green  | Monokai | XML attribute names                                                      | Consistency with HTML                              | Same logic as HTML_ATTRIBUTE_NAME.                                                                                                                                                                                                                                                                                                                |
| ✏️ CSS.IMPORTANT                 | `attributes > CSS.IMPORTANT > FOREGROUND`                            | `#f92672`               | Monokai Pink   | Monokai | !important directive in CSS                                              | !important = critical priority                     | The !important directive significantly modifies CSS cascade. Pink makes it as visible as a keyword, because it has a major impact on rendering.                                                                                                                                                                                                   |
| ✏️ CUSTOM_KEYWORD1_ATTRIBUTES    | `attributes > CUSTOM_KEYWORD1_ATTRIBUTES > FOREGROUND`               | `#f92672`               | Monokai Pink   | Monokai | First custom keywords group                                              | Consistency with keywords                          | Same logic as DEFAULT_KEYWORD.                                                                                                                                                                                                                                                                                                                    |
| ✏️ PROPERTIES.KEY                | `attributes > PROPERTIES.KEY > FOREGROUND`                           | `#f92672`               | Monokai Pink   | Monokai | Keys in .properties files                                                | Keys = important identifiers                       | Property keys are like keywords, they define the configuration file structure.                                                                                                                                                                                                                                                                    |
| ✏️ JSP_DIRECTIVE_NAME            | `attributes > JSP_DIRECTIVE_NAME > FOREGROUND`                       | `#f92672`               | Monokai Pink   | Monokai | JSP directive names                                                      | Directives = critical instructions                 | JSP directives control page behavior, like keywords.                                                                                                                                                                                                                                                                                              |
| ✏️ JS.INSTANCE_MEMBER_FUNCTION   | `attributes > JS.INSTANCE_MEMBER_FUNCTION > FOREGROUND`              | `#66d9ef`               | Monokai Cyan   | Monokai | JavaScript instance methods                                              | Consistency with function calls                    | Same logic as DEFAULT_INSTANCE_METHOD. Method calls use cyan to trace execution flow, distinct from declarations (green).                                                                                                                                                                                                                         |

#### ADDED Elements (absent in Islands Dark)

| Element              | XML Path                                                  | Color                | Name           | Source  | Description                                          | Short Justification                    | Full Justification                                                                                                                                                                                                         |
| -------------------- | --------------------------------------------------------- | -------------------- | -------------- | ------- | ---------------------------------------------------- | -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ➕ DEFAULT_PARAMETER | `attributes > DEFAULT_PARAMETER > FOREGROUND + FONT_TYPE` | `#fd971f` + italic   | Monokai Orange | Monokai | Function parameters                                  | Parameters = understand signatures     | Parameters define a function's interface. Monokai's italic orange distinguishes them from local variables, helping immediately understand which values are passed to the function. Islands Dark didn't distinguish them.    |
| ➕ JS.PARAMETER      | `attributes > JS.PARAMETER > FOREGROUND + FONT_TYPE`      | `#fd971f` + italic   | Monokai Orange | Monokai | JavaScript function parameters                       | Consistency with DEFAULT_PARAMETER     | Same logic, JavaScript-specific.                                                                                                                                                                                           |
| ➕ CSS.PROPERTY_NAME | `attributes > CSS.PROPERTY_NAME > FOREGROUND + FONT_TYPE` | `#66d9ef` + italic   | Monokai Cyan   | Monokai | CSS property names (color, margin, display, etc.)    | Properties = style structure           | CSS property names are like function calls: they define what will be modified. Italic cyan distinguishes them from values.                                                                                                  |
| ➕ CSS.TAG_NAME      | `attributes > CSS.TAG_NAME > FOREGROUND`                  | `#f92672`            | Monokai Pink   | Monokai | CSS tag selectors (div, span, p, etc.)               | Tag selectors = important targets      | Tag selectors target entire HTML elements. Pink makes them as important as keywords.                                                                                                                                        |

#### KEPT Elements from Islands Dark

| Element                        | XML Path                                                     | Color                  | Name                    | Description                                     | Short Justification                 | Full Justification                                                                                                                                                                               |
| ------------------------------ | ------------------------------------------------------------ | ---------------------- | ----------------------- | ----------------------------------------------- | ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ✅ DEFAULT_STRING              | `attributes > DEFAULT_STRING > FOREGROUND`                   | `#6aab73`              | Soft green              | Character strings                               | Strings = data, not logic           | Strings are content, not programming logic. Islands Dark's soft green is soothing and doesn't distract from active code. Monokai's yellow was too close to warnings.                             |
| ✅ DEFAULT_BLOCK_COMMENT       | `attributes > DEFAULT_BLOCK_COMMENT > FOREGROUND`            | `#7a7e85`              | Gray                    | Multi-line comments /\* \*/                     | Comments = secondary context        | Comments are important but should NEVER visually dominate the code. Islands Dark's gray makes them readable without distracting.                                                                  |
| ✅ DEFAULT_LINE_COMMENT        | `attributes > DEFAULT_LINE_COMMENT > FOREGROUND`             | `#7a7e85`              | Gray                    | Line comments //                                | Consistency with blocks             | Same logic as DEFAULT_BLOCK_COMMENT.                                                                                                                                                             |
| ✅ DEFAULT_DOC_COMMENT         | `attributes > DEFAULT_DOC_COMMENT > FOREGROUND`              | `#5f826b`              | Grayed green            | Documentation comments /\*\* \*/                | Doc = useful but secondary          | Documentation is important but remains a comment. Islands Dark's grayed green distinguishes it from normal comments while staying discreet.                                                       |
| ✅ DEFAULT_IDENTIFIER          | `attributes > DEFAULT_IDENTIFIER > FOREGROUND`               | `#bcbec4`              | Light gray              | Variables and generic identifiers               | Neutral base for text               | Identifiers are omnipresent. Islands Dark's light gray forms a neutral base that lets colored elements stand out.                                                                                 |
| ✅ DEFAULT_OPERATION_SIGN      | `attributes > DEFAULT_OPERATION_SIGN > FOREGROUND`           | `#bcbec4`              | Light gray              | Operators (+, -, \*, /, =, ==, etc.)            | Operators = don't distract          | Operators are everywhere. Coloring them like keywords (Monokai pink) would be too distracting and reduce the visual impact of real keywords. Islands Dark's gray is judicious.                    |
| ✅ DEFAULT_BRACES              | `attributes > DEFAULT_BRACES > FOREGROUND`                   | `#bcbec4`              | Light gray              | Braces { }                                      | Structure = neutral                 | Braces delimit but have no semantics of their own. Gray keeps them neutral.                                                                                                                       |
| ✅ DEFAULT_BRACKETS            | `attributes > DEFAULT_BRACKETS > FOREGROUND`                 | `#bcbec4`              | Light gray              | Brackets [ ]                                    | Consistency with braces             | Same logic as DEFAULT_BRACES.                                                                                                                                                                    |
| ✅ DEFAULT_PARENTHS            | `attributes > DEFAULT_PARENTHS > FOREGROUND`                 | `#bcbec4`              | Light gray              | Parentheses ( )                                 | Consistency with braces             | Same logic as DEFAULT_BRACES.                                                                                                                                                                    |
| ✅ DEFAULT_COMMA               | `attributes > DEFAULT_COMMA > FOREGROUND`                    | `#bcbec4`              | Light gray              | Commas                                          | Punctuation = neutral               | Commas are pure punctuation.                                                                                                                                                                     |
| ✅ DEFAULT_SEMICOLON           | `attributes > DEFAULT_SEMICOLON > FOREGROUND`                | `#bcbec4`              | Light gray              | Semicolons                                      | Punctuation = neutral               | Same logic as DEFAULT_COMMA.                                                                                                                                                                     |
| ✅ DEFAULT_DOT                 | `attributes > DEFAULT_DOT > FOREGROUND`                      | `#bcbec4`              | Light gray              | Dots (accessor)                                 | Punctuation = neutral               | Same logic as DEFAULT_COMMA.                                                                                                                                                                     |
| ✅ DEFAULT_CONSTANT            | `attributes > DEFAULT_CONSTANT > FOREGROUND + FONT_TYPE`     | `#c77dbb` + italic     | Mauve pink              | Constants                                       | Constants = immutable values        | Constants are special values that don't change. Islands Dark's mauve pink with italic indicates their immutable nature.                                                                           |
| ✅ DEFAULT_INSTANCE_FIELD      | `attributes > DEFAULT_INSTANCE_FIELD > FOREGROUND`           | `#c77dbb`              | Mauve pink              | Instance fields                                 | Consistency with constants          | Fields are like constants at the object level.                                                                                                                                                   |
| ✅ DEFAULT_STATIC_FIELD        | `attributes > DEFAULT_STATIC_FIELD > FOREGROUND + FONT_TYPE` | `#c77dbb` + italic     | Mauve pink              | Static fields                                   | Static = italic                     | Italic distinguishes the static nature.                                                                                                                                                          |
| ✅ DEFAULT_METADATA            | `attributes > DEFAULT_METADATA > FOREGROUND`                 | `#b3ae60`              | Olive yellow            | Annotations/Decorators (@Override, @param, etc.)| Metadata = supplementary info       | Annotations are metadata, important but secondary to code.                                                                                                                                       |
| ✅ HTML_TAG                    | `attributes > HTML_TAG > FOREGROUND`                         | `#d5b778`              | Gold                    | HTML tags                                       | Tags = distinct structure           | Islands Dark's gold distinguishes HTML tags from logical code (pink). Monokai used the same pink as keywords, which is confusing.                                                                 |
| ✅ HTML_TAG_NAME               | `attributes > HTML_TAG_NAME > FOREGROUND`                    | `#d5b778`              | Gold                    | HTML tag names                                  | Consistency with HTML_TAG           | Same logic.                                                                                                                                                                                      |
| ✅ XML_TAG                     | `attributes > XML_TAG > FOREGROUND`                          | `#d5b778`              | Gold                    | XML tags                                        | Consistency with HTML               | Same logic as HTML_TAG.                                                                                                                                                                          |
| ✅ XML_TAG_NAME                | `attributes > XML_TAG_NAME > FOREGROUND`                     | `#d5b778`              | Gold                    | XML tag names                                   | Consistency with XML_TAG            | Same logic.                                                                                                                                                                                      |
| ✅ TODO_DEFAULT_ATTRIBUTES     | `attributes > TODO_DEFAULT_ATTRIBUTES > FOREGROUND`          | `#8bb33d`              | Lime green              | TODO comments                                   | TODO = attention required           | TODOs must stand out from normal comments. Islands Dark's lime green is distinctive without being alarming.                                                                                       |
| ✅ WARNING_ATTRIBUTES          | `attributes > WARNING_ATTRIBUTES > EFFECT_COLOR`             | `#f2c55c`              | Yellow                  | Warning underline                               | Warning = attention, not error      | Yellow is universally associated with warning. It attracts attention without being as alarming as error red.                                                                                      |
| ✅ NOT_USED_ELEMENT_ATTRIBUTES | `attributes > NOT_USED_ELEMENT_ATTRIBUTES > FOREGROUND`      | `#6f737a`              | Dark gray               | Unused elements                                 | Unused = dimmed                     | Dark gray indicates the element is present but not used, suggesting removal or use.                                                                                                               |
| ✅ DEPRECATED_ATTRIBUTES       | `attributes > DEPRECATED_ATTRIBUTES > EFFECT_COLOR`          | `#bcbec4`              | Light gray + strikethrough | Deprecated elements                          | Deprecated = to be replaced         | Strikethrough clearly indicates the element should no longer be used.                                                                                                                             |
| ✅ TEXT (Background)           | `attributes > TEXT > BACKGROUND`                             | `#191a1c`              | Deep black              | Editor background                               | Very dark background = less strain  | Islands Dark's very dark background considerably reduces eye fatigue during long coding sessions. Darker than Darcula and Monokai.                                                                |
| ✅ TEXT (Foreground)           | `attributes > TEXT > FOREGROUND`                             | `#bcbec4`              | Light gray              | Default text                                    | Optimal contrast                    | Light gray offers good contrast without being pure white, which would be harsh on the eyes.                                                                                                       |
