# PROJECT PLAN — DELISHA KARIGARI SHOPIFY STORE REDESIGN

## 1. Executive Overview & Brand Context

**DELISHA KARIGARI** is a premium modern Indian lifestyle and gifting ecommerce brand specializing in handcrafted products including Rakhi, Lumba, Toran, Latkan, Bangles, Kada, Fine & Fashion Jewellery (Earrings, Rings, Necklaces, Mangalsutra, Bracelets), Watches, Festive Decor, and Curated Gift Sets.

This plan details the transformation of the storefront into a warm, elegant, modern Indian shopping experience inspired by high-end Indian artisanal commerce while establishing a unique visual identity for DELISHA KARIGARI.

---

## 2. Shopify Environment & Safety Status Audit

* **Local Workspace**: `c:\DKshopify` (contains full theme structure copied & verified).
* **Shopify CLI Installation**: Version `4.6.1` installed and functional.
* **Shopify Authentication**: Store domain connection required (`--store=your-store.myshopify.com`).
* **Safety Protocols**:
  * Live theme will **NOT** be modified or published automatically.
  * All development will take place locally / on unpublished development theme copies.
  * No destructive commands (theme delete, product delete, collection delete) will be executed.

---

## 3. Current Theme Architecture & Existing Assets

### Theme Directory Structure
```
c:\DKshopify\
├── assets/
│   ├── cart-drawer.js
│   ├── theme.css
│   ├── theme.js
│   └── wishlist.js
├── blocks/
│   ├── button.liquid
│   ├── image.liquid
│   └── text.liquid
├── config/
│   ├── settings_data.json
│   └── settings_schema.json
├── layout/
│   └── theme.liquid
├── locales/
│   └── en.default.json
├── sections/
│   ├── announcement-bar.liquid
│   ├── brand-story.liquid
│   ├── cart-drawer.liquid
│   ├── circular-categories.liquid
│   ├── collection-banner.liquid
│   ├── deal-of-day.liquid
│   ├── delisha-grid.liquid
│   ├── featured-collections.liquid
│   ├── footer.liquid
│   ├── header.liquid
│   ├── hero-banner.liquid
│   ├── main-cart.liquid
│   ├── main-collection-product-grid.liquid
│   ├── main-list-collections.liquid
│   ├── main-product.liquid
│   ├── product-banner-breadcrumb.liquid
│   ├── product-description-tabs.liquid
│   ├── product-grid.liquid
│   ├── promotional-banner.liquid
│   ├── rakhi-offer-banner.liquid
│   ├── related-products.liquid
│   ├── sale-offer-slider.liquid
│   ├── shop-by-collection.liquid
│   ├── sticky-product-bar.liquid
│   └── wishlist-drawer.liquid
├── snippets/
│   ├── all-collections-list.liquid
│   ├── cart-item.liquid
│   ├── collection-card.liquid
│   ├── pagination.liquid
│   ├── product-card.liquid
│   └── search-modal.liquid
└── templates/
    ├── cart.json
    ├── collection.json
    ├── index.json
    ├── list-collections.json
    ├── page.about.liquid
    ├── page.contact.liquid
    ├── page.faqs.liquid
    ├── page.refund-policy.liquid
    ├── page.shipping-policy.liquid
    ├── product.json
    ├── search.liquid
    └── customers/
        ├── account.liquid
        ├── login.liquid
        └── register.liquid
```

---

## 4. Design System & Visual Identity

### Color Palette
* **Primary Background**: `#F9F5EE` (Warm Off-White / Ivory)
* **Secondary Background**: `#F2E5DD` (Soft Warm Nude / Sand)
* **Primary Brand Accent**: `#6E1F2A` (Deep Royal Burgundy / Maroon)
* **Muted Gold**: `#B89552` (Subtle Champagne Gold)
* **Primary Text**: `#252525` (Soft Charcoal Black)
* **Card & Module Backgrounds**: `#FFFFFF` (Pure White)

### Typography
* **Headings / Editorial Titles**: `Playfair Display` (Serif — Elegant, Sophisticated)
* **Body / Navigation / UI / Buttons**: `Poppins` or `Inter` (Clean Sans-Serif — Modern, Readable)

### Design Guidelines
* Generous whitespace & editorial padding
* Subtle single-pixel borders (`rgba(110, 31, 42, 0.12)`)
* Micro-interactions & soft hover transitions (0.3s ease)
* Responsive cards & mobile-first tap targets (minimum 44px)

---

## 5. Homepage Information Architecture & Section Plan

The homepage will be structured into a dynamic, merchant-configurable flow in `templates/index.json`:

1. **Announcement Bar** (`sections/announcement-bar.liquid`) — Rotating banner for free shipping & festive offers.
2. **Header / Navigation** (`sections/header.liquid`) — Logo, search, wishlist trigger, cart trigger, and mega-menu/dropdowns.
3. **Hero Banner** (`sections/hero-banner.liquid`) — High-impact slider/banner with mobile & desktop images, overlay settings, and strong CTA.
4. **Shop By Category** (`sections/shop-by-category.liquid` - *[NEW]* or upgrade `circular-categories.liquid`) — Visual category discovery grid (Rakhi, Toran, Latkan, Bangles, Earrings, Jewellery, Gifting, Festive Decor).
5. **Shop By Occasion** (`sections/shop-by-occasion.liquid` - *[NEW]*) — Raksha Bandhan, Wedding, Festive, Housewarming, Birthday, Gifting.
6. **Bestsellers Carousel / Grid** (`sections/featured-collections.liquid` / `sections/product-grid.liquid`) — Collection picker powered bestseller shelf with `product-card.liquid`.
7. **New Arrivals** (`sections/new-arrivals.liquid` - *[NEW]*) — Highlight new handcrafted arrivals with reusable product cards.
8. **Curated Gifting** (`sections/curated-gifting.liquid` - *[NEW]*) — Editorial highlight section ("Gifts That Feel Personal").
9. **Shop By Recipient** (`sections/shop-by-recipient.liquid` - *[NEW]*) — For Her, For Him, For Mom, For Dad, For Sister, For Brother, For Kids, For Friends.
10. **Festive Promotional Banner** (`sections/promotional-banner.liquid`) — Full-width reusable campaign section with mobile/desktop images & CTAs.
11. **Why DELISHA KARIGARI** (`sections/why-delisha.liquid` - *[NEW]*) — Handcrafted, Premium Quality, Beautiful Gifting, Fast Shipping trust badges.
12. **Trending Products** (`sections/trending-products.liquid` - *[NEW]*) — Featured carousel of trending handcrafted items.
13. **Brand Story** (`sections/brand-story.liquid`) — "Crafted with Love" narrative highlighting Indian craftsmanship.
14. **Instagram / Social Section** (`sections/social-gallery.liquid` - *[NEW]*) — Responsive 4–6 photo grid with social callout.
15. **Blog / Gifting Guide** (`sections/featured-blog.liquid` - *[NEW]*) — Displays articles from Shopify Blog system.
16. **Newsletter** (`sections/newsletter.liquid` - *[NEW]*) — Native Shopify newsletter subscription form.
17. **Footer** (`sections/footer.liquid`) — Comprehensive shop navigation, help links, brand policies, social handles, and copyright.

---

## 6. Product Card & Merchandising Strategy

### Snippet: `snippets/product-card.liquid`
* **Desktop Features**:
  * Dual image hover (primary & secondary hover image)
  * Sale badge / Sold-out badge overlay
  * Wishlist quick-toggle button
  * Clean typography for product title & price formatting (`money_with_currency`)
  * Compare-at price strike-through
  * Quick Add / Add to Cart drawer button
* **Mobile Optimizations**:
  * Touch-friendly layout with standard target heights (>= 44px)
  * Clear sale tags and easy swipe/tap accessibility

---

## 7. Files to Modify & Files to Create

### Files Recommended to Modify
* `layout/theme.liquid`: Integrate custom font loading, CSS variables, structured schema.
* `assets/theme.css`: Core design system, color variables, typography, component styling (`dk-` prefixed).
* `assets/theme.js`: Cart drawer interaction, wishlist toggle, carousel behavior.
* `sections/header.liquid`: Mega-menu support, brand navigation styling.
* `sections/footer.liquid`: Brand policy links, newsletter form, category links.
* `sections/announcement-bar.liquid`: Top announcement ticker with multi-message support.
* `sections/hero-banner.liquid`: Enhancing slide options, overlay controls, button styling.
* `sections/brand-story.liquid`: Fine-tuning typography, spacing, and layout.
* `sections/promotional-banner.liquid`: Adding responsive image controls.
* `snippets/product-card.liquid`: Modernizing card architecture, badges, quick add.
* `templates/index.json`: Rebuilding homepage section configuration.
* `templates/product.json`: Structuring product page layout.
* `templates/collection.json`: Enhancing filtering & grid view.
* `config/settings_schema.json`: Adding DELISHA KARIGARI brand color tokens & typography options.

### Files Recommended to Create
* `sections/shop-by-category.liquid`: Dynamic category cards with collection pickers.
* `sections/shop-by-occasion.liquid`: Festive & occasion grid with URL/collection pickers.
* `sections/shop-by-recipient.liquid`: Recipient card grid with custom images and collection links.
* `sections/curated-gifting.liquid`: Editorial banner for personalized gifting.
* `sections/why-delisha.liquid`: 4-column trust/value icon block.
* `sections/social-gallery.liquid`: Instagram-style image grid.
* `sections/featured-blog.liquid`: Dynamic blog article picker section.
* `sections/newsletter.liquid`: Native newsletter signup block.
* `snippets/mega-menu.liquid`: Multi-column dropdown snippet for main navigation.

---

## 8. Mobile, Performance, SEO & Accessibility Strategy

* **Mobile Strategy**: Mobile-first design for touch screens, fixed slideouts for navigation and cart drawer, optimized image sizing.
* **Performance Strategy**: Native Shopify `image_url` filter with explicit width density descriptors (`srcset`), `loading="lazy"`, native CSS grid/flexbox, zero heavy external frameworks.
* **SEO Strategy**: Strict single `<h1>` hierarchy per page, rich snippet JSON-LD metadata for Products & Organization, descriptive `alt` tags using Shopify dynamic fallbacks.
* **Accessibility Strategy**: High contrast ratios, full keyboard navigation support, visible focus rings, valid ARIA labels for buttons and modals.

---

## 9. 16-Phase Development Roadmap

1. **Phase 1**: Theme setup & complete architecture audit *(Completed)*
2. **Phase 2**: Brand design system implementation (`theme.css` tokens & typography)
3. **Phase 3**: Announcement Bar + Header + Navigation overhaul
4. **Phase 4**: Hero Banner enhancement
5. **Phase 5**: Shop By Category & Shop By Occasion sections
6. **Phase 6**: Product sections & enhanced `product-card.liquid`
7. **Phase 7**: Curated Gifting & Shop By Recipient sections
8. **Phase 8**: Brand Story + Why DELISHA KARIGARI trust bar
9. **Phase 9**: Social Gallery + Blog Guide + Newsletter sections
10. **Phase 10**: Footer overhaul
11. **Phase 11**: Product Page (`templates/product.json` & `main-product.liquid`) refinement
12. **Phase 12**: Collection Page (`templates/collection.json`) refinement
13. **Phase 13**: Cart & Search drawers/pages
14. **Phase 14**: Comprehensive Mobile Optimization
15. **Phase 15**: Performance, SEO & Accessibility verification
16. **Phase 16**: Final QA, Theme Check & merchant handoff presentation
