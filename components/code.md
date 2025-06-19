-# Code Blocks

Code presentation in Keen Design follows the "let's not get too fancy here" philosophy - clean, readable, and functional.

## Base Code Styling

### Inline Code
For short code snippets within sentences:

```css
code {
  font-family: "Courier New", Courier, monospace;
  font-size: 0.9em;
  background-color: var(--gray-100);
  padding: 2px 6px;
  border-radius: 3px;
  color: var(--text-primary);
  border: 1px solid var(--gray-200);
}
```

**Example:** Use the `console.log()` function to output values.

### Code Blocks
For multi-line code examples:

```css
pre {
  font-family: "Courier New", Courier, monospace;
  background-color: var(--gray-900);
  color: var(--gray-100);
  padding: 20px;
  border-radius: 6px;
  overflow-x: auto;
  line-height: 1.5;
  font-size: 0.875rem;
  margin: 24px 0;
}

pre code {
  background: none;
  padding: 0;
  border: none;
  border-radius: 0;
  color: inherit;
  font-size: inherit;
}
```

## Code Block Variations

### Light Theme Code Block
For sites with light themes or when dark blocks feel too heavy:

```css
.code-light {
  background-color: var(--gray-50);
  color: var(--text-primary);
  border: 1px solid var(--gray-200);
}
```

### Subtle Code Block
Minimal styling that blends with content:

```css
.code-subtle {
  background-color: var(--gray-100);
  color: var(--gray-700);
  border-left: 4px solid var(--gray-300);
  border-radius: 0 4px 4px 0;
}
```

### Terminal/Command Style
For shell commands and terminal output:

```css
.code-terminal {
  background-color: #0D1117; /* Darker than gray-900 */
  color: #58A6FF; /* Light blue */
  font-family: "Courier New", Courier, monospace;
}

.code-terminal::before {
  content: "$ ";
  color: #7C3AED; /* Purple prompt */
  user-select: none;
}
```

## Syntax Highlighting

### Minimal Syntax Colors
Keep it simple with just a few semantic colors:

```css
/* Comments */
.token.comment { color: #6B7280; font-style: italic; }

/* Strings */
.token.string { color: #10B981; }

/* Keywords */
.token.keyword { color: #8B5CF6; font-weight: 600; }

/* Functions */
.token.function { color: #3B82F6; }

/* Numbers */
.token.number { color: #F59E0B; }

/* Operators */
.token.operator { color: #EC4899; }
```

### Language-Specific Styling
Optional enhancements for specific languages:

```css
/* JavaScript */
.language-javascript .token.keyword { color: #F59E0B; }

/* CSS */
.language-css .token.property { color: #3B82F6; }
.language-css .token.selector { color: #10B981; }

/* HTML */
.language-html .token.tag { color: #EC4899; }
.language-html .token.attr-name { color: #8B5CF6; }
```

## Code Block Features

### Copy Button
```css
.code-container {
  position: relative;
}

.copy-button {
  position: absolute;
  top: 12px;
  right: 12px;
  background: var(--gray-700);
  color: var(--gray-100);
  border: none;
  padding: 6px 12px;
  border-radius: 4px;
  font-size: 0.75rem;
  cursor: pointer;
  opacity: 0;
  transition: opacity 0.2s;
}

.code-container:hover .copy-button {
  opacity: 1;
}

.copy-button:hover {
  background: var(--gray-600);
}
```

### Line Numbers
```css
.code-numbered {
  counter-reset: line;
}

.code-numbered .line {
  counter-increment: line;
}

.code-numbered .line::before {
  content: counter(line);
  color: var(--gray-500);
  width: 2em;
  display: inline-block;
  text-align: right;
  margin-right: 16px;
  user-select: none;
}
```

### Language Labels
```css
.code-block::before {
  content: attr(data-language);
  position: absolute;
  top: 8px;
  right: 12px;
  font-size: 0.75rem;
  color: var(--gray-500);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}
```

## Responsive Code Blocks

### Mobile Optimization
```css
@media (max-width: 768px) {
  pre {
    margin: 16px -16px; /* Extend to screen edges */
    border-radius: 0;
    padding: 16px;
    font-size: 0.8rem;
  }
  
  .copy-button {
    position: static;
    display: block;
    margin: 8px 0 0 0;
    opacity: 1;
  }
}
```

### Horizontal Scrolling
```css
pre {
  overflow-x: auto;
  scrollbar-width: thin;
  scrollbar-color: var(--gray-600) var(--gray-800);
}

pre::-webkit-scrollbar {
  height: 8px;
}

pre::-webkit-scrollbar-track {
  background: var(--gray-800);
}

pre::-webkit-scrollbar-thumb {
  background: var(--gray-600);
  border-radius: 4px;
}
```

## Usage Guidelines

### When to Use Each Style
- **Inline code:** Variable names, short functions, file names
- **Standard code blocks:** Complete examples, snippets
- **Light theme blocks:** When dark blocks feel too prominent
- **Terminal style:** Shell commands, CLI examples
- **Subtle blocks:** Configuration files, simple examples

### Code Formatting Best Practices
- **Consistent indentation:** Use 2 or 4 spaces consistently
- **Reasonable line length:** Aim for 80-100 characters
- **Clear comments:** Explain complex logic
- **Remove unnecessary code:** Keep examples focused
- **Proper syntax:** Ensure code is valid and runnable

### Content Guidelines
- **Complete examples:** Provide context for code snippets
- **Explain complex parts:** Use comments or surrounding text
- **Test your code:** Ensure examples actually work
- **Keep it relevant:** Code should serve the content's purpose

## Accessibility

### Screen Reader Support
```html
<pre role="region" aria-label="Code example" tabindex="0">
  <code class="language-javascript">
    function example() {
      return "accessible code";
    }
  </code>
</pre>
```

### Keyboard Navigation
- Code blocks should be focusable (`tabindex="0"`)
- Copy buttons must be keyboard accessible
- Provide skip links for long code sections

### Color Considerations
- Syntax highlighting should not rely solely on color
- Maintain sufficient contrast ratios
- Test with color blindness simulators

---

*Good code presentation gets out of the way and lets the logic speak for itself.*