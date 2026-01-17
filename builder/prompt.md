# JetBrains Optimal Dark Theme Generation Prompt

You are an expert in creating syntax highlighting themes for JetBrains IDEs. Your mission is to generate an optimized `.icls` theme file for readability and reduced eye strain.

---

## Source Files

### Starting File (to copy as base)

```
./builder/ideas/Islands_Dark.icls
```

Read and copy this file entirely as the starting point into:

```
./theme/Optimal_Dark.icls
```

### Files to Compare

For **each parameter** of the theme, you must compare the colors/configurations of these three files and choose the best option:

| Theme                | File                                    | Characteristics                              |
| -------------------- | --------------------------------------- | -------------------------------------------- |
| **Islands Dark**     | `./builder/ideas/Islands_Dark.icls`     | Very dark background, soft and balanced colors |
| **Darcula Contrast** | `./builder/ideas/Darcula_Contrast.icls` | Classic JetBrains colors, high contrast      |
| **Monokai**          | `./builder/ideas/Monokai.icls`          | Vivid and distinctive colors                 |

---

## Working Method

### Step 1: Read the three source files

Read all three `.icls` files entirely to understand their respective color palettes.

### Step 2: Reset and copy the base file

> 🗑️ **CRITICAL**: If the file `./theme/Optimal_Dark.icls` already exists, you MUST delete it or completely overwrite it. You are fully authorized to do so — this is the expected behavior.

**Reset the output file** by copying the entire contents of `Islands_Dark.icls` into `Optimal_Dark.icls`:

```
./builder/ideas/Islands_Dark.icls → ./theme/Optimal_Dark.icls
```

This ensures you always start with a clean, complete base file structure.

> ⚠️ **Important**: Copying Islands_Dark as the base is ONLY for the file structure. This does NOT mean Islands_Dark values are the default choice. For EVERY parameter, you MUST evaluate all three themes equally and choose the best option.

### Step 3: Analyze each parameter

For **each color parameter** (in `<colors>` and `<attributes>`), ask yourself:

> "Among the three themes, which color/configuration best respects the rules below?"

### Step 4: Choose the best option

For each parameter:
1. **Compare the values from ALL THREE themes** (Islands Dark, Darcula Contrast, AND Monokai)
2. Apply the selection rules (see below)
3. **Choose the BEST option among the three** — not necessarily Islands Dark just because it's the base file
4. Modify the output file accordingly

> 💡 **Reminder**: Each parameter must be evaluated independently. The fact that Islands_Dark is the base template should have NO influence on your choice. Always pick the color that best respects the hierarchy and selection rules, whether it comes from Islands_Dark, Darcula_Contrast, or Monokai.

### Step 5: Generate the final file

Save the result in `./theme/Optimal_Dark.icls` with the scheme name "Optimal Dark".

---

## Fundamental Principle

> **Critical elements must be immediately visible. Secondary elements must be discreet.**

This is THE main rule. All other rules derive from it.

---

## Color Selection Rules

Use these rules to decide which color to choose among the three themes.

### Rule 1: Visibility by Importance

| Importance Level | Visual Treatment                |
| ---------------- | ------------------------------- |
| **CRITICAL** (keywords, errors, functions) | **Vivid and saturated** colors |
| **IMPORTANT** (numbers, parameters, escapes) | **Distinctive** colors |
| **DATA** (strings, comments) | **Soft and desaturated** colors |
| **STRUCTURE** (operators, punctuation) | **Neutral (gray)** colors |
| **METADATA** (annotations, tags) | **Tertiary** colors |
| **FEEDBACK** (errors, warnings, TODO) | **Strong semantic** colors |

### Rule 2: Frequency of Appearance

- **Very frequent** elements (operators, commas, identifiers) → **low saturation** colors to avoid fatigue
- **Rare but critical** elements (errors, keywords) → **highly saturated** colors as they must attract attention

### Rule 3: Element Distinction

- Each element type must have a **distinct** color from others
- Two elements of the same importance but different nature must be visually distinguishable
- Example: A function declaration and a function call must have different colors

### Rule 4: Universal Color Semantics

Respect universal psychological associations:

| Color          | Meaning               | Appropriate for              |
| -------------- | --------------------- | ---------------------------- |
| **Red**        | Danger, error, urgency | Errors, invalid escapes     |
| **Yellow/Orange** | Attention, warning  | Warnings, special elements   |
| **Green**      | Success, validation, data | Strings, additions, validations |
| **Blue/Cyan**  | Information, navigation | Links, references, calls    |
| **Purple**     | Special, unique       | Numbers, constants           |
| **Gray**       | Neutral, secondary    | Comments, punctuation        |

### Rule 5: Eye Strain

- Favor a **very dark** background to reduce strain during long sessions
- Frequent element colors must be **comfortable** to look at for long periods
- Avoid overly bright colors for omnipresent elements

### Rule 6: Accessibility (Color Blindness)

- Never distinguish elements **only** by red/green (8% of men are color blind)
- Use additional cues if necessary: **italic**, **bold**, **underline**
- Favor **luminosity** contrasts in addition to hue

---

## Typography Style Rules

In addition to colors, consider font style:

| Style             | When to Use                                |
| ----------------- | ------------------------------------------ |
| **Normal**        | Standard elements (variables, text, operators) |
| **Italic**        | Special or modified elements (parameters, static fields, constants) |
| **Wavy underline** | Errors and problems (syntax, warnings)    |
| **Strikethrough** | Obsolete elements (deprecated code)        |

---

## Visual Hierarchy Reference

Classify elements in this hierarchy to decide their treatment:

| Level         | Elements Concerned                              | Objective                               |
| ------------- | ----------------------------------------------- | --------------------------------------- |
| **CRITICAL**  | Keywords, errors, function declarations         | Must immediately catch the eye          |
| **IMPORTANT** | Numbers, parameters, constants, escapes         | Must be spotted quickly                 |
| **DATA**      | Strings, comments, documentation                | Readable but should not distract        |
| **STRUCTURE** | Operators, punctuation, braces, parentheses     | Invisible during quick scan             |
| **METADATA**  | Annotations, decorators, HTML/XML tags          | Visible but secondary                   |
| **FEEDBACK**  | Warnings, TODO, unused code, deprecated         | Appropriate semantic colors             |

---

## Decision Process for Each Parameter

For each parameter, follow this process:

```
1. Identify the element type (keyword, string, operator, etc.)
2. Determine its level in the hierarchy (CRITICAL, IMPORTANT, DATA, STRUCTURE, METADATA, FEEDBACK)
3. Consider its frequency of appearance (rare, medium, high)
4. Compare the colors of the 3 themes for this parameter
5. Choose the one that:
   - Respects the visual hierarchy
   - Respects color semantics
   - Distinguishes from other elements
   - Minimizes eye strain if the element is frequent
6. Apply appropriate typography style if necessary
```

---

## ⚠️ Important: Files NOT to Read Before Generation

> **DO NOT read the `./README.md` file before generating the theme.**

The `README.md` file contains information from the **previous generation process** (color choices, justifications, palette). Reading this file before generating the theme could **influence and bias** your decisions.

**Correct workflow:**
1. Generate the theme using ONLY the source files in `./builder/ideas/`
2. AFTER generation is complete, read `README.md` to update it with the new choices

This ensures each generation is based purely on the comparison of source themes and the selection rules defined in this prompt.

---

## Generation Instructions

1. **Read the three source files**:
   - `./builder/ideas/Islands_Dark.icls`
   - `./builder/ideas/Darcula_Contrast.icls`
   - `./builder/ideas/Monokai.icls`

2. **Reset the output file**: Delete or overwrite `./theme/Optimal_Dark.icls` if it exists, then copy the entire contents of `./builder/ideas/Islands_Dark.icls` into it as the working base

3. **For each parameter** in `<colors>` and `<attributes>`:
   - Compare the values from the three themes
   - Apply the selection rules
   - Choose the best color/configuration
   - Briefly justify your choice

4. **Name the scheme** "Optimal Dark"

5. **Save the result** in `./theme/Optimal_Dark.icls` (overwrite if it already exists)

6. **Update the `./README.md` file**:
   - Update the configuration tables with the chosen colors
   - Indicate for each parameter the chosen source (Islands Dark, Darcula Contrast, or Monokai)
   - Update the color palette with the final colors
   - Add justifications for each choice

---

## Expected Output Format

For each modification, indicate:

```
[PARAMETER]: parameter_name
[CHOICE]: Islands Dark | Darcula Contrast | Monokai
[VALUE]: #hexcolor (or complete configuration)
[REASON]: Justification based on rules (1-2 sentences)
```

Then generate the complete `.icls` file at the end.

---

## Final Validation

Before finalizing, verify that:

- [ ] Visual hierarchy is respected (critical elements visible, frequent elements discreet)
- [ ] Semantic colors are coherent (red = error, etc.)
- [ ] Same-type elements have consistent colors
- [ ] Frequent elements don't use fatiguing colors
- [ ] Background remains very dark for visual comfort
- [ ] Each choice is justifiable by the established rules
