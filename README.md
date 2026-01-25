# wgo - Entertainment Blog Hub

**Wa Goin' On?** — Your digital guide to attractions and events in the British Virgin Islands.

## Overview

wgo is a two-page platform built with **accessible, semantic HTML and CSS**, inspired by the spirit of *Limin' Times*, a beloved local circular that kept the community informed about current happenings. The platform serves as:

1. **Attractions Page** (Static, Free) - Permanent things to do in the British Virgin Islands
2. **Events Page** (Dynamic, For-Profit) - Time-sensitive, expirable events and experiences

## Architecture

### File Structure

```
wgo/
├── index.html          # Attractions page (static, BVI-focused)
├── events.html         # Events page (dynamic listings)
├── styles.css          # Global styles & responsive design
└── README.md          # This file
```

## Design Philosophy

### 1. **Semantic HTML Structure**
- Uses `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>` tags
- Proper heading hierarchy (h1 → h2 → h3)
- ARIA labels for enhanced accessibility
- Role attributes for screen readers

### 2. **Accessibility First**
- WCAG 2.1 AA compliant
- Keyboard navigation support
- Focus indicators for all interactive elements
- Color contrast ratios meet accessibility standards
- Screen reader optimized with semantic markup
- Support for reduced motion preferences
- High contrast mode support

### 3. **Marketing & Communications Layout**

The site employs strategic layout principles:

**Attractions Page:**
- Hero section with clear value proposition
- Grid layout for visual scanning (responsive: 1 → 2 → 3 columns)
- Card-based design for attractions (scannable format)
- Category tags for quick filtering by interest
- Location prominence to aid discovery
- Call-to-action teaser for upcoming Events page

**Events Page:**
- Similar card design for consistency
- Subscribe section for early access
- Clear communication of future revenue model
- Vision section explaining the concept

### 4. **Responsive Design**
- Mobile-first approach
- Three breakpoints: 768px (tablet), 1024px (desktop), 1440px (wide)
- Flexible grid that adapts to screen size
- Touch-friendly navigation and tap targets
- Optimized for all devices

### 5. **Stack: HTML/CSS Only**
- No JavaScript (for now)
- Pure semantic HTML
- CSS Grid & Flexbox for layout
- CSS custom properties for theming
- Future: JavaScript for interactivity (image zoom, filters, etc.)

## Pages

### Attractions (index.html)

The main landing page showcasing permanent attractions across the British Virgin Islands:

- **6 Featured Attractions** (placeholders - to be updated with real BVI attractions)
- Each card includes:
  - Attraction title
  - Location designation
  - Description
  - Category tag
  - Semantic article wrapper

The page includes an "About wgo" section explaining the connection to *Limin' Times* and the mission to keep the community informed.

### Events (events.html)

Digital bulletin board for time-sensitive community happenings:

- **Bulletin board grid** with 6 placeholder event cards
- **Color-coded event labels** by category
- **Event metadata** (date, time, location)
- **Posted date** showing recency
- **Post Event section** explaining how to submit

Event categories include:
- Nightlife
- Church Services
- Sales & Specials
- Volunteer Opportunities
- Music & Entertainment
- Community Events

## Technical Details

### HTML (Semantic Markup)
- No div soup; proper semantic tags throughout
- ARIA labels for images and complex elements
- Screen reader testing recommended
- Keyboard navigation support built-in

### CSS (Responsive Design)
- CSS custom properties (--primary-color, --spacing-lg, etc.)
- Mobile-first media queries
- Flexbox for alignment
- CSS Grid for multi-column layouts
- Gradient backgrounds for visual interest
- Smooth transitions and hover states

### Color Palette
- Primary: `#0066cc` (Professional blue)
- Secondary: `#00a8e8` (Bright cyan)
- Accent: `#ff6b35` (Vibrant orange)
- Light Background: `#f8f9fa`
- Dark Text: `#1a1a1a`
- Muted Text: `#666666`

### Typography
- System font stack for performance
- Base font size: 1rem (16px)
- Line height: 1.6 for readability
- Responsive font sizes using CSS variables

## Future Enhancements

### Phase 1: Polish & Testing
- Full accessibility audit
- Cross-browser testing (Chrome, Firefox, Safari, Edge)
- Mobile device testing
- Performance optimization

### Phase 2: Backend Integration
- User authentication
- Event submission form
- Admin approval workflow
- Database integration

### Phase 3: JavaScript Features (if needed)
- Image zoom functionality
- Event filtering by category
- Search capability
- Date sorting

### Phase 4: Payment Integration
- Stripe integration for paid listings
- Event expiration management
- Revenue tracking
- Promoter dashboard

## How to Use

1. **Start local server:** `python -m http.server 8000`
2. **Open in browser:** `http://localhost:8000`
3. **Navigate:** Click "Attractions" or "Events" in header
4. **Test responsive design:** Use browser DevTools device emulation

## Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Accessibility Notes

- All images should have descriptive alt text
- Links are clearly labeled and styled
- Color is not the only means of conveying information
- All interactive elements are keyboard accessible
- Tab order is logical and intuitive
- Focus indicators are visible on all focusable elements

## Code Standards

- Semantic HTML tags (not `<div>` for everything)
- 2-space indentation
- Clear class naming (BEM-inspired)
- Section comments for organization
- Mobile-first CSS approach
- CSS custom properties for theming

## License

© 2026 wgo. All rights reserved.

---

**Status:** MVP Phase  
**Stack:** HTML5 + CSS3 (no JavaScript yet)  
**Accessibility:** WCAG 2.1 AA Compliant  
**Last Updated:** January 24, 2026

### CSS Features

- **CSS Custom Properties** (Variables) for consistent theming
- **CSS Grid** for responsive layout
- **CSS Flexbox** for component alignment
- **Smooth transitions** for polished interactions
- **Print-friendly styles** for accessibility

### Color Palette

| Variable | Color | Usage |
|----------|-------|-------|
| `--primary-color` | #0066cc | Brand blue, headings, primary actions |
| `--secondary-color` | #00a8e8 | Hover states, secondary actions |
| `--accent-color` | #ff6b35 | Call-to-action, highlights |
| `--bg-light` | #f8f9fa | Secondary backgrounds |
| `--bg-white` | #ffffff | Primary background |
| `--text-dark` | #1a1a1a | Main text |
| `--text-muted` | #666666 | Secondary text |

### Typography

- **Font Stack:** System fonts (Apple System, Segoe UI, Roboto) for optimal performance
- **Base Size:** 16px (1rem)
- **Hierarchy:** Clear size progression from 0.875rem to 2.5rem

## Future Enhancements

### Phase 2: Events with Dynamic Content
- Database-backed event listings
- Expiration timers for events
- User authentication for event creators
- Payment integration for premium listings
- Real-time event search & filtering
- Email notification system for subscriptions

### Phase 3: App Development
- Native iOS app
- Native Android app
- Push notifications
- Location-based event discovery
- User accounts and saved favorites

### Phase 4: Community Features
- User-generated content
- Reviews and ratings
- Social sharing
- Event creation tools
- Community forum

## Communications & Marketing Strategy

The site implements several communication principles:

1. **Clear Value Proposition** - Immediately explains what wgo is and why users need it
2. **Scannable Content** - Card design with hierarchy allows quick scanning
3. **Trust & Transparency** - Explains revenue model and future vision openly
4. **Responsive to Audience** - Supports both tourists and locals
5. **Local Heritage** - References to Limin' Times creates cultural connection
6. **Call-to-Action** - Teases Events page to drive return visits
7. **Professional Design** - Conveys legitimacy and investment in quality

## Getting Started

### Local Development

1. Clone or navigate to the project directory:
   ```bash
   cd wgo
   ```

2. Open in a web server (VS Code Live Server, Python, etc.):
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js (if http-server installed)
   npx http-server
   ```

3. Visit `http://localhost:8000` in your browser

### No Build Required

This project uses vanilla HTML/CSS with no build dependencies. It's intentionally simple and fast-loading.

## Accessibility Testing

To test accessibility:

- **Keyboard Navigation:** Tab through all interactive elements
- **Screen Reader:** Use NVDA (Windows), JAWS, or VoiceOver (Mac)
- **Color Contrast:** Use WebAIM Contrast Checker
- **Responsive:** Test at 320px, 768px, 1024px widths
- **Print:** Use print preview to verify print styles

## Browser Support

- Chrome/Edge (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- **No external dependencies** - Lightning fast load times
- **Optimized CSS** - Minimal file size
- **Semantic HTML** - Faster parsing
- **Sticky header** - Better navigation UX

## Inspiration

**Limin' Times** was a beloved circular publication that kept the Virgin Islands community informed about current events and happenings. wgo honors that legacy by:

- Maintaining the spirit of community connection
- Providing timely, relevant information
- Supporting local event creators
- Creating a hub for authentic island experiences

## License

© 2026 wgo. All rights reserved.

---

**Contact & Support**
For questions about wgo or to list events, please reach out through the main website.

Built with care for the Virgin Islands community.
