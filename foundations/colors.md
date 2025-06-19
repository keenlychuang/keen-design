# Colors

## Primary Palette

### Base Colors
```css
--background:    #FEFEFE  /* Almost white - softer than pure white */
--text-primary:  #1A1A1A  /* Near black - easier on eyes than pure black */
--accent:        #2563EB  /* Royal blue - trustworthy and distinctive */
```

### Supporting Grays
Essential for creating hierarchy and subtle interfaces:

```css
--gray-50:       #F9FAFB  /* Lightest backgrounds */
--gray-100:      #F3F4F6  /* Card backgrounds, code backgrounds */
--gray-200:      #E5E7EB  /* Borders, dividers */
--gray-300:      #D1D5DB  /* Disabled states, subtle borders */
--gray-500:      #6B7280  /* Secondary text, placeholders */
--gray-700:      #374151  /* Dark secondary text */
--gray-900:      #111827  /* Code block backgrounds, high contrast */
```

### Accent Colors
Use sparingly for maximum impact:

```css
--dot-accent:    #6B7280  /* For dot motifs and subtle highlights */
--success:       #10B981  /* Success states, positive feedback */
--warning:       #EF4444  /* Warnings, errors, important alerts */
```

## Semantic Color Usage

### Text Colors
- **Primary text:** `var(--text-primary)` - Main content, headings
- **Secondary text:** `var(--gray-500)` - Captions, metadata, labels
- **Muted text:** `var(--gray-300)` - Placeholder text, disabled states
- **Accent text:** `var(--accent)` - Links, interactive elements

### Background Colors
- **Page background:** `var(--background)` - Main page background
- **Card backgrounds:** `var(--gray-50)` - Content cards, callout boxes
- **Code backgrounds:** `var(--gray-100)` - Inline code, light code blocks
- **Dark code backgrounds:** `var(--gray-900)` - Syntax highlighted code blocks

### Interactive Elements
- **Primary buttons:** `var(--accent)` background, white text
- **Secondary buttons:** `var(--accent)` border and text, transparent background
- **Hover states:** Darker shade of the base color
- **Focus states:** `var(--accent)` outline

### Borders and Dividers
- **Subtle borders:** `var(--gray-200)` - Table borders, card outlines
- **Prominent borders:** `var(--gray-300)` - Form inputs, emphasized sections
- **Accent borders:** `var(--accent)` - Active states, callout left borders

## Color Combinations

### High Contrast (Accessibility)
Text on background: 4.5:1 contrast ratio minimum
- `--text-primary` on `--background`: ✓ Excellent contrast
- `--gray-500` on `--background`: ✓ Good for secondary text
- `--accent` on `--background`: ✓ Sufficient for interactive elements

### Callout Color Schemes
```css
/* All callouts use minimal background with semantic border colors */
/* Information callout */
background: var(--gray-50);  /* Minimal background */
border-left: 4px solid var(--accent);

/* Warning callout */
background: var(--gray-50);  /* Minimal background */
border-left: 4px solid var(--warning);

/* Success callout */
background: var(--gray-50);  /* Minimal background */
border-left: 4px solid var(--success);

/* Quote callout */
background: var(--gray-50);
border-left: 4px solid var(--gray-300);
```

## Usage Guidelines

### Do's
- Use the accent color (`--accent`) for all interactive elements
- Maintain consistent contrast ratios for accessibility
- Use dot accent (`--dot-accent`) only for subtle motifs and separators
- Employ the gray scale for subtle hierarchy and structure
- Stick to primary colors: red, green, blue for semantic meanings
- Use minimal backgrounds with semantic border colors for callouts

### Don'ts
- Don't use more than 3 colors on a single page (excluding grays)
- Avoid pure black (`#000000`) or pure white (`#FFFFFF`)
- Don't use accent colors for large background areas
- Never compromise readability for visual impact
- Avoid oversaturated or "rainbow" color schemes
- Don't use color-specific backgrounds for callouts (rely on border colors instead)

## Color Temperature

The palette maintains a cool, calm feeling with:

- Neutral grays that don't lean warm or cool
- A blue accent that feels trustworthy and professional
- Muted accent colors that complement rather than compete
- Primary color focus: simple red, green, blue for semantic clarity

*A restrained palette ensures your content remains the star of the show.*