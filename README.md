# Sibi S — Portfolio

Personal portfolio of **Sibi S**, Senior Software Engineer (Backend) and AI Engineer based in Chennai, India.

A single-page site built with plain HTML, CSS and JavaScript. There are no frameworks, no build step and no dependencies other than one Google Font.

## About me

Backend engineer with 4+ years of experience building production systems in **Python and FastAPI**: REST APIs, async/event-driven microservices, AI/LLM-powered features and real-time streaming endpoints, running on **AWS** (Lambda, DynamoDB, S3, EC2).

- LinkedIn: <https://www.linkedin.com/in/sibi-sengodan/>
- GitHub: <https://github.com/sibi-sengodan>
- Website: <https://sibisengodan.cloud>
- Email: sibisengodan@gmail.com

## What's on the site

| Section | What it shows |
| --- | --- |
| Hero | Name, typing effect cycling through roles, tagline, resume download and contact buttons |
| About | Photo, short bio and animated stats (years of experience, featured projects, technologies) |
| Experience | Timeline of four roles (Entropik Technologies, Cognizant) that draws itself as you scroll |
| Projects | Three project cards with 3D tilt on hover |
| Skills | Skills grouped by category, plus a scrolling strip of top technologies |
| Education | Master of Computer Applications and B.Sc. in Computer Software Engineering |
| Contact | Email, phone, LinkedIn and GitHub |

## Features

- Dark theme by default, with a light/dark toggle that remembers the visitor's choice
- Live background: dot grid that lights up under the cursor, soft cursor glow, slowly drifting colour orbs and an aurora in the hero
- Scroll effects: fade-up reveals, progress bar, hero parallax, wave dividers between sections
- Responsive layout, from phones to wide desktops
- Accessible: semantic HTML, keyboard navigation, visible focus states, skip link, text contrast of WCAG AA or better
- Respects `prefers-reduced-motion`: every animation turns off for visitors who need it
- Animations use only transform and opacity, to stay smooth on mobile

## Project structure

```
portfolio/
├── index.html      # the whole site: markup, styles and script in one file
├── sibi.jpg        # profile photo
└── README.md
```

## Run locally

No install needed. Either open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Customise

Everything lives in `index.html`, and the code is commented by section.

- **Colours:** edit the theme variables at the top of the stylesheet. The dark and light themes each have their own block.
  - `--accent`, `--accent-rgb` and `--on-accent` set the main colour, its glow colour and the text colour on buttons.
  - `--blob-1` to `--blob-4` set the hero aurora and background orbs.
  - `--bg`, `--surface`, `--line`, `--text` and `--muted` set the base palette.
- **Content:** edit the text directly in each section's markup. To add a job, copy one `<li class="job">` block.
- **Typing roles:** edit the `ROLES` list in the script.
- **Photo:** replace `sibi.jpg`.
- **Resume link:** the Download Resume button points to a Google Drive file. The file must be shared as "Anyone with the link".
- **Certifications:** the block is commented out in the Education section. Uncomment it and fill it in when ready.
- **Domain and social preview:** the site is set up for `https://sibisengodan.cloud/`. The canonical link and Open Graph tags in `<head>` use that address, and the preview image is `sibi.jpg`. Change them if the domain changes.

## Deploy

The site is static, so any static host works.

**GitHub Pages:** push the repo, then go to Settings → Pages, choose the `main` branch and the root folder. The site goes live at `https://<user>.github.io/<repo>`.

**Netlify:** drag the folder onto <https://app.netlify.com/drop>, or connect the repo with no build command and publish directory `.`.

## Tech

HTML5, CSS3 (custom properties, grid, flexbox, masks), vanilla JavaScript (IntersectionObserver, requestAnimationFrame), and the Manrope font from Google Fonts.
