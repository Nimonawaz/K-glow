# Design Guidelines: Korean Skincare E-Commerce Platform

## Design Approach
**Reference-Based**: Drawing inspiration from premium beauty e-commerce platforms (Glossier, Glow Recipe, YesStyle) combined with K-beauty aesthetic principles—clean minimalism, soft sophistication, and ingredient transparency.

## Core Design Principles
1. **Visual Trust**: High-quality product imagery with clean backgrounds to showcase skincare authenticity
2. **Calm Sophistication**: Gentle, approachable design that reflects skincare's nurturing qualities
3. **Information Clarity**: Easy-to-scan ingredient lists and skin type indicators
4. **Mobile-First Commerce**: Touch-friendly interactions, optimized product browsing

---

## Color Palette

### Light Mode
- **Primary**: 340 100% 85% (Soft Pink) - CTAs, accents, highlights
- **Secondary**: 130 30% 85% (Sage Green) - secondary actions, trust indicators
- **Neutral Base**: 30 25% 96% (Warm Beige) - backgrounds, cards
- **Text**: 0 0% 20% (Charcoal) - primary text
- **Borders**: 30 15% 88% (Light Taupe) - dividers, input borders

### Dark Mode
- **Primary**: 340 70% 70% (Muted Rose)
- **Secondary**: 130 25% 65% (Muted Sage)
- **Background**: 30 10% 12% (Dark Warm)
- **Surface**: 30 8% 18% (Elevated Dark)
- **Text**: 30 5% 92% (Off-white)

---

## Typography

**Primary Font**: 'Plus Jakarta Sans' (Google Fonts) - Modern, approachable, excellent readability
**Accent Font**: 'Cormorant Garamond' (Google Fonts) - Elegant serif for hero headlines only

### Type Scale
- **Hero**: text-5xl md:text-6xl lg:text-7xl, font-light (Cormorant)
- **H1**: text-3xl md:text-4xl, font-semibold
- **H2**: text-2xl md:text-3xl, font-semibold
- **H3**: text-xl md:text-2xl, font-medium
- **Body**: text-base, font-normal, leading-relaxed
- **Small**: text-sm, font-normal
- **Micro**: text-xs, uppercase tracking-wide (labels, tags)

---

## Layout System

**Spacing Primitives**: Use Tailwind units of 2, 4, 6, 8, 12, 16, 20, 24
- **Component spacing**: gap-4, gap-6, gap-8
- **Section padding**: py-12 md:py-16 lg:py-20
- **Container padding**: px-4 md:px-6 lg:px-8
- **Card padding**: p-4 md:p-6

**Responsive Breakpoints**:
- Mobile: base (default)
- Tablet: md: (768px)
- Desktop: lg: (1024px)
- Wide: xl: (1280px)

**Grid Systems**:
- Product grid: grid-cols-2 md:grid-cols-3 lg:grid-cols-4
- Feature grid: grid-cols-1 md:grid-cols-2 lg:grid-cols-3
- Bundle cards: grid-cols-1 md:grid-cols-2 lg:grid-cols-5

**Max Widths**:
- Full sections: max-w-7xl
- Content areas: max-w-6xl
- Product details: max-w-5xl
- Text content: max-w-prose

---

## Component Library

### Navigation
- **Header**: Sticky top navigation, backdrop-blur, border-b, dual currency toggle (USD/PKR), cart icon with item count badge
- **Mobile nav**: Slide-in drawer with category navigation
- **Search bar**: Prominent, with category filter dropdown

### Hero Section
- **Large hero image**: Full-width lifestyle shot showcasing Korean skincare routine (dewy skin, natural light, minimal props)
- **Height**: h-[500px] md:h-[600px] lg:h-[700px]
- **Overlay content**: Centered text with backdrop-blur background on buttons, Cormorant headline, subtitle explaining value proposition, dual CTA buttons

### Product Cards
- **Image**: aspect-square, object-cover, rounded-lg, hover:scale-105 transition
- **Badge**: Absolute positioned "New" or "Best Seller" tags (top-left)
- **Title**: font-medium, truncate
- **Price**: Dual currency display (USD primary, PKR secondary in text-sm)
- **Skin type tags**: Flex row of small pills (e.g., "Dry", "Sensitive")
- **Add to cart**: Full-width button on hover (desktop), always visible (mobile)

### Product Detail Page
- **Layout**: Two-column (image gallery + details) on lg:, stacked on mobile
- **Image gallery**: Thumbnails + main large image viewer
- **Details section**: Product name, price, star rating, skin type indicators, ingredient accordion, quantity selector, add to cart CTA
- **Tabs**: Description | Ingredients | How to Use | Reviews

### Shopping Cart
- **Drawer**: Slide-in from right on desktop, full-page on mobile
- **Item card**: Product thumbnail, name, price, quantity adjuster, remove button
- **Summary**: Subtotal, estimated shipping, total (dual currency)
- **CTAs**: Continue shopping (outline), Checkout (primary)

### Checkout Form
- **Layout**: Two-column (form + order summary sidebar) on lg:
- **Sections**: Customer info, Shipping address, Payment placeholder
- **Inputs**: Consistent border-2 rounded-lg, focus:ring-2 ring-primary
- **Order summary**: Sticky sidebar showing cart items, totals

### Bundles Section
- **Card design**: Vertical cards with stacked product images, bundle name, savings badge, discounted price
- **Grid**: 5 columns on lg:, 2 on md:, 1 on base

### Footer
- **Layout**: Four-column grid (lg:), stacked on mobile
- **Sections**: Shop categories, Customer care, About, Newsletter signup
- **Newsletter**: Input + submit inline, social media icons
- **Trust badges**: Payment methods, secure checkout icons

---

## Images

### Hero Section
**Primary hero image**: Lifestyle shot featuring a person with glowing, hydrated skin applying or holding Korean skincare products. Natural lighting, soft focus background, dewy skin texture visible. Calming aesthetic with plants or minimal decor. Image should convey freshness and self-care ritual.

### Product Images
Clean, white-background product shots with soft shadows. Consistent angle (slight 3/4 view). Show texture/translucency of products where applicable.

### Category Banners
Close-up lifestyle shots: hands applying serums, water droplets on skin, natural ingredients (rice, green tea, snail mucin visualization).

### Testimonial Section
Optional: Customer photos with before/after skin improvements or holding favorite products.

---

## Interactions & Animations

**Use sparingly**:
- Product card hover: Scale 1.05, shadow increase (transition-all duration-300)
- Image gallery: Smooth fade transitions
- Cart drawer: Slide-in animation (translate-x)
- Add to cart: Subtle shake on validation error
- Loading states: Skeleton screens for product grids

**No animations**: Page transitions, scroll effects, excessive micro-interactions

---

## Accessibility & Dark Mode

- Maintain WCAG AA contrast ratios (4.5:1 for text)
- Dark mode: Consistent across all pages, including forms and inputs
- Focus indicators: Visible ring-2 ring-offset-2
- Touch targets: Minimum 44x44px on mobile
- Alt text: Descriptive product image alternatives

---

## Icons

**Library**: Heroicons (via CDN)
- Cart, search, user profile, menu, close, chevrons, heart (wishlist), star (ratings), check (verified ingredients)

This design system creates a trustworthy, sophisticated Korean beauty e-commerce experience that prioritizes product discovery and mobile shopping while maintaining visual elegance.