# SMU Beamer Template

A simple LaTeX Beamer presentation template for Southern Methodist University (SMU) with official brand styling, including SMU-styled color themes and fonts.

## Overview

This template provides a professional Beamer design that follows SMU's visual identity guidelines as specified at [smu.edu/brand](https://www.smu.edu/brand). It features authentic SMU branding elements including official logos, colors, and fonts to create presentations that align with the university's brand standards.

## Requirements

- **XeLaTeX compiler** (required - will not work with pdfLaTeX or LuaTeX)
- Reason: The template relies on the `fontspec` package for custom font support

## Key Features

### 1. SMU Branding Elements

**Official Logos:**
- Dallas Hall icon
- SMU formal logos (multiple color variations)
- School/department logos (Lyle, Dedman, Moody, etc.)
- All logos sourced from [official SMU Box repository](https://smu.app.box.com/s/bkdanzfumpcle67rfcqlakx3c9aa0lay)

**Color Palette:**
- Primary colors: **SMU Blue** and **SMU Red**
- Secondary colors: **SMU Yellow**, **SMU Salmon**, **SMU Teal**, and **SMU Black**
- Pre-defined color commands: `\textcolor{SMUBlue}{...}`, `\color{SMURed}`, etc.
- Colored theorem blocks matching SMU brand colors

**Typography:**
- Serif font: **Tiempos Headline** (with free alternative: Source Serif 4)
- Sans serif font: **Arial**
- Monospace font: **JetBrains Mono**
- Serif used for titles/subtitles, sans serif for body text

### 2. Customization Options

**Background Styles (4 combinations):**
- Colored or white background
- Light or dark frame title header
- Toggle via `\usecolorbgtrue`/`\usecolorbgfalse` and `\uselightheadertrue`/`\uselightheaderfalse`

**Title Page Customization:**
- `\titletop{...}` - Add content above title (e.g., conference logos)
- `\extrainfo{...}` - Add content below author/institute (e.g., email, collaborators)

**Logo Placement:**
- Customizable title page logo via `\titlegraphic{...}`
- Corner logo on each slide via `\setbeamertemplate{background}{...}`

### 3. Technical Features

- Syntax highlighting for multiple languages (Python, C/C++, Java, MATLAB, Fortran, LaTeX)
- Default serif math fonts (preserving mathematical notation standards)
- Support for complex layouts with columns, tables, and figures
- Multi-line title and subtitle support

## Getting Started

### Basic Setup

1. **Set main document**: In Overleaf, set `main.tex` as your main document (upper left menu)
2. **Compile with XeLaTeX**: Ensure XeLaTeX is selected as the compiler
3. **Customize metadata**: Edit the following in `template_main.tex`:
   ```latex
   \title[Short Title]{Your Full Title}
   \subtitle{Your Subtitle}
   \author[Short Name]{Your Full Name}
   \institute[Short Inst]{Your Institution/Department}
   \date{\today}
   ```

### Using SMU Colors

```latex
% Text coloring
\textcolor{SMUBlue}{Blue text}
{\color{SMURed}Red text}

% In math mode
$$\frac{x^2}{2} {\color{SMUSalmon} + C}$$
```

### Using Serif Font

```latex
{\serif\textbf{Southern} \textit{Methodist} University}
```

### Creating Blocks

```latex
\begin{block}{Block Title}
    Default block with SMU Blue
\end{block}

\begin{alertblock}{Alert Title}
    Alert block with SMU Red
\end{alertblock}

\begin{exampleblock}{Example Title}
    Example block with SMU Yellow
\end{exampleblock}
```

### Adding Code with Syntax Highlighting

```latex
\begin{lstlisting}[style=python]
def hello_world():
    print("Hello, World!")
\end{lstlisting}
```

## File Structure

- `template_main.tex` - Main presentation file
- `smu_beamer_template.sty` - Template style file
- `template-source/` - Supporting files (logos, fonts, images)
  - `codestyle.tex` - Syntax highlighting definitions
  - `SourceSerif4/` - Free alternative serif font
  - Various SMU logos and brand assets

## Customization Guide

### Switching to Source Serif 4 (Free Alternative)

1. In `smu_beamer_template.sty`, uncomment:
   ```latex
   \newfontfamily\sourceserif[...]{SourceSerif4}
   ```
2. Change:
   ```latex
   \def\serif{\tiempos}
   % to
   \def\serif{\sourceserif}
   ```

### Changing Block Colors

Find and modify these commands in `smu_beamer_template.sty`:
```latex
\setbeamercolor{block title}{...}
\setbeamercolor{block body}{...}
\setbeamercolor{block title alerted}{...}
\setbeamercolor{block body alerted}{...}
\setbeamercolor{block title example}{...}
\setbeamercolor{block body example}{...}
```

### Changing Monospace Font

Modify the `\setmonofont{...}[...]` command in `smu_beamer_template.sty`.

## Best Practices

### Color Usage Hierarchy
Follow SMU's color importance order:
**Blue > Red > Yellow > Salmon ≈ Teal**

- Use **Salmon** for emphasis (with bold)
- Use **Salmon** and **Teal** together to contrast concepts
- Avoid Salmon and Teal in formal contexts

### Figure Backgrounds
Remove white backgrounds from figures when using colored slide backgrounds for a more professional appearance.

### Font Usage
- **Serif**: Titles, subtitles, and special emphasis only
- **Sans serif**: Body text, lists, tables, captions
- **Math**: Keep default LaTeX serif for formulas

## Examples Included

The template includes several example frames demonstrating:
- Multi-column layouts
- Mathematical content (Calkin-Wilf Tree)
- Complex tables (sorting algorithms comparison)
- Figure handling and background removal
- Code listings with syntax highlighting
- Custom title and thank you pages

## License

This template is intended for **non-commercial use only**.

## Author

Andrew Ho (Qing He)  
Southern Methodist University, Department of Mathematics  
Email: andrewho@smu.edu

## Resources

- SMU Brand Guidelines: [smu.edu/brand](https://www.smu.edu/brand)
- SMU Logos: [smu.edu/brand/logos](https://www.smu.edu/brand/logos)
- SMU Colors: [smu.edu/brand/color-palette](https://www.smu.edu/brand/color-palette)
- SMU Fonts: [smu.edu/brand/fonts](https://www.smu.edu/brand/fonts)
- Official Logo Repository: [SMU Box](https://smu.app.box.com/s/bkdanzfumpcle67rfcqlakx3c9aa0lay)

## Support

For questions or issues with the template, please contact the author at andrewho@smu.edu.

---

**Note**: This template requires XeLaTeX compilation and uses the Tiempos font (test version). A free alternative (Source Serif 4) is included for users who prefer to avoid licensing concerns.
