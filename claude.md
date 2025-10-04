Project Guidelines
Tech Stack

HTML: Static HTML files only
CSS: Tailwind CSS via CDN + minimal custom styles.css
No JavaScript: Unless explicitly requested
No build tools: Pure static files only

Core Principles
1. Pixel-Perfect Implementation

Build EXACTLY what is shown in Figma designs
Never add features, elements, or styling not explicitly shown
Match spacing, typography, and colors precisely
If something seems missing, ASK before adding

2. Layout Strategy

Always use Flexbox for layouts (never absolute positioning)
Prefer flex containers with proper alignment over margins for spacing
Use CSS Grid only when explicitly beneficial for the design
Maintain responsive behavior through Flexbox's natural flow

3. Development Workflow

Receive Figma design
Implement initial HTML structure with Tailwind classes
Use Chrome DevTools MCP to inspect and verify
Iterate until pixel-perfect match
Test at multiple viewport sizes

Implementation Standards
HTML Structure
html<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[Page Title]</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Custom styles only when Tailwind insufficient -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Content here -->
</body>
</html>
Flexbox Best Practices

Container setup: flex flex-col or flex flex-row
Alignment: Use justify-* and items-* for positioning
Spacing: Prefer gap-* over margins between flex items
Wrapping: Use flex-wrap when appropriate
Growth: Leverage flex-grow, flex-shrink, flex-1 for fluid layouts

Spacing & Sizing

Use Tailwind's spacing scale consistently (p-4, m-8, gap-6)
Match Figma's exact pixel values using arbitrary values when needed: w-[237px]
For custom spacing not in Tailwind's scale, use styles.css sparingly

Typography

Match font families exactly (add Google Fonts if needed)
Use Tailwind's typography scale when it matches
Create custom classes in styles.css for specific text styles that repeat

Colors

Use Tailwind's default palette when possible
Define custom colors via Tailwind config or inline arbitrary values
Maintain consistency across all uses of the same color

Chrome DevTools MCP Usage

After initial implementation, use DevTools to:

Measure actual spacing vs. design
Verify color values
Check computed font sizes and line heights
Test responsive behavior


Make adjustments based on DevTools feedback
Repeat until pixel-perfect

Responsive Design

Start with mobile-first approach unless specified otherwise
Use Tailwind's responsive prefixes (sm:, md:, lg:, xl:)
Test at key breakpoints: 375px, 768px, 1024px, 1440px
Maintain design integrity across all screen sizes

What NOT to Do
❌ Create additional pages or sections
❌ Use absolute/fixed positioning (except for overlays if needed)
❌ Add JavaScript interactivity without explicit ask
❌ Implement "nice to have" features
❌ Make assumptions about missing design elements

Custom styles.css Usage
Only use styles.css for:

Complex selectors Tailwind can't handle
Specific font imports
CSS variables for repeated custom values
Styles that would require excessive arbitrary Tailwind values

Keep it minimal - prefer Tailwind classes whenever possible.
Questions to Ask
Before implementing, clarify:

Exact hex values for custom colors
Specific font families and weights
Behavior at different screen sizes if not shown
Any interactive states (hover, active, focus)
Link destinations for any links in the design

Quality Checklist

 [] Matches Figma design exactly
 [] Uses Flexbox for all layouts
 [] No unnecessary custom CSS
 [] Verified with Chrome DevTools MCP
 [] Responsive at all breakpoints
 [] Clean, semantic HTML
 [] No added features or embellishments
 [] All spacings match design precisely