# Typography

## Font Hierarchy

### Display/Title Font
**Primary:** Georgia, serif  
**Usage:** Main page titles, hero headings, major section titles

```css
font-family: Georgia, serif;
```

### Heading Fonts (H1, H2, H3)
**Primary:** Georgia, serif  
**Sans serif alternative:** System UI stack  
**Fallback:** serif  

```css
/* Primary */
font-family: Georgia, serif;

/* Sans serif alternative */
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;

/* Fallback */
font-family: serif;
```

### Body Text
**Primary:** Times New Roman, serif  
**Sans serif alternative:** System UI stack  
**Fallback:** Times New Roman, serif  
**Usage:** All body content, captions, descriptions

```css
/* Primary */
font-family: "Times New Roman", serif;

/* Sans serif alternative */
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;

/* Fallback */
font-family: "Times New Roman", serif;
```

### Monospace/Code
**Primary:** Courier New, monospace  
**Fallback:** Courier, monospace  
**Character:** "Let's not get too fancy here" - straightforward, functional  
**Usage:** Code blocks, technical references, timestamps

```css
font-family: "Courier New", Courier, monospace;
```

### Labels
**Primary:** System UI stack (sans-serif)  
**Usage:** Form labels, metadata, small UI elements  

```css
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
```

## Typographic Scale

| Element | Size | Line Height | Usage |
|---------|------|-------------|-------|
| Display | 2.5rem (40px) | 1.2 | Hero titles, main headings |
| H1 | 2rem (32px) | 1.3 | Page titles, major sections |
| H2 | 1.5rem (24px) | 1.4 | Section headings |
| H3 | 1.25rem (20px) | 1.4 | Subsection headings |
| Body | 1rem (16px) | 1.6 | Paragraphs, main content |
| Small | 0.875rem (14px) | 1.5 | Captions, secondary text |
| Label | 0.75rem (12px) | 1.4 | Form labels, metadata |

## Typography Rules

### Line Length
- **Optimal:** 50-75 characters per line
- **Maximum:** 65ch for body text
- **Implementation:** Use `max-width: 65ch` on text containers

### Vertical Rhythm
- **Base line-height:** 1.6 for body text
- **Heading line-height:** 1.2-1.4 (smaller for larger text)
- **Margin bottom:** 1.5rem between elements
- **Consistent spacing:** Use multiples of base line-height

### Font Weights
- **Regular (400):** Body text, normal content
- **Semi-bold (600):** Table headers, form labels
- **Bold (700):** Strong emphasis only (use sparingly)

### Text Colors
- **Primary text:** #1A1A1A (near black)
- **Secondary text:** #6B7280 (gray)
- **Accent text:** #2563EB (blue)
- **Muted text:** #9CA3AF (light gray)

## Usage Examples
---
