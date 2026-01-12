# My Second Brain - Project Spec

## Overview
**My Second Brain** is a lead generation landing page for a digital product business targeting moms. The product helps moms use AI to manage their mental load through copy-paste prompts for everyday situations.

**Domain:** mysecondbrain.xyz

## What We're Building

### Phase 1: Landing Page (MVP)
A single-page website to capture email addresses in exchange for a free PDF guide ("10 AI Prompts That'll Give You Your Brain Back").

### Core User Flow
1. Mom lands on page (likely from social media, word of mouth, or search)
2. Sees headline, relates to pain points
3. Views what's included in free guide
4. Enters email
5. Receives PDF via email
6. Gets added to email list for future products

---

## Technical Requirements

### Hosting
- Static site (can deploy to Vercel, Netlify, or any static host)
- Domain: mysecondbrain.xyz

### Email Integration
- **Recommended:** ConvertKit, Beehiiv, or Mailchimp
- Need to set up:
  - Email capture form integration
  - Welcome email with PDF attachment/download link
  - Email list/audience for future marketing

### Tech Stack Options
**Option A: Simple HTML/CSS/JS (Recommended for speed)**
- Single HTML file (provided)
- Easy to deploy anywhere
- Form posts to email service

**Option B: React/Next.js (If planning to expand)**
- More structure for future pages
- Better for adding blog, product pages later
- Slightly more complex deployment

### Form Integration Code Needed
The landing page has placeholder form handling. Need to replace with actual integration:

```javascript
// Current placeholder - needs replacement
form.addEventListener('submit', function(e) {
    e.preventDefault();
    // TODO: Replace with actual form submission
});
```

**ConvertKit example:**
```html
<form action="https://app.convertkit.com/forms/YOUR_FORM_ID/subscriptions" method="post">
    <input type="email" name="email_address" placeholder="Enter your email" required>
    <button type="submit">Send Me the Guide</button>
</form>
```

**Beehiiv example:**
```html
<form action="https://embeds.beehiiv.com/YOUR_PUBLICATION_ID" method="post">
    <input type="email" name="email" placeholder="Enter your email" required>
    <button type="submit">Send Me the Guide</button>
</form>
```

---

## Design Specs

### Brand Colors
```css
--sage: #5B7B6D          /* Primary - buttons, accents */
--sage-light: #7A9A8C    /* Hover states */
--sage-pale: #D4E2DB     /* Light backgrounds */
--sage-wash: #EEF4F1     /* Very light backgrounds */
--cream: #FAF8F5         /* Page background */
--cream-dark: #F5F1EB    /* Section backgrounds */
--coral: #E8A598         /* Accent - eyebrows, highlights */
--coral-deep: #D4877A    /* Darker coral */
--charcoal: #2D3436      /* Primary text */
--gray: #636E72          /* Secondary text */
```

### Typography
- **Headings:** Fraunces (Google Fonts) - serif, warm, distinctive
- **Body:** Source Sans 3 (Google Fonts) - clean, readable

### Fonts Import
```html
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,500;0,9..144,600;0,9..144,700;1,9..144,400;1,9..144,500&family=Source+Sans+3:wght@300;400;500;600&display=swap" rel="stylesheet">
```

### Design Tone
- Warm, not corporate
- Speaks directly to her ("you" language)
- Relatable, not preachy
- Clean but not cold
- Professional but not stuffy

---

## Page Structure

### 1. Navigation
- Logo: "My Second Brain" (text, Fraunces font)
- CTA button: "Get the Free Guide" → scrolls to form

### 2. Hero Section
- Eyebrow: "For moms who carry everything"
- Headline: "Finally, a way to get your brain back"
- Subhead: Description of what the guide offers
- Email capture form
- Trust note: "Free download. No spam, just actual help."
- Floating card illustrations (optional decorative element)

### 3. "Sound Familiar?" Section
- Dark sage background
- 6 relatable thought bubbles:
  - "Did I respond to that email or just think about responding?"
  - "It's 5pm and I have no idea what's for dinner. Again."
  - "How do I explain this to a 6-year-old without scarring them?"
  - "I need to say no to this but I can't find the words."
  - "What are we out of? We're out of something..."
  - "The birthday party is in 3 days and I haven't planned anything."
- Closing message: "You're not losing your mind. You're just carrying more than any one brain was designed to hold."

### 4. What's Inside Section
- 6 benefit cards with icons:
  1. 🍳 Meals Without the Mental Gymnastics
  2. ✉️ Emails You'll Actually Send
  3. 💬 Scripts for Hard Conversations
  4. 🎈 Party Planning Without Pinterest Panic
  5. 📚 Homework Help (Without Doing It)
  6. 🧘 Overwhelm → Clarity

### 5. Sneak Peek Section
- Shows one full prompt example (The "What's For Dinner" Solver)
- Includes the prompt text, why it works
- "Plus 9 more prompts" teaser

### 6. Final CTA Section
- Headline: "Ready to get your brain back?"
- Email capture form (duplicate of hero form)
- Trust note

### 7. Footer
- Logo
- Tagline: "AI-powered relief for the mental load"

---

## Files Included

```
/my-second-brain/
├── my-second-brain-landing.html    # Complete landing page
├── my-second-brain-lead-magnet.pdf # Free guide PDF
├── PROJECT-SPEC.md                 # This file
└── COPY.md                         # All copy/text content
```

---

## Future Expansion (Phase 2+)

### Additional Pages to Build Later
- `/products` - Paid prompt packs
- `/blog` - SEO content
- `/about` - Story/mission
- `/library` - Free prompt samples

### Potential Paid Products
- Meal Planning Deep Dive ($17-27)
- School Year Survival Pack ($17-27)
- Birthday Party Playbook ($17-27)
- Boundary Scripts Bundle ($17-27)
- Summer Sanity Pack ($17-27)
- Complete Course: "AI Confidence in 7 Days" ($47-97)
- Membership: Monthly new prompts + community ($19-29/mo)

### Email Sequences to Build
1. Welcome sequence (deliver PDF + introduce brand)
2. Nurture sequence (more free value)
3. Product launch sequence (when paid products ready)

---

## Deployment Checklist

- [ ] Set up email service account (ConvertKit/Beehiiv/Mailchimp)
- [ ] Create form and get embed code
- [ ] Upload PDF to email service for delivery
- [ ] Create welcome email with PDF download
- [ ] Update form action URLs in HTML
- [ ] Deploy to hosting (Vercel/Netlify)
- [ ] Connect custom domain (mysecondbrain.xyz)
- [ ] Test full flow: submit email → receive PDF
- [ ] Set up basic analytics (Plausible, Fathom, or Google Analytics)

---

## Copy Notes

### Voice Guidelines
- Use "you" language, speak directly to her
- Acknowledge the hard stuff without wallowing
- Warm but not saccharine
- Funny in a dry, "we're all in this chaos together" way
- Zero judgment
- Assumes she's smart and capable, just stretched thin

### Words to Use
- "Mental load"
- "The invisible stuff"
- "Get your brain back"
- "Thinking partner"
- "Relief"

### Words to Avoid
- "Mompreneur" / "boss mom" / "supermom"
- "Productivity hacking"
- "Self-care" (overused)
- "Easy" (nothing feels easy)
- Anything condescending about tech ability
