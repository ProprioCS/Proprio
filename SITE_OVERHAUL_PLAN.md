# Proprio Cloud Solutions — Website Overhaul Plan

## Color Scheme (Derived from Logo)

| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| Primary Red | Proprio Red | `#C24F48` | CTAs, accent borders, hover states |
| Primary Blue | Checkmark Blue | `#3D6FB4` | Navigation, headings, links, trust elements |
| Dark Navy | Deep Blue | `#1B2A4A` | Dark sections, footer, hero overlay |
| Light Gray | Background | `#F7F8FA` | Alternating section backgrounds |
| White | Clean | `#FFFFFF` | Cards, main content background |
| Text Dark | Body | `#1A1A2E` | Primary body text |
| Text Light | Secondary | `#5A6278` | Descriptions, secondary copy |
| Success Green | Accent | `#2ECC71` | Checkmarks in feature lists |

### Color Usage Rules
- **Red** is the action color — buttons, CTAs, important highlights
- **Blue** is the trust/authority color — headings, navigation, feature icons
- **Never** use red and blue adjacent without a neutral separator
- Dark navy for high-contrast sections (hero, footer, testimonial bands)

---

## Site Structure (Single Page, 8 Sections)

### 1. Navigation Bar (Sticky)
- Logo (left)
- Links: Features | Modules | AI Innovation | About | Contact
- "Request a Demo" button (red, right-aligned)
- Transparent on hero, solid white with shadow on scroll

### 2. Hero Section
- **Background**: Dark navy gradient overlay on the existing office hero image
- **Headline**: "The ERP Built for Contract Furniture Dealers"
- **Subheadline**: "75+ custom modules purpose-built for contract furniture, running on NetSuite's rock-solid data security and enterprise platform."
- **CTA**: "Request a Demo" (red button) + "See Features" (ghost/outline button)
- **Trust bar** below hero: Small logos or text badges — "Built on NetSuite" | "75+ Custom Modules" | "MillerKnoll Integration" (verify any user counts with Luke before adding)

### 3. Problem/Solution Section
- **Heading**: "NetSuite Alone Wasn't Built for Furniture Dealers"
- Three-column layout with icon + short copy:

| Pain Point | Solution |
|-----------|----------|
| **Generic ERP, Specific Industry** — NetSuite doesn't understand dealer discounts, BOM specs, or multi-manufacturer sourcing | Orion adds contract furniture logic directly into NetSuite — dealer pricing, catalog codes, vendor-specific workflows |
| **Slow Order Entry** — Manual line-by-line entry from design software exports kills productivity | BOM Import ingests SIF, XML, and CSV files with drag-and-drop. Smart Table enables inline editing at scale |
| **Disconnected Operations** — Receiving, delivery, installation, and invoicing live in separate systems | One platform from quote through field installation, with real-time visibility at every stage |

### 4. Core Modules Section
- **Heading**: "Everything a Furniture Dealer Needs, Nothing They Don't"
- Card grid layout (2x3 or 3x2), each card has:
  - Icon (from a consistent icon set — suggest Lucide or Phosphor)
  - Module name
  - 2-sentence description
  - "Learn more" expand or anchor

#### Cards:

**Smart Table**
Edit lines directly across quotes, orders, and POs with real-time calculations. Import BOMs from design software, bulk-edit, and manage vendor acknowledgments — all in one view.

**Operations Suite**
Receiving, work orders, scheduling, and field dispatch in one connected system. Your warehouse and field teams work from the same data, with a mobile app that works offline.

**Purchase Order Management**
Generate POs directly from sales orders with intelligent splitting by vendor, address, and ship date. Acknowledgments are processed in-context so pricing discrepancies are caught immediately.

**Manufacturer Integrations**
Electronic ordering with MillerKnoll and Knoll — transmit POs, receive acknowledgments, validate pricing, and track shipments without manual re-entry.

**Invoice Scheduling & Commissions**
Automate invoicing tied to project milestones with reusable templates. Commissions calculate at the project level and true-up automatically as costs change.

**Kanban & Project Management**
Visual workflow boards for projects, opportunities, and design requests. Drag-and-drop cards with cycle time and throughput analytics built in.

### 5. AI Innovation Section (Existing Table, Reworked Presentation)
- **Heading**: "AI-Powered Innovation for Furniture Dealers"
- **Intro paragraph**: "We're building AI tools that solve real problems in the furniture industry — from contract analysis to financial reporting. These projects extend Orion's capabilities with intelligent automation."
- Keep the existing project table but style it as modern cards instead of a plain table:
  - Each AI project gets a small card with an icon, name, and description
  - Subtle "In Development" badge on each

### 6. Why Proprio Section
- **Heading**: "Why Dealers Choose Proprio"
- Two-column: left = bullet points, right = supporting image or illustration

**Bullet points:**
- **Industry expertise, not generic consulting** — Built by people who've worked inside NetSuite for furniture dealers for years
- **Single platform** — No bolt-on integrations to maintain. Orion lives inside NetSuite
- **Operational depth** — From warehouse receiving to field installation, not just back-office transactions
- **Manufacturer connections** — Electronic ordering with MillerKnoll and Knoll reduces errors and speeds fulfillment
- **Actively developed** — Regular releases with new features driven by dealer feedback

### 7. Contact Section
- **Heading**: "Let's Talk"
- **Subheading**: "See how Orion can work for your dealership"
- Embedded contact form:
  - Name (required)
  - Email (required)
  - Company (required)
  - Phone (optional)
  - Message / "What are you looking for?" (textarea, optional)
  - "Send Message" button (red)
- Note: Form submission will need a backend (options: Formspree, Netlify Forms, or a simple email endpoint). Since this is GitHub Pages, recommend **Formspree** for zero-backend form handling.

### 8. Footer
- Three columns:
  - **Left**: Logo + one-line company description
  - **Center**: Quick links (Features, Modules, AI, Contact)
  - **Right**: Contact info (email, phone — confirm with Luke what to list publicly)
- Copyright line at bottom
- Remove residential address (21265 Hasenclever Dr) — replace with just city/state or remove entirely

---

## Content Principles

1. **No outrageous claims** — Everything stated should be verifiable from the actual product
2. **Specificity sells** — "Import SIF and XML files with drag-and-drop" beats "streamline your workflow"
3. **Industry language** — Use terms dealers know: BOM, acknowledgments, dealer discounts, catalog codes
4. **Benefits over features** — Lead with the problem solved, then name the feature
5. **Honest AI positioning** — AI projects are real R&D efforts, not shipped features. Label them clearly
6. **PROTECT THE SECRET SAUCE** — Never reveal specific architecture, technical patterns, or implementation details. Describe *what* Orion does and *why* it matters, never *how* it's built. No mention of SuiteScript, Redux, specific record structures, or module architecture. The public message is: "75+ custom modules purpose-built for contract furniture on top of NetSuite's enterprise platform."

---

## Design Principles

1. **Clean, professional** — Lots of white space, consistent spacing, no visual clutter
2. **Modern but not trendy** — Inter font (keep it), subtle animations, no parallax gimmicks
3. **Mobile-first** — Responsive grid, stacked cards on mobile, readable font sizes
4. **Consistent iconography** — Pick one icon library and stick with it
5. **Photography** — Replace stock "red chairs" image. Use real Orion UI screenshots from Luxe 1 demo environment (scrubbed of sensitive data) plus modern office/warehouse imagery

---

## Technical Approach

- **Single HTML file** — Keep the current GitHub Pages approach (simple, fast, no build step)
- **CSS custom properties** — Expand the existing variable system with new color scheme
- **No framework** — Vanilla HTML/CSS/JS is fine for a marketing page
- **Form handling** — Formspree (free tier: 50 submissions/month) or similar
- **Fonts** — Keep Inter, possibly add a display weight for hero headlines
- **Icons** — Inline SVGs from Lucide (lightweight, consistent)

## Product Screenshots (Luxe 1)

Take real screenshots from **Luxe 1** demo environment to use as product imagery:
- Smart Table (showing inline editing, BOM import, bulk operations)
- Operations Suite (receiving drag-and-drop, scheduling calendar)
- Kanban board with cards
- Field interface (mobile view)
- Expected Receipts calendar

Screenshots should be cropped to highlight the UI without exposing sensitive data, customer names, or underlying architecture details. Blur or redact any customer-specific information.

## Herman Miller Environment Images

Source: https://www.hermanmiller.com/en_eur/resources/images/?q=office&ft=Environment
- 125+ high-quality office environment photos available (authorized for use)
- Available in Low (527x720), Medium (2196x3000), and High (2196x3000) resolution
- Download via detail panel on each image

**Recommended usage by section:**

| Section | Image Style | Search Terms |
|---------|------------|--------------|
| Hero background | Wide office environment, open plan | `office` (Environment filter) |
| Problem/Solution | Collaborative workspace | `collaboration`, `meeting` |
| Why Proprio | Modern workplace, executive feel | `office`, `workspace` |
| About section | Team/collaborative setting | `collaboration`, `team` |

**Notes:**
- Use Medium resolution (2196x3000) and compress for web — aim for ~200KB per image
- The blue-toned office shots (Atlas Office Landscape series) align well with the Proprio blue color scheme
- Crop to wide aspect ratios (16:9 or wider) for hero and section backgrounds
- Apply a dark overlay (like existing hero) to maintain text readability over photos

---

## Sections Removed
- ~~Video Library / Demos~~ — No content available yet
- ~~"Founded by Luke Abbott"~~ — Move to About or remove (company credibility > personal attribution on landing page)

## Sections Added
- Navigation bar
- Problem/Solution section
- Core Modules detail cards
- Why Proprio bullet points
- Contact form

---

## Open Questions for Luke

1. **Trust bar numbers** — How many active dealer users? How many transactions processed? Any metrics we can cite?
2. **Contact info** — What email/phone should be public on the site?
3. **Photography** — Can we use actual Orion UI screenshots? Or do we need to stick with stock imagery?
4. **Form submissions** — Where should form submissions go? (Formspree → email? Specific inbox?)
5. **Company description** — Is there a preferred one-liner beyond "Bringing AI to the NetSuite Ecosphere"?
6. **Footer address** — Keep the South Lyon address, switch to just "Michigan, USA", or remove?
7. **Team section** — Should there be an About/Team section with bios, or keep it company-focused?
