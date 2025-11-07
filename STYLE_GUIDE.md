# MKAVS Ultra-Minimal Design System

## Design Philosophy
**"Maximum impact with minimum elements"** - Ultra-minimal design prioritizing sophistication, focus, and premium perception through strategic reduction and generous whitespace.

## Brand Colors
- **Primary Black**: `#000000` - Sophisticated background, premium feel
- **Pure White**: `#ffffff` - High contrast text, maximum readability
- **Muted Gray**: `rgba(255, 255, 255, 0.6)` - Secondary text hierarchy
- **Brand Orange**: `#fe5d03` - Minimal accent use (logo glow only)

## Typography Hierarchy

### Ultra-Minimal Scale
- **Main Title**: 40px (mobile: 32px) | Font Weight: 300 (Light) | Color: White
- **Subtitle**: 16px (mobile: 14.4px) | Font Weight: 400 | Color: Muted Gray

### Typography Rules
- **Font Family**: Inter (Light, Normal weights only)
- **Letter Spacing**: Minimal (-0.02em for titles)
- **Line Height**: 1.5 for optimal readability
- **Alignment**: Center-aligned for focus and elegance

## Spacing System
**5-Point Minimal Scale:**
- xs: 8px - Fine adjustments
- sm: 16px - Component spacing
- md: 24px - Section spacing  
- lg: 32px - Layout spacing
- xl: 48px - Major layout gaps

## Layout Principles

### Container
- **Max Width**: 480px - Optimal reading width
- **Alignment**: Center-aligned for focus
- **Padding**: 24px responsive padding

### Logo Treatment
- **Size**: 64px (mobile: 56px, large: 72px)
- **Style**: Rounded corners (12px radius)
- **Effect**: Subtle orange glow for brand connection
- **Spacing**: 24px margin below logo

## Responsive Breakpoints
- **Mobile**: 0-639px (stacked, smaller elements)
- **Desktop**: 640px+ (larger elements, more whitespace)
- **Large**: 1024px+ (maximum scale and spacing)

## Accessibility Standards
- **Contrast**: White on black exceeds WCAG AAA (21:1 ratio)
- **Focus**: Orange outline (2px) with 2px offset
- **Motion**: Respects prefers-reduced-motion
- **Semantic**: Proper heading hierarchy and landmarks

## Component Standards

### Logo Component
```css
.logo {
  width: 64px;
  height: 64px;
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(254, 93, 3, 0.15);
}
```

### Typography Components
```css
.title {
  font-size: 2.5rem;
  font-weight: 300;
  color: #ffffff;
  letter-spacing: -0.02em;
}

.subtitle {
  font-size: 1rem;
  font-weight: 400;
  color: rgba(255, 255, 255, 0.6);
}
```

## Performance Guidelines
- **Critical CSS**: All styles inlined (< 2KB)
- **Fonts**: Only load required weights (300, 400)
- **Images**: Use optimized PNG for logo
- **Load Time**: Target sub-1 second render

## Quality Metrics
- **Page Weight**: < 50KB total
- **Accessibility**: WCAG AAA compliance
- **Performance**: Lighthouse 95+ score
- **Cross-browser**: Chrome, Firefox, Safari, Edge support

## QA Checklist

### Visual Testing
- [ ] Logo displays with correct proportions and glow
- [ ] Typography scales properly across devices  
- [ ] Spacing follows 5-point scale consistency
- [ ] Pure black background with no gradients

### Responsive Testing  
- [ ] Mobile (375px): Compact layout, readable text
- [ ] Tablet (768px): Proportional scaling
- [ ] Desktop (1280px): Optimal whitespace and scale

### Accessibility Testing
- [ ] Keyboard navigation (tab to logo)
- [ ] Screen reader announces "MKAVS Coming soon"
- [ ] High contrast mode compatibility
- [ ] Reduced motion preference respected

### Performance Testing
- [ ] Page loads under 1 second
- [ ] No layout shift during font loading
- [ ] Logo image optimized and cached

## Development Commands
```bash
# Serve locally (Python)
python -m http.server 8000

# Serve locally (Node.js)
npx serve .

# Test accessibility
lighthouse http://localhost:8000 --only-categories=accessibility

# Check performance  
lighthouse http://localhost:8000 --only-categories=performance
```