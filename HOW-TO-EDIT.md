# How to edit your portfolio

Everything is in two places:

- `index.html` — all the text and data
- `assets/` — images, icons and your CV

Open `index.html` in any text editor (VS Code is easiest), use Ctrl+F to find what you want, change it, save, and upload again.

## Replace a project thumbnail

Thumbnails live in `assets/work/`. Each project uses one file:

| Project | File |
|---|---|
| CN ChatBot | `cn-chatbot.webp` |
| Fyers IPO & Mutual Funds | `fyers.webp` |
| Nutrabay | `nutrabay.webp` |
| NerdAgent | `nerdagent.webp` |
| EyeScanner | `eyescanner.webp` |
| Nova | `nova.webp` |
| PRTC Telecom | `prtc.webp` |
| Mcvac Environmental | `mcvac.webp` |
| SupplyVue | `supplyvue.webp` |
| Equation Editor | `equation-editor.webp` |
| Codex | `codex.webp` |
| Kwiqtap | `kwiqtap.webp` |
| Pavlov Media | `pavlov.webp` |
| Sneh Herbal | `sneh-herbal.webp` |
| Erdos Engineering | `erdos.webp` |
| Open-Mind | `open-mind.webp` |

To use a real screenshot:

1. Take a screenshot, ideally wide (16:10, for example 1200 × 750 px).
2. Convert it to `.webp` (free at squoosh.app), or keep it as `.png`/`.jpg`.
3. Give it the same name as the old file and replace it in `assets/work/`.
   - If you keep `.png` or `.jpg`, also search `index.html` for `.webp'` in the `thumb(` function and change the extension, or simply convert to `.webp`.

Once you use real screenshots, delete this line in `index.html` so the popup stops calling them illustrations:
`Preview image is an illustration of the product, not a screenshot.`

## Add or change a live link

Search `index.html` for the project name, e.g. `t:'Codex'`. Next to it you'll see `live:''`. Put the URL between the quotes:

```js
t:'Codex',th:'codex',live:'https://example.com',
```

Projects with a link automatically get a green "Live" badge and a "Visit live site" button.

## Add your GitHub

Search for `GITHUB_URL` near the top of the script and set it:

```js
var GITHUB_URL='https://github.com/your-username';
```

GitHub buttons then appear in the hero, the contact list and the footer.

## Add client reviews

Search for `TESTIMONIALS` and add one line per review (copy the client's words exactly):

```js
var TESTIMONIALS=[
  {q:"Harshit delivered the API ahead of schedule.", n:"Jane Smith", r:"CTO, Example Inc"},
];
```

The reviews section appears automatically once there is at least one.

## Other common edits

| What | Search for |
|---|---|
| Projects (text, problem, what you built, stack) | `var P=[` |
| Experience / jobs | `var J=[` |
| Skill areas and bar levels (0–100) | `var A=[` |
| "Ask about me" questions and answers | `var QA=[` |
| Recruiter snapshot facts | `The short version` |
| Hero headline and intro | `Senior Python &amp; AI Engineer` |
| Phone / WhatsApp | `917014744311` |
| Email | `harshit.j7196@gmail.com` |
| Your photo | replace `assets/portrait.jpg` (same name) |
| Your CV | replace `assets/Harshit-Jain-CV.pdf` (same name) |

Tip: inside the `var P=[...]` and similar lists, keep the quotes and commas exactly as they are. If the page goes blank after an edit, a missing quote or comma is almost always the reason.
