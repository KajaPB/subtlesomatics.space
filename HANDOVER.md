# Handover: Subtle Somatics Website Upgrade

## For the Claude session with Tana MCP access

You have access to Tana's local MCP server. Use it to pull content for upgrading subtlesomatics.space. This document tells you everything you need to know about the current state and what to do.

---

## Your Tana mission

Search Tana for ALL nodes related to:
- **#subtlesomatics** (or any supertag related to the brand/practice)
- **#post** (ideas Kaja wanted to publish)
- Anything about **somatic coaching**, **spinal energetics**, **presence-based work**
- Any **blog post drafts**, **writings**, **reflections**, **philosophy**
- Any **testimonials** or **client feedback** (real ones - see note below)
- **Bio / about** content for Kaja
- **Service descriptions**, **pricing**, **session formats**
- **Upcoming events**, **workshops**, **offerings**
- Any **quotes**, **poetry**, or **language** Kaja uses in her practice

### Tana MCP tools to use:
```
search_nodes - search for "subtlesomatics", "post", "somatic", "spinal energetics", "coaching", etc.
list_tags - find relevant supertags
get_tag_schema - understand the structure of content
read_node - read full content of each found node
```

Do multiple searches with different keywords. Be thorough. Kaja's Tana workspace likely has rich content that should populate the website.

---

## Important corrections

- **Kaya Orf is NOT Kaja's wife.** Do not include any such association.
- The practitioner's name is **Kaja Possert-Bienzle** (not Kaya, not Kaja Orf)
- Do not invent fake testimonials. The current site has placeholder testimonials (Emily Johnson, Michael Lee, Sarah L., John D., Emily R., James T.) - these should be replaced with REAL testimonials from Tana if available, or removed entirely.

---

## Current website state

### Tech stack
- **Astro 6.1.3** static site
- **No frameworks** (pure Astro/HTML/CSS)
- **Fonts**: Cormorant Garamond (headings) + Nunito Sans (body)
- **Colors**: Deep purple (#1F1346 / #673de6), cream (#f8f6f3), warm white
- **Site URL**: https://subtlesomatics.space
- **Repo**: github.com/KajaPB/subtlesomatics.space (you have push access via gh CLI at "/c/Program Files/GitHub CLI/gh.exe")

### Current pages (4 total)
1. **index.astro** - Hero with invitation text, about intro, 3 offering cards, 2 service cards, image break
2. **about.astro** - Mind-body connection, journey section, 4 values (Presence/Wholeness/Embodiment/Trust), placeholder testimonials
3. **services.astro** - Presence-Based Coaching + Spinal Energetics detail sections, session types, placeholder testimonials
4. **contact.astro** - Contact form, email/Instagram/sessions info, placeholder testimonials

### Current layout (Layout.astro)
- Fixed nav with logo + 4 links
- Footer with brand, contact, Instagram, email subscribe form
- WhatsApp floating button (currently links to empty wa.me/)
- Responsive with 768px breakpoint

### Current images (public/images/)
- hero.jpg (230KB) - hero background
- kaja-profile.jpg (36KB) - professional portrait
- kaja-secondary.png (137KB) - secondary image
- subtle-coaching.png (15KB) - service card image
- spinal-energetics.png (17KB) - service card image

---

## What to upgrade (based on Kaja's request for "the best and most attuned website")

### Content priorities (pull from Tana)
1. **Real testimonials** to replace all placeholders
2. **Blog/post content** - Kaja's writings, reflections, insights (consider adding a blog/writings page)
3. **Richer about/bio content** - Kaja's actual journey, training, background
4. **Service details** - actual pricing, session duration, booking links
5. **Kaja's own language** - her specific way of describing her work, her unique terminology and poetic voice
6. **WhatsApp number** - currently the button links to empty wa.me/
7. **Any events/workshops** coming up

### Design/structure improvements to consider
- Add a **blog/writings/insights page** if post content exists in Tana
- Add **real pricing/booking information** if available
- Fix the **WhatsApp link** with actual phone number
- Replace **placeholder testimonials** with real ones or remove them
- Add any **certifications/training** details
- Consider adding a **FAQ section** if relevant questions exist in Tana
- Update copyright year from 2025 to 2026
- Remove the "v0.3 early publication" note if the site is ready to be polished
- Make the **contact form functional** (currently action="#")

### Voice and tone guidance
Kaja's language on the current site is:
- Poetic and spacious ("the luminous wonder of deeper aliveness")
- Invitational, not prescriptive
- Uses words like: unfolding, presence, embodiment, innate, wholeness, aliveness, coherence, integration
- Describes herself as: "Unfolding companion, wholeness witnesser and integration facilitator"
- Keep this voice. Content from Tana should feel consistent with this.

---

## File paths (all relative to project root)

```
src/layouts/Layout.astro    - Master layout (nav, footer, global CSS)
src/pages/index.astro       - Home page
src/pages/about.astro       - About page
src/pages/services.astro    - Services page
src/pages/contact.astro     - Contact page
public/images/              - Image assets
astro.config.mjs            - Astro config
package.json                - Dependencies
```

## How to run locally

```bash
npm install
npm run dev      # starts dev server
npm run build    # builds static site
```

## How to deploy

Push to the `main` branch of `KajaPB/subtlesomatics.space` on GitHub. The site appears to be deployed from there.

---

## Summary of what to do

1. **Search Tana thoroughly** for all subtlesomatics/post content
2. **Read every relevant node** and extract usable content
3. **Update the website pages** with real content from Tana
4. **Add new pages** if Tana has blog/writing content worth publishing
5. **Replace all placeholder testimonials** with real ones from Tana
6. **Fix broken links** (WhatsApp, form action)
7. **Polish the design** to be the most attuned, beautiful somatic practitioner website possible
8. **Commit and push** when done

The goal: make this website feel as present, embodied, and attuned as the work Kaja does.
