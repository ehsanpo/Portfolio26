# Design System Documentation

Portfolio26 Design System - A modern, accessible, and multilingual design foundation.

## Overview

The Portfolio26 design system provides a comprehensive foundation for building consistent, accessible, and beautiful user interfaces across all components and pages.

### Key Features

- **CSS Variables**: Semantic token system with light/dark mode support
- **RTL Support**: Full right-to-left language support for Persian (Farsi)
- **Accessibility First**: WCAG 2.1 AA compliance built-in
- **Modern CSS**: Uses logical properties and modern CSS features
- **Performance Optimized**: Minimal CSS with smart defaults

## Architecture

```
design system/
├── base.css      # Foundation styles and imports
├── tokens.css    # Design tokens (colors, typography, spacing)
├── themes.css    # Light/dark theme definitions
├── rtl.css       # RTL language support
└── README.md     # This documentation
```

## Design Tokens

### Colors

#### Primary Brand Colors
- `--color-primary-*`: Blue color scale (50-950)
- Primary brand color: `--color-primary-500` (#0ea5e9)

#### Neutral Colors
- `--color-neutral-*`: Gray scale (0-950)
- White: `--color-neutral-0`
- Black: `--color-neutral-950`

#### Semantic Colors
- Success: `--color-success-*` (Green)
- Warning: `--color-warning-*` (Amber)
- Error: `--color-error-*` (Red)
- Info: `--color-info-*` (Blue)

### Typography

#### Font Families
- **Sans Serif**: `--font-family-sans` (Inter + system fonts)
- **Serif**: `--font-family-serif` (Playfair Display + system fonts)
- **Monospace**: `--font-family-mono` (JetBrains Mono + system fonts)

#### Font Sizes (Fluid Typography)
- `--font-size-xs` to `--font-size-6xl`
- Responsive scaling using `clamp()`
- Base size: `--font-size-base` (1rem - 1.125rem)

#### Font Weights
- `--font-weight-thin` (100) to `--font-weight-black` (900)

### Spacing

#### Spacing Scale
- Based on 0.25rem (4px) increments
- `--spacing-1` (0.25rem) to `--spacing-96` (24rem)
- Consistent mathematical progression

#### Container Sizes
- `--container-xs` (20rem) to `--container-7xl` (80rem)
- Responsive container system

### Border Radius
- `--border-radius-none` to `--border-radius-full`
- Consistent rounding scale

### Shadows
- `--shadow-xs` to `--shadow-2xl`
- Subtle, modern shadow system

## Semantic Tokens

### Theme System

The design system uses semantic tokens that automatically adapt to light/dark themes:

#### Surface Colors
- `--surface-primary`: Main background
- `--surface-secondary`: Secondary background
- `--surface-tertiary`: Tertiary background
- `--surface-elevated`: Elevated surfaces (cards, modals)
- `--surface-overlay`: Overlay backgrounds

#### Text Colors
- `--text-primary`: Primary text
- `--text-secondary`: Secondary text
- `--text-tertiary`: Tertiary text
- `--text-brand`: Brand-colored text
- `--text-success/warning/error/info`: Semantic text colors

#### Border Colors
- `--border-primary`: Primary borders
- `--border-secondary`: Secondary borders
- `--border-brand`: Brand-colored borders

#### Interactive Colors
- `--interactive-primary`: Primary interactive elements
- `--interactive-secondary`: Secondary interactive elements
- `--interactive-ghost`: Transparent interactive elements

### Theme Usage

#### Automatic Theme Detection
```css
/* Automatically detects user preference */
@media (prefers-color-scheme: dark) {
  /* Dark theme styles */
}
```

#### Manual Theme Control
```html
<!-- Force dark theme -->
<html data-theme="dark">

<!-- Force light theme -->
<html data-theme="light">
```

## RTL Support

### Language Support
- Full RTL support for Persian (Farsi) and Arabic
- Logical CSS properties for directional independence
- Icon mirroring for directional elements

### Usage

#### HTML Setup
```html
<!-- Persian/RTL -->
<html lang="fa" dir="rtl">

<!-- English/LTR -->
<html lang="en" dir="ltr">

<!-- Swedish/LTR -->
<html lang="sv" dir="ltr">
```

#### CSS Classes
```css
/* Text alignment */
.text-start  /* Start of text direction */
.text-end    /* End of text direction */

/* Spacing */
.padding-inline-4    /* Horizontal padding */
.margin-inline-auto  /* Center alignment */
```

### RTL-Specific Features

#### Font Loading
- Persian: Vazirmatn font family
- Improved line height for Arabic script
- Proper number formatting

#### Component Adjustments
- Navigation items
- Button icons
- Form layouts
- Dropdown positioning

## Accessibility

### Built-in Features

#### Focus Management
- Consistent focus rings: `--focus-ring`
- Proper focus offset: `--focus-ring-offset`
- Keyboard navigation support

#### Color Contrast
- WCAG 2.1 AA compliant color combinations
- High contrast mode support
- Semantic color meanings

#### Motion Preferences
```css
@media (prefers-reduced-motion: reduce) {
  /* Reduced motion styles */
}
```

#### Screen Reader Support
- Semantic HTML structure
- Proper heading hierarchy
- Screen reader utility classes

### Utility Classes

```css
.sr-only          /* Screen reader only */
.visually-hidden  /* Visually hidden but accessible */
.hidden           /* Completely hidden */
```

## Usage Examples

### Basic Setup

```css
/* Import the design system */
@import './design system/base.css';
```

### Component Styling

```css
.button {
  background-color: var(--interactive-primary);
  color: var(--text-inverse);
  border: 1px solid var(--border-brand);
  border-radius: var(--border-radius-md);
  padding: var(--spacing-3) var(--spacing-6);
  font-size: var(--font-size-base);
  font-weight: var(--font-weight-medium);
  transition: var(--transition-colors);
}

.button:hover {
  background-color: var(--interactive-primary-hover);
}

.button:focus {
  outline: 2px solid var(--focus-ring);
  outline-offset: 2px;
}
```

### RTL-Aware Layout

```css
.navigation {
  display: flex;
  gap: var(--spacing-4);
}

.nav-item {
  margin-inline-start: var(--spacing-2);
  padding-inline: var(--spacing-3);
}
```

### Responsive Design

```css
.container {
  width: 100%;
  max-width: var(--container-4xl);
  margin-inline: auto;
  padding-inline: var(--spacing-4);
}

@media (min-width: 768px) {
  .container {
    padding-inline: var(--spacing-8);
  }
}
```

## Best Practices

### Do's
✅ Use semantic tokens instead of raw color values
✅ Use logical properties for RTL support
✅ Follow the spacing scale consistently
✅ Test in both light and dark themes
✅ Verify RTL layout functionality
✅ Use proper focus management
✅ Follow accessibility guidelines

### Don'ts
❌ Don't use hardcoded color values
❌ Don't use left/right properties for layout
❌ Don't skip focus states
❌ Don't forget to test RTL layouts
❌ Don't ignore reduced motion preferences
❌ Don't break the visual hierarchy

## Browser Support

- **Modern Browsers**: Full support (Chrome 88+, Firefox 85+, Safari 14+)
- **CSS Custom Properties**: Required
- **Logical Properties**: Required for RTL support
- **CSS Grid/Flexbox**: Required for layout components

## Performance

- **CSS Size**: ~8KB minified + gzipped
- **No JavaScript**: Pure CSS solution
- **Caching**: Long-term cacheable tokens
- **Critical Path**: Only base.css needed initially

## Updates and Versioning

The design system follows semantic versioning:
- **Major**: Breaking changes to token names or structure
- **Minor**: New tokens or features
- **Patch**: Bug fixes and improvements

Last updated: 2025-08-09
