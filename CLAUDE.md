# CLAUDE.md - Instructions for Claude Code

## Project: My Second Brain
A landing page for a digital product business targeting moms with AI prompts for managing mental load.

## What's Already Done
- ✅ Landing page HTML/CSS (`my-second-brain-landing.html`) - complete and styled
- ✅ Lead magnet PDF (`my-second-brain-lead-magnet.pdf`) - 10 prompts, ready to deliver
- ✅ All copy written (`COPY.md`)
- ✅ Full project spec (`PROJECT-SPEC.md`)

## What Needs To Be Done

### Priority 1: Email Integration
The landing page has two email forms that need to be connected to an email service.

**Current state:** Forms have placeholder JavaScript that logs to console
**Needed:** Real integration with ConvertKit, Beehiiv, or Mailchimp

Options:
1. **Simple form action** - Update `<form>` to post directly to email service
2. **API integration** - Use fetch to submit to email service API
3. **Embedded form** - Replace with email service's embed code

The user will need to:
1. Create account with email service
2. Create a form/signup
3. Get the form ID or API endpoint
4. Provide it to Claude Code for integration

### Priority 2: Deployment
Deploy to mysecondbrain.xyz

**Recommended approach:**
1. Create a simple project structure (can stay as single HTML or convert to basic framework)
2. Deploy to Vercel or Netlify
3. Connect custom domain

**If converting to a framework:**
- Next.js is a good option for future expansion
- Keep it simple - don't over-engineer for a landing page

### Priority 3: PDF Delivery
Set up automated PDF delivery when someone subscribes:
1. Upload PDF to email service
2. Configure welcome email to include download link
3. Test the full flow

## File Structure

```
/my-second-brain/
├── CLAUDE.md                       # This file
├── PROJECT-SPEC.md                 # Full project specification
├── COPY.md                         # All copy/text content
├── my-second-brain-landing.html    # Landing page (ready to deploy)
└── my-second-brain-lead-magnet.pdf # Lead magnet PDF
```

## Key Technical Details

### Colors (CSS Variables)
```css
--sage: #5B7B6D
--sage-light: #7A9A8C
--cream: #FAF8F5
--coral: #E8A598
--charcoal: #2D3436
```

### Fonts
- Fraunces (headings) - Google Fonts
- Source Sans 3 (body) - Google Fonts

### Forms
There are two identical forms on the page:
1. Hero section form (`#get-it`)
2. Final CTA section form

Both need to submit to the same email list.

## Commands

If converting to a proper project:

```bash
# Create Next.js project
npx create-next-app@latest my-second-brain --typescript --tailwind --app

# Or keep it simple with just the HTML file and deploy
# Vercel can deploy a single HTML file directly
```

## Questions for the User

Before proceeding, Claude Code should ask:
1. Which email service do you want to use? (ConvertKit, Beehiiv, Mailchimp, other?)
2. Do you want to keep this as a simple HTML file or convert to Next.js?
3. Which hosting do you prefer? (Vercel, Netlify, other?)
4. Do you have the domain (mysecondbrain.xyz) set up with a registrar?

## Design Notes

The design is intentionally warm and approachable, not corporate. Key elements:
- Sage green as primary color (calm, natural)
- Coral accents (warmth, energy)
- Cream background (soft, not stark white)
- Fraunces serif font (distinctive, not generic)
- Rounded corners, soft shadows
- Floating card animations in hero

Do NOT:
- Make it look like a typical tech/SaaS page
- Use harsh colors or stark white backgrounds
- Make it feel corporate or cold
- Over-engineer the animations

## Future Expansion

The user plans to add:
- Product pages for paid prompt packs
- Blog for SEO content
- Prompt library page
- About page

Keep architecture simple but extensible for these additions.
