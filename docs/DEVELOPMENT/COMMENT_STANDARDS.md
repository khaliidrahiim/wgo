# Code Standards & Comment Guidelines

**How to write professional, clear code comments and maintain consistency across the wgo project.**

---

## HTML Comment Standards

### Section Comments
Mark major sections with clear dividers:

```html
<!-- ============================================
     HEADER & NAVIGATION
     ============================================ -->
<header role="banner">
  ...
</header>
```

**Format:**
- Opening: `<!-- ============================================`
- Section name (UPPERCASE, descriptive)
- Closing: `============================================ -->`
- Use 60 equal signs total

### Inline Comments
Explain non-obvious elements:

```html
<!-- Main attractions grid - responsive layout -->
<div class="articles-grid">
  ...
</div>

<!-- Subscribe form for email notifications -->
<form class="subscribe-form" action="#" method="POST">
  ...
</form>
```

**Rules:**
- Comment above the element, not inline
- Keep comments brief (one line when possible)
- Explain "why," not "what" (the HTML shows what)

### Complex Structures
Explain conditional logic or accessibility features:

```html
<!-- 
  Semantic article tag for each event
  Screen readers will announce: "article"
  Category label provides visual context
-->
<article class="event-card bulletin-card">
  <span class="event-label">Nightlife</span>
  ...
</article>
```

---

## CSS Comment Standards

### Section Comments
```css
/* ============================================
   BULLETIN BOARD STYLES
   ============================================ */
```

**Format:** Same as HTML section comments

### Property Group Comments
```css
/* Card styling - base appearance */
.bulletin-card {
    background: linear-gradient(135deg, #ffffff 0%, #f5f7fa 100%);
    border: 3px solid var(--primary-color);
    border-radius: 8px;
    padding: 0;
    overflow: hidden;
    transition: all 0.3s ease;
}
```

**Rules:**
- Brief comment above related properties
- Explain purpose or rationale
- Group related properties together

### Complex Rules
```css
/* 
  Bulletin card hover effect:
  - Lifts up (transform: translateY)
  - Enhanced shadow for depth
  - Border color changes to orange
  - Smooth 0.3s transition
*/
.bulletin-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 16px rgba(0, 102, 204, 0.2);
    border-color: var(--accent-color);
}
```

### Media Query Comments
```css
/* Tablet view - adjust grid for 2 columns */
@media (min-width: var(--breakpoint-md)) {
    .bulletin-board {
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    }
}
```

---

## Naming Conventions

### HTML Classes
Use clear, descriptive names based on purpose:

**Good:**
```html
<div class="bulletin-card">           <!-- What it is -->
<div class="section-header">          <!-- Where it appears -->
<span class="event-label">            <!-- What it contains -->
```

**Bad:**
```html
<div class="card1">                   <!-- Not descriptive -->
<div class="red-box">                 <!-- Uses color/style -->
<span class="small-text">             <!-- Uses appearance -->
```

### CSS Class Patterns
```css
/* Base element */
.bulletin-card { }

/* Element within container */
.bulletin-card .card-header { }
.bulletin-card .card-content { }
.bulletin-card .card-footer { }

/* State or variation */
.bulletin-card:hover { }
.bulletin-card.featured { }
.event-label { }
```

### CSS Variables
Use clear names for custom properties:

```css
:root {
    /* Colors - descriptive purpose */
    --primary-color: #0066cc;
    --accent-color: #ff6b35;
    
    /* Spacing - semantic names */
    --spacing-sm: 1rem;
    --spacing-md: 1.5rem;
    
    /* Typography - size and weight */
    --font-size-lg: 1.25rem;
    --font-size-xl: 1.75rem;
    
    /* Layout - breakpoints */
    --breakpoint-md: 768px;
    --breakpoint-lg: 1024px;
}
```

---

## Comment Philosophy

### Write "Why" Not "What"

**Bad:** Comments describe what the code does (obvious from reading it)
```css
/* Set the color to blue */
color: #0066cc;

/* Make the border 3 pixels */
border: 3px solid var(--primary-color);
```

**Good:** Comments explain why this approach
```css
/* Primary color for brand consistency */
color: #0066cc;

/* Thick border provides visual emphasis on bulletin board */
border: 3px solid var(--primary-color);
```

### Document Decisions

```css
/* 
  Using auto-fill minmax for responsive grid:
  - Automatically adjusts column count based on space
  - Prevents manual media query updates
  - Fallback for older browsers
*/
grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
```

### Explain Accessibility Features

```html
<!-- 
  ARIA role="banner" indicates header section
  Screen readers announce: "banner"
  Semantically defines page structure
-->
<header role="banner">
```

---

## When to Comment

### Always Comment
- Why a specific approach was chosen
- Non-obvious CSS interactions
- Accessibility features
- Complex layouts or algorithms
- Browser compatibility workarounds

### Don't Comment
- Simple, obvious code
- Self-explanatory element purposes
- Standard HTML tags in normal use
- Every single CSS property

### Good Balance
```html
<!-- 
  Section for user to submit events
  Uses semantic <section> and <form> tags
  Form submission handled by future backend
-->
<section id="post-event" class="post-event-section">
    <h2>Have an Event or Flyer?</h2>
    <p>Got a nightlife event, church service, special sale, volunteer opportunity, or community happening? Share it with the wgo community.</p>
    <p class="post-cta"><strong>Submit Your Event:</strong> Coming soon. Post your flyer and event details to reach locals and visitors throughout the islands.</p>
</section>
```

---

## Indentation Standards

### HTML: 2 Spaces

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>wgo</title>
  </head>
  <body>
    <header>
      <nav>
        <ul>
          <li><a href="#">Link</a></li>
        </ul>
      </nav>
    </header>
  </body>
</html>
```

### CSS: 2 Spaces

```css
.bulletin-board {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: var(--spacing-lg);
}

.bulletin-card {
  background: linear-gradient(135deg, #ffffff 0%, #f5f7fa 100%);
  border: 3px solid var(--primary-color);
  transition: var(--transition);
}
```

---

## File Organization

### HTML File Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Meta tags, title, links -->
</head>
<body>
    <!-- ============================================
         HEADER & NAVIGATION
         ============================================ -->
    <header>
        <!-- Header content -->
    </header>

    <!-- ============================================
         MAIN CONTENT
         ============================================ -->
    <main>
        <!-- Page-specific sections -->
    </main>

    <!-- ============================================
         FOOTER
         ============================================ -->
    <footer>
        <!-- Footer content -->
    </footer>
</body>
</html>
```

### CSS File Structure
```css
/* ============================================
   GLOBAL RESET & BASE STYLES
   ============================================ */

/* ============================================
   CSS VARIABLES & CUSTOM PROPERTIES
   ============================================ */

/* ============================================
   HEADER & NAVIGATION
   ============================================ */

/* ============================================
   BULLETIN BOARD STYLES
   ============================================ */

/* ============================================
   RESPONSIVE DESIGN - MEDIA QUERIES
   ============================================ */

/* ============================================
   PRINT STYLES
   ============================================ */
```

---

## Code Examples

### Good HTML Comment

```html
<!-- 
  Event bulletin card with color-coded category
  Includes: category label, title, metadata, description, posted date
  Used in events.html bulletin board grid
-->
<article class="event-card bulletin-card">
  <div class="card-header">
    <!-- Color-coded category (Nightlife, Church Services, etc.) -->
    <span class="event-label">Nightlife</span>
  </div>
  <div class="card-content">
    <h3>Event Title Here</h3>
    <!-- Metadata: Date, Time, Location -->
    <p class="event-meta">Date • Time • Location</p>
    <p class="event-description">Event description with flyer details.</p>
  </div>
  <div class="card-footer">
    <!-- Shows when event was posted -->
    <span class="event-date">Posted Today</span>
  </div>
</article>
```

### Good CSS Comment

```css
/* ============================================
   BULLETIN BOARD STYLES
   Digital bulletin appearance with card-based layout
   ============================================ */

/* 
  Main bulletin board grid:
  - auto-fill: Responsive column count (no fixed numbers)
  - minmax(280px, 1fr): Each card minimum 280px wide
  - gap: 2rem spacing between cards
  Works on all screen sizes without media queries
*/
.bulletin-board {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: var(--spacing-lg);
  margin-top: var(--spacing-lg);
}

/* 
  Individual bulletin card:
  - Gradient background for visual interest
  - 3px primary color border for emphasis
  - Hover effect lifts card (transform: translateY)
  - Flex layout for consistent content spacing
*/
.bulletin-card {
  background: linear-gradient(135deg, #ffffff 0%, #f5f7fa 100%);
  border: 3px solid var(--primary-color);
  border-radius: 8px;
  padding: 0;
  overflow: hidden;
  transition: var(--transition);
  cursor: pointer;
  display: flex;
  flex-direction: column;
  box-shadow: var(--shadow-md);
}
```

---

## Quick Reference

### Comment Template - HTML
```html
<!-- ============================================
     SECTION NAME
     ============================================ -->
```

### Comment Template - CSS
```css
/* ============================================
   SECTION NAME
   ============================================ */
```

### Comment Template - Complex Rule
```css
/* 
  Element name or purpose
  - Detail 1
  - Detail 2
  - Why this approach
*/
```

---

## Checklist for Code Review

- [ ] All major sections have divider comments
- [ ] Comments explain "why," not "what"
- [ ] HTML uses 2-space indentation
- [ ] CSS uses 2-space indentation
- [ ] Class names are descriptive and semantic
- [ ] CSS variables used for colors, spacing, fonts
- [ ] Accessibility features are documented
- [ ] Media queries are clearly labeled
- [ ] Comments are helpful but not excessive
- [ ] Code follows the style of existing files

---

## Code Quality Principles

1. **Clarity First** - Code should be easy to understand
2. **Semantic HTML** - Use tags that describe their purpose
3. **Consistent Style** - Follow established patterns
4. **Accessibility** - Always consider screen readers and keyboard users
5. **Responsive Design** - Mobile-first, test on multiple sizes
6. **Performance** - Use CSS variables, minimal repetition
7. **Maintainability** - Future developers should understand quickly

---

**Version:** 1.0  
**Last Updated:** January 24, 2026  
**Status:** Ready for team use

---

When in doubt, ask: "Would a new developer understand this code's purpose?"

If the answer is "maybe," add a comment explaining the "why."
