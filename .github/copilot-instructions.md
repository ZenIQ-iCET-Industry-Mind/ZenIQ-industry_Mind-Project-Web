# AI Agent Instructions for ZENIQ Website

## Project Overview
This is a static website for ZENIQ, a student-led ICT consultancy. The site uses a modern, minimalist design approach with a focus on accessibility and performance.

## Architecture & Structure
- Single-page static website built with HTML and TailwindCSS
- Uses CDN-hosted Tailwind for styles (`cdn.tailwindcss.com`)
- No build process or package manager required
- Images stored in `/image` directory
- Custom CSS variables for brand theming in `:root`

## Key Design Patterns

### CSS Structure
1. Brand Tokens:
```css
:root {
  --clr-primary: #0f172a;    /* Deep/Navy Tech Blue */
  --clr-secondary: #e2e8f0;  /* Metallic Silver */
  --clr-accent: #3b82f6;     /* Electric Blue */
  --clr-glass: rgba(226, 232, 240, 0.05);
  --clr-highlight: #06b6d4;  /* Subtle Cyan */
}
```

2. Glass Panel Effect:
- Use the `.glass-panel` class for frosted glass UI elements
- Always include proper backdrop-filter fallbacks for browser compatibility

### Accessibility Features
- Skip link implementation for keyboard navigation
- ARIA labels on interactive elements
- Focus states with custom accent outlines
- Semantic HTML structure

### Responsive Design
- Mobile-first approach using Tailwind breakpoints
- Custom scrollbar styling for horizontal scrolling elements
- iOS momentum scroll fix with `.scroll-touch` utility

## Working with Images
- Store all images in `/image` directory
- Use descriptive filenames (e.g., `logojpg.jpg` for logo)
- Support for JPG and PNG formats

## Best Practices
1. Maintain CDN compatibility:
   - Avoid Tailwind `@apply` directives
   - Use vanilla CSS for custom components
2. Performance:
   - Keep images optimized
   - Minimize custom CSS where Tailwind utilities suffice
3. Accessibility:
   - Include meta descriptions and Open Graph tags
   - Maintain proper heading hierarchy
   - Ensure sufficient color contrast

## Common Tasks
- Adding new sections: Follow existing pattern with proper ARIA labels
- Styling: Prefer Tailwind utilities, use custom CSS only for complex patterns
- Images: Place in `/image` directory with descriptive names