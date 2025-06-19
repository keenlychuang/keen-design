# Callouts

Callouts draw attention to important information while maintaining the clean, minimal aesthetic of Keen Design.

## Base Callout Structure

All callouts share common styling with color variations:

```css
.callout {
  padding: 16px 20px;
  margin: 24px 0;
  border-left: 4px solid;
  border-radius: 0 4px 4px 0;
  font-family: "Times New Roman", serif;
  font-size: 0.9em;
  line-height: 1.6;
}

.callout-icon {
  display: inline-block;
  margin-right: 8px;
  font-size: 1.1em;
}
```

## Callout Types

### Information Callout
For helpful tips, additional context, or general information:

```css
.callout-info {
  background-color: #EFF6FF; /* Blue 50 */
  border-left-color: var(--accent);
  color: var(--text-primary);
}
```

**Example:**
```html
<div class="callout callout-info">
  <span class="callout-icon">ℹ️</span>
  This is an informational callout with helpful context about the topic.
</div>
```

**Alternative icon:** ★ (star for Keen Design personality)

### Warning Callout
For cautions, important notes, or things to watch out for:

```css
.callout-warning {
  background-color: #FFFBEB; /* Yellow 50 */
  border-left-color: var(--star-gold);
  color: var(--text-primary);
}
```

**Example:**
```html
<div class="callout callout-warning">
  <span class="callout-icon">⚠️</span>
  Be careful with this approach - it may have unintended consequences.
</div>
```

### Success Callout
For positive outcomes, completed tasks, or good practices:

```css
.callout-success {
  background-color: #ECFDF5; /* Green 50 */
  border-left-color: var(--success);
  color: var(--text-primary);
}
```

**Example:**
```html
<div class="callout callout-success">
  <span class="callout-icon">✓</span>
  Great! This is the recommended way to implement this feature.
</div>
```

### Quote Callout
For quotations, testimonials, or highlighted text:

```css
.callout-quote {
  background-color: var(--gray-50);
  border-left-color: var(--gray-300);
  color: var(--text-primary);
  font-style: italic;
}

.callout-quote p {
  margin: 0;
}
```

**Example:**
```html
<div class="callout callout-quote">
  <span class="callout-icon">"</span>
  Sometimes the most interesting designs are the ones that know when to hold back.
</div>
```

## Callout Variations

### Subtle Callout
Less prominent styling for secondary information:

```css
.callout-subtle {
  background: none;
  border-left: 2px solid var(--gray-300);
  padding: 12px 16px;
  color: var(--gray-700);
  font-size: 0.875em;
}
```

### Prominent Callout
More emphasis for critical information:

```css
.callout-prominent {
  border: 1px solid;
  border-left: 4px solid;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

.callout-prominent.callout-info {
  border-color: var(--accent);
  border-left-color: var(--accent);
}
```

### Inline Callout
For brief notes within text flow:

```css
.callout-inline {
  display: inline-block;
  padding: 4px 8px;
  margin: 0 4px;
  background-color: var(--gray-100);
  border-left: 3px solid var(--gray-300);
  font-size: 0.85em;
  vertical-align: baseline;
}
```

## Content Guidelines

### Writing Style
- **Be concise:** Callouts should be scannable
- **Use active voice:** Direct and clear communication
- **Start with action words:** "Note," "Remember," "Consider"
- **Avoid redundancy:** Don't repeat information from main text

### Length Recommendations
- **Optimal:** 1-3 sentences
- **Maximum:** One short paragraph
- **Inline callouts:** Single phrase or sentence

### Icon Usage
- **Information:** ℹ️ or ★ (star for brand consistency)
- **Warning:** ⚠️ or ⚡
- **Success:** ✓ or ✅
- **Quote:** " or ❝
- **Tip:** 💡 or ★
- **Note:** 📝 or •

## Responsive Behavior

### Mobile Considerations
```css
@media (max-width: 768px) {
  .callout {
    margin: 16px -16px; /* Extend to screen edges */
    border-radius: 0;
    border-left-width: 3px;
  }
  
  .callout-icon {
    font-size: 1em;
  }
}
```

## Accessibility

### Screen Reader Support
```html
<div class="callout callout-info" role="note" aria-label="Information">
  <span class="callout-icon" aria-hidden="true">ℹ️</span>
  <span class="sr-only">Information: </span>
  This is important information for all users.
</div>
```

### Color Contrast
All callout combinations meet WCAG AA standards:
- Text on light backgrounds: 4.5:1 minimum contrast
- Border colors provide sufficient visual distinction
- Icons supplement color coding (not dependent on color alone)

## Usage Guidelines

### When to Use Callouts
- **Information:** Additional context, explanations, related links
- **Warning:** Potential issues, deprecated features, breaking changes
- **Success:** Confirmations, best practices, positive outcomes
- **Quote:** Testimonials, external references, highlighted insights

### Best Practices
- Use sparingly - too many callouts reduce their impact
- Place callouts close to relevant content
- Maintain consistent icon usage throughout your site
- Test readability on various devices and screen sizes

### Avoid
- Overusing callouts (no more than 2-3 per page section)
- Long paragraphs in callouts
- Nesting callouts within each other
- Using callouts for primary content

---

*A well-placed callout can guide readers to exactly what they need to know.*