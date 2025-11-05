# ANT/OR Beamer Theme

A modified Beamer presentation theme for the **ANT/OR Research Group** (Department of Engineering Management, University of Antwerp).

## About

This is a modified Beamer theme specifically designed for the ANT/OR research group. The theme provides a professional and consistent look for presentations with the ANT/OR branding, including custom colors, logos, and layouts.

## Original Author

The original Beamer theme was created by **Kenneth Sörensen (KS)**, as documented in `art/antor-logo-info.pdf`. This version has been adapted to make it more easily usable.

## Features

- **Multiple theme options:**
  - `darktitle` - Use dark background for title slides
  - `repeattitleslide` - Repeat title slide at the end
  - `framenumber` - Display frame numbers
  - `compress` - Compressed navigation bar
  - `dark` - Dark theme variant

- **Custom branding elements:**
  - ANT/OR logos and graphics in various styles
  - Custom color scheme
  - University of Antwerp wave graphics
  - Light blue and dark blue background options

- **Aspect ratio support:** 16:9 aspect ratio (configurable)

## Installation

1. Clone or download this repository
2. Place the `theme/` folder in your project directory
3. Ensure the `art/` folder is accessible for logo graphics

## How to Use

To use this theme in your presentation:

1. **Keep the folder structure intact:** Ensure both the `theme/` and `art/` folders are in the same directory as your main `.tex` file
2. **Added the path configuration** to your preamble (before `\usetheme`):
   ```latex
   \makeatletter
   \def\input@path{{theme/}}
   \makeatother
   ```
3. **Load the theme** with your desired options:
   ```latex
   \usetheme[darktitle, repeattitleslide, framenumber, compress]{ANTOR}
   ```
4. **Compile** your document with pdfLaTeX or XeLaTeX

See `antor-beamer.tex` for a complete working example.

## Usage

### Basic Example

```latex
\documentclass[aspectratio=169]{beamer}

% Configure paths so LaTeX finds theme files in ./theme folder
\makeatletter
\def\input@path{{theme/}}
\makeatother

\usetheme[darktitle, repeattitleslide, framenumber, compress]{ANTOR}

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

### Theme Options

Available options when loading the theme:

- `darktitle` - Dark background for title slide
- `repeattitleslide` - Automatically adds title slide at the end
- `framenumber` - Shows frame numbers on slides
- `compress` - Compresses navigation elements
- `dark` - Enables dark theme variant

Example:
```latex
\usetheme[darktitle, framenumber]{ANTOR}
```

## File Structure

```
.
├── theme/
│   ├── beamerthemeANTOR.sty          # Main theme file
│   ├── beamercolorthemeANTOR.sty     # Color definitions
│   ├── beamerfontthemeANTOR.sty      # Font settings
│   ├── beamerinnerthemeANTOR.sty     # Inner theme elements
│   ├── beamerouterthemeANTOR.sty     # Outer theme elements
│   └── beamerthemeANTORPOSTER.sty    # Poster variant
├── art/                               # Graphics and logos
│   ├── antor-logo.pdf
│   ├── antor-logo-text.pdf
│   ├── antor-logo-white.pdf
│   ├── antorBackgroundLightBlue.pdf
│   ├── antorBackgroundDarkBlue.pdf
│   └── ...
└── antor-beamer.tex                  # Example presentation
```


