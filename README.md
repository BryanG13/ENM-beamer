# ENM Beamer Template

A LaTeX Beamer presentation template for the **ENM (Engineering Management) and ANT/OR** at the University of Antwerp.

## About

This is a custom Beamer theme designed for presentations by the ENM (Engineering Management) department and the ANT/OR group at the University of Antwerp. The theme provides a professional and consistent look with ENM/University of Antwerp branding, including custom colors, logos, and layouts.

## Installation

1. Clone or download this repository
2. Place the `theme/` folder in your project directory
3. Ensure the `Logos/` folder is accessible for logo graphics

## How to Use

To use this theme in your presentation:

1. **Keep the folder structure intact:** Ensure both the `theme/` and `Logos/` folders are in the same directory as your main `.tex` file
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

### Theme Options

The theme supports several customization options that can be combined:

#### Color Schemes

- **Dark mode (default):**
  ```latex
  \usetheme[dark]{ENM}
  % or simply
  \usetheme{ENM}
  ```
  Title and end slides use dark blue backgrounds (RGB 15,45,100 and RGB 87,108,150).

- **Light mode:**
  ```latex
  \usetheme[light]{ENM}
  ```
  Title and end slides use green backgrounds (RGB 103,167,49 for title slide and RGB 153,197,99 for end slide).

#### Logo Options

- **ENM logo (default):**
  ```latex
  \usetheme{ENM}
  ```
  Uses the ENM logo (`Logos/enm-en-rgb`) in the header of content slides.

- **ANT/OR logo:**
  ```latex
  \usetheme[antor]{ENM}
  ```
  Uses the University of Antwerp logo instead of the ENM logo in the header. When combined with light mode, uses green Antor logos (`Logos/antor-logo-green` for title page and `Logos/antor-logo-green-light` for slide headers). In dark mode, uses the classic light Antor logo.

- **ANT/OR classic logo:**
  ```latex
  \usetheme[antor,classic]{ENM}
  ```
  Uses the original University of Antwerp logo (`Logos/antor-logo`) regardless of the theme mode.

#### Combining Options

You can combine multiple options together:

```latex
% Light theme with Antwerp logo (uses green logos)
\usetheme[light,antor]{ENM}

% Dark theme with Antwerp logo (uses dark logo)
\usetheme[dark,antor]{ENM}

% Light theme with classic Antwerp logo
\usetheme[light,antor,classic]{ENM}
```

### Footer and Header Customization

You can control the visibility of various elements:

- `\hidefooter` - Hide the entire footer
- `\showfooter` - Show the footer (default)
- `\hidefooterleft` - Hide only the left side information in footer
- `\showfooterleft` - Show left side information (default)
- `\hideframenumber` - Hide slide numbering
- `\showframenumber` - Show slide numbering (default)
- `\hideheadline` - Hide the header logos
- `\showheadline` - Show header logos (default)

These commands can be used globally in the preamble or locally before specific frames.

4. **Compile** your document with pdfLaTeX or XeLaTeX

See `ENM-beamer.tex` for a complete working example.

## File Structure

```
.
├── theme/
│   ├── beamerthemeENM.sty            # Main theme file
│   ├── beamercolorthemeENM.sty       # Color definitions
│   ├── beamerfontthemeENM.sty        # Font settings
│   ├── beamerinnerthemeENM.sty       # Inner theme elements
│   └── beamerouterthemeENM.sty       # Outer theme elements
├── Logos/                             # Theme logos
│   ├── antor-logo.pdf                # University of Antwerp logo (classic)
│   ├── antor-logo-dark.pdf           # University of Antwerp logo (dark)
│   ├── antor-logo-green.pdf          # University of Antwerp logo (green, for light theme)
│   ├── antor-logo-green-light.pdf    # University of Antwerp logo (green light, for light theme headers)
│   ├── antor-logo-light.pdf          # University of Antwerp logo (light, for dark theme)
│   ├── enm-en-rgb.png                # ENM logo (RGB)
│   ├── enm-en-white.png              # ENM logo (white)
│   └── ...                           # Other logo variants
├── pictures/                          # Your presentation images
├── ENM_Beamer.tex                     # Example presentation
└── README.md                          # This file
```

