# ENM Beamer Template

A LaTeX Beamer presentation template for the **Department of Engineering Management (ENM)** at the University of Antwerp.

## About

This is a custom Beamer theme designed for presentations by the Department of Engineering Management (ENM) at the University of Antwerp. The theme provides a professional and consistent look with ENM/University of Antwerp branding, including custom colors, logos, and layouts.

## Original Author

The original Beamer theme was created by **Nico Schlömer**. The logo design is by **Kenneth Sörensen (KS)**, as documented in `art/antor-logo-info.pdf`. This version has been adapted for the ENM department.

## Features

- **Custom ENM branding:**
  - ENM/University of Antwerp logos
  - Custom color scheme matching ENM branding
  - University of Antwerp wave graphics
  - Dark blue background for title slides

- **Professional layout:**
  - Clean and modern design
  - 16:9 aspect ratio support
  - Title and contact slides with logos
  - Customizable navigation symbols

## Installation

1. Clone or download this repository
2. Place the `theme/` folder in your project directory
3. Ensure the `art/` folder is accessible for logo graphics

## How to Use

To use this theme in your presentation:

1. **Keep the folder structure intact:** Ensure both the `theme/` and `art/` folders are in the same directory as your main `.tex` file
2. **Add the path configuration** to your preamble (before `\usetheme`):
   ```latex
   \makeatletter
   \def\input@path{{theme/}}
   \makeatother
   ```
3. **Load the theme:**
   ```latex
   \usetheme{ENM}
   ```
4. **Compile** your document with pdfLaTeX or XeLaTeX

See `ENM-beamer.tex` for a complete working example.

## Usage

### Basic Example

```latex
\documentclass[aspectratio=169]{beamer}
\usepackage{graphicx}

% Configure paths so LaTeX finds theme files in ./theme folder
\makeatletter
\def\input@path{{theme/}}
\makeatother

\setbeamertemplate{navigation symbols}{}

\usetheme{ENM}

\title{Your Presentation Title}
\subtitle{Your Subtitle}
\author{Your Name}
\institute{Department of Engineering Management (ENM), University of Antwerp}
\email{your.email@uantwerpen.be}
\date{\today}

\begin{document}

% Title slide
\begin{frame}
    \titlepage
\end{frame}

% Your content slides here

% Contact slide
\begin{frame}
    \titlewithemail
\end{frame}

\end{document}
```

### Additional Customization

You can customize various aspects:

- Remove navigation symbols: `\setbeamertemplate{navigation symbols}{}`
- Add custom email for contact slide: `\email{your.email@uantwerpen.be}`
- Adjust aspect ratio: `\documentclass[aspectratio=169]{beamer}` (default 16:9)

## File Structure

```
.
├── theme/
│   ├── beamerthemeENM.sty            # Main theme file
│   ├── beamercolorthemeENM.sty       # Color definitions
│   ├── beamerfontthemeENM.sty        # Font settings
│   ├── beamerinnerthemeENM.sty       # Inner theme elements
│   └── beamerouterthemeENM.sty       # Outer theme elements
├── art/                               # Graphics and logos
│   ├── antor-logo.pdf
│   ├── antor-logo-text.pdf
│   ├── antor-logo-white.pdf
│   ├── antorBackgroundLightBlue.pdf
│   ├── antorBackgroundDarkBlue.pdf
│   └── ...
├── pictures/                          # Your presentation images
└── ENM-beamer.tex                     # Example presentation
```

## Example

See `ENM-beamer.tex` for a complete working example with various slide types and formatting options.

## Compiling

Compile your presentation using pdfLaTeX or XeLaTeX:

```bash
pdflatex ENM-beamer.tex
```

Or use latexmk for automatic compilation:

```bash
latexmk -pdf ENM-beamer.tex
```

## License

Original theme: Copyright 2009 by Nico Schlömer

This file may be distributed and/or modified under:
1. The LaTeX Project Public License and/or
2. The GNU Public License

## Credits

- **Original Theme Author:** Nico Schlömer
- **Logo Design:** Kenneth Sörensen (KS) - See `art/antor-logo-info.pdf` for details
- **Modified for:** Department of Engineering Management (ENM), University of Antwerp

## Contact

Department of Engineering Management (ENM)  
University of Antwerp  
https://www.uantwerpen.be/en/faculties/business-economics/research/research-groups/antor/
