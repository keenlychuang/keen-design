# Tables

Tables in Keen Design prioritize readability and clean presentation while maintaining the system's minimal aesthetic.

## Basic Table Structure

### Default Table
Clean, bordered table with subtle styling:

```css
table {
  border-collapse: collapse;
  width: 100%;
  font-family: "Times New Roman", serif;
  font-size: 1rem;
  line-height: 1.6;
}

th, td {
  padding: 12px 16px;
  text-align: left;
  border: 1px solid var(--gray-200);
}

th {
  background-color: var(--gray-50);
  font-weight: 600;
  color: var(--text-primary);
}

tr:hover {
  background-color: var(--gray-50);
}
```

### Example Default Table
| Heading 1 | Heading 2 | Heading 3 |
|-----------|-----------|-----------|
| Data cell | Data cell | Data cell |
| Data cell | Data cell | Data cell |
| Data cell | Data cell | Data cell |

## Table Variants

### Minimal Table
Clean design with header underline only:

```css
.table-minimal {
  border: none;
}

.table-minimal th,
.table-minimal td {
  border: none;
  border-bottom: 1px solid var(--gray-200);
  padding: 8px 12px;
}

.table-minimal th {
  background: none;
  border-bottom: 2px solid var(--gray-300);
  font-weight: 600;
}

.table-minimal tr:hover {
  background: none;
}
```

### Striped Table
Alternating row backgrounds for easier scanning:

```css
.table-striped tbody tr:nth-child(even) {
  background-color: var(--gray-50);
}

.table-striped tbody tr:nth-child(odd) {
  background-color: var(--background);
}

.table-striped tr:hover {
  background-color: var(--gray-100) !important;
}
```

### Compact Table
Reduced padding for dense information:

```css
.table-compact th,
.table-compact td {
  padding: 8px 12px;
  font-size: 0.875rem;
}
```

## Table Styling Rules

### Typography
- **Font:** Times New Roman (body font) for consistency
- **Headers:** Font-weight 600, same size as body
- **Alignment:** Left-aligned by default
- **Numbers:** Right-aligned for easier comparison

### Spacing
- **Cell padding:** 12px vertical, 16px horizontal (default)
- **Compact padding:** 8px vertical, 12px horizontal
- **Border width:** 1px for all borders

### Colors
- **Header background:** `var(--gray-50)` (subtle)
- **Border color:** `var(--gray-200)` (gentle separation)
- **Hover state:** `var(--gray-50)` (light highlight)
- **Striped rows:** Alternating `var(--background)` and `var(--gray-50)`

## Responsive Tables

### Mobile-First Approach
For narrow screens, consider stacking or horizontal scrolling:

```css
@media (max-width: 768px) {
  .table-responsive {
    display: block;
    overflow-x: auto;
    white-space: nowrap;
  }
  
  .table-responsive table {
    min-width: 600px;
  }
}
```

### Card-Style (Alternative)
Transform table rows into cards on mobile:

```css
@media (max-width: 768px) {
  .table-cards thead {
    display: none;
  }
  
  .table-cards tbody,
  .table-cards tr,
  .table-cards td {
    display: block;
  }
  
  .table-cards tr {
    border: 1px solid var(--gray-200);
    margin-bottom: 16px;
    padding: 16px;
    border-radius: 4px;
  }
  
  .table-cards td::before {
    content: attr(data-label) ": ";
    font-weight: 600;
    color: var(--gray-700);
  }
}
```

## Special Table Types

### Data Tables
For numerical data or comparisons:

```css
.table-data td:nth-child(n+2) {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

.table-data th:nth-child(n+2) {
  text-align: right;
}
```

### Simple List Tables
For basic key-value pairs:

```css
.table-simple {
  border: none;
}

.table-simple td {
  border: none;
  border-bottom: 1px solid var(--gray-100);
  padding: 8px 0;
}

.table-simple td:first-child {
  font-weight: 600;
  color: var(--gray-700);
  width: 30%;
}
```

## Usage Guidelines

### When to Use Each Variant
- **Default:** General data presentation, documentation
- **Minimal:** Clean layouts, fewer visual elements needed
- **Striped:** Long tables where row tracking is important
- **Compact:** Dense information, dashboards, technical specs

### Best Practices
- Keep headers concise and descriptive
- Align numerical data to the right for easy comparison
- Use consistent data formatting within columns
- Consider responsive behavior from the start
- Limit table width for better readability (max 8-10 columns)

### Accessibility
- Always include `<th>` elements for headers
- Use `scope` attribute for complex tables
- Provide `<caption>` for table context
- Ensure sufficient color contrast (4.5:1 minimum)
- Test with screen readers

---

*Good tables disappear into the background, letting the data tell its story.*