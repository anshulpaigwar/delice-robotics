# Delice Robotics — startup / sales site

A single-file site (`index.html`, no build step) positioning RoboDélice as a product
to sell and pitch. Smooth scrolling and scroll animations via GSAP + Lenis (loaded
from CDN). The hero plays a looping background video.

## Sections (in order)
1. **Hero** — background video + headline + CTAs (View pitch deck / Request a demo)
2. **Product & features** — the RoboDélice platform
3. **Technical specs** — editable spec table (replace with verified figures)
4. **Use cases / locations** — where the kiosk can be placed
5. **Videos** — YouTube embeds (click to load)
6. **Gallery** — food photos as small thumbnails, click to enlarge
7. **Pitch deck** — cover, contents, PDF download / meeting CTA (embed optional)
8. **Team**
9. **Mentors / scientific advisors**
10. **Incubator & partners** — Inria + EHL
11. **Story**
12. **Contact CTA** + footer

## Add your content
- **Hero video** → `assets/video/hero.mp4` (short, muted, looping; ~3-8 MB).
  Add `assets/images/hero-poster.jpg` as the still shown first.
  GIF alternative: see `assets/video/README.txt`.
- **Pitch deck** → `assets/deck/Delice-Pitch-Deck.pdf` (buttons already point to it).
  To embed slides, uncomment the iframe in the Pitch deck section.
- **Photos** → `assets/images/` (see that folder's README for exact filenames).
- **Gallery** → set each thumbnail's `data-img` and `.ph` background to a photo path.
- **YouTube** → set `data-yt="VIDEO_ID"` on each video card.
- **Specs** → edit the values in the Technical section (they're representative placeholders).
- **Contact** → the CTA uses `mailto:contact@delicerobotics.com`; change to your address.

## Deploy to GitHub Pages (free) + keep your domain
1. Create a public repo and upload these files, keeping the `assets/` folders.
2. **Settings → Pages** → Source "Deploy from a branch" → Branch `main`, folder `/ (root)`.
3. **Custom domain**: enter `delicerobotics.com` (the `CNAME` file is included), then at
   your registrar add four `A` records for the apex domain pointing to
   `185.199.108.153 / .109.153 / .110.153 / .111.153`, and a `CNAME` for `www` →
   `YOURUSERNAME.github.io`. Enable **Enforce HTTPS** once available.
   (Confirm the IPs against GitHub's current docs.)

## Notes
- A static site can't send form submissions itself. The contact CTA uses a mailto link.
  If you want a real form later, a free service like Formspree or Tally drops in with no
  backend.
- Keep heavy media off the repo: short hero clip only, longer videos on YouTube.
