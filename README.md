# Kavya — "I Make Sense of Messy Products" Portfolio

Theme: light gray + Poppins + yellow/red/teal circle accents (Wix template style), with the scroll-story animation layer (Motion / motion.dev, vendored inline).

A single-file, zero-build creative portfolio. Everything lives in `index.html`; `Kavya_Chaturvedi_Resume.pdf` sits beside it for the "Download résumé" button.

## Deploy to Vercel

**Same project, same URL (recommended):** if you deployed via GitHub, replace the files in your repo with these two and push — Vercel redeploys automatically at kavya-portfolio-eta.vercel.app.

**Drag and drop:** go to https://vercel.com/new and drag this whole folder onto the page → Deploy.

**CLI:**
```bash
cd kavya-creative
vercel --prod
```

## Scroll animation — powered by Motion (motion.dev)

The Motion library is vendored (inlined) into `index.html`, so there is still nothing to install and no CDN dependency. Its `scroll()` API drives every scroll-linked effect below.

**The hero is now a scroll story:** on load the headline letters lie scattered in a tangle of lines — the mess. As you scroll, the letters fly into place, the tangle retracts and fades, the scribble strikes through MESSY, a clean orange line draws itself across, the arrowhead lands, and "the outcome" dot pops in — then the page releases into the ticker. On phones and for reduced-motion users the hero renders fully assembled and static.

Other effects:

- **Smooth inertia scrolling** on desktop (disabled on touch + for reduced-motion users)
- **Scroll progress bar** across the top (Motion `scroll()` → `scaleX`)
- **Pinned "How I Think" sequence** — the section sticks while a tangled line draws itself through the five sticky notes, flattening into a straight arrow as each note pops in
- **Pinned horizontal scroll** on "Currently Exploring" — cards travel sideways as you scroll down
- **Word-by-word heading reveals**, staggered
- **Parallax** on the photo and hero diagram; **clip-path wipe** on the photo
- **Counters** that count up when they enter view
- **Velocity-linked ticker** — scroll faster and the marquee speeds up; scroll up and it reverses

To tune: the hero story length is `header.hero-outer{height:300vh}`; the pinned sections' length is CSS — `.pin-outer{height:330vh}` and `.hz-outer{height:300vh}`. Bigger = slower, more scrolling. Smooth-scroll feel is the `0.115` lerp in the main loop (lower = floatier). To turn smooth scrolling off entirely, set `var SMOOTH = false;` in the script.

## What's interactive

- Hero: animated "mess → outcome" line drawing, scribble over MESSY
- Marquee ticker, custom cursor, scroll reveals
- "Things I've built" — click any card to expand THE MESS / MY QUESTION / WHAT I DID / OUTCOME
- "Try me" — visitor picks A/B/C, your reasoning types itself out
- Unpopular opinions — click to reveal reasoning
- "Give me a messy problem" — visitor types a problem, sees your untangling framework animate, and the "send it to me" link opens an email with their text pre-filled

## Editing

All copy is plain HTML in `index.html`. The typed-out scenario answers live in the `answers` object near the bottom of the file.
