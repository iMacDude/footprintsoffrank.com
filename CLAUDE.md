# CLAUDE.md — Footprints of Frank
## Permanent Project Memory — Read This First, Every Session

---

## 1. WHAT THIS IS

**footprintsoffrank.com** is the calling card and blog home of Frank — a 30-inch stuffed zebra
who has been making people smile since April 13, 2022. The site is owned and narrated by John Belen
(GitHub: iMacDude). It is hosted on GitHub Pages, built with Jekyll, and designed to be
low-maintenance, privacy-first, and genuinely fun.

This is not a brand exercise. It is an archive of a real joy that compounded over four years —
road trips, charity galas, hotel bars, airport lounges, a growing cast of characters, and
the strangers who kept saying "you should make a page for him." Frank now has a page.

**The guiding creative principle:** Pixar in real life. Family-friendly with a knowing wink
for adults. The bourbon jokes are seasoning, not the meal. Fun first. Always.

---

## 2. TECHNICAL STACK

| Layer | Tool |
|---|---|
| Hosting | GitHub Pages (free, CDN, auto SSL) |
| Build | Jekyll (native GitHub Pages support) |
| Domain | footprintsoffrank.com (registered at GoDaddy, DNS managed there) |
| Email | frank@footprintsoffrank.com via Zoho Mail |
| Repo | github.com/iMacDude/footprintsoffrank.com |
| Primary workstation | Mac Studio |
| Mobile editing | iPhone / iPad |

**Jekyll conventions used in this repo:**
- `index.html` — calling card landing page, at repo root, NOT processed as Jekyll (no front matter)
- `_layouts/default.html` — master frame (header, rail, footer, zebra texture)
- `_layouts/post.html` — blog post template, inherits default
- `_posts/` — all blog posts as Markdown, named `YYYY-MM-DD-slug.md`
- `assets/images/` — all site images
- `assets/images/posts/YYYY-MM-DD-slug/` — per-post image folders
- `_config.yml` — site settings, social links, author info

**How to reference images in a post:**
```markdown
![Alt text]({{ site.baseurl }}/assets/images/posts/YYYY-MM-DD-slug/filename.jpg)
*Caption in italics beneath.*
```

---

## 3. DESIGN SYSTEM — NEVER DEVIATE FROM THESE

These tokens were established through deliberate decisions, not defaults.
Do not change them without explicit instruction from John.

```css
/* Core palette */
--bg:       #1a1a1c;   /* dark warm grey body */
--bg-deep:  #0a0a0b;   /* footer / deeper sections */
--bg-hdr:   #050506;   /* black header */
--fg:       #f0ede5;   /* primary text — warm white */
--fg2:      #bab6ad;   /* secondary text */
--fg3:      #7c7870;   /* muted text, captions */
--paper:    #d4cfc1;   /* warm paper — section subheads, hero body */
--red:      #A82423;   /* THE red — sampled from Kelley's nail polish, April 13 2022 */
--red-dk:   #6b1716;   /* rail gradient shadow */
--edge:     #2a2a2c;   /* borders */
```

**The red (#A82423) has a story.** It was pixel-sampled from Kelley's nail polish in the
unboxing selfie taken April 13, 2022 at 4:48 PM. It is not "a red." It is *that* red.
Do not substitute a generic red.

**Typography:**
- `Bebas Neue` — site title, section labels, large display type (all-caps, cinematic)
- `Fraunces` — subheads, pull quotes, italic flourishes (optical serif, literary)
- `Lora` — body prose (readable serif, warm)
- All loaded from Google Fonts

**Structural elements — present on every page:**
1. **Red rail** — 7px fixed left edge, full viewport height, `#A82423` with gradient shadows,
   draws down on page load via CSS animation (`rail-draw` keyframe)
2. **Black header** — `#050506` background, `BEBAS NEUE` site title in `--fg`,
   italic Fraunces tagline in `--fg2`
3. **Zebra-stripe border** — 6px repeating CSS stripe pattern immediately below header
   and immediately above footer. Alternating `--fg` and `--bg-hdr` segments of irregular widths
4. **Organic zebra texture** — inline fixed SVG background, 15 diagonal bands warped by
   `feTurbulence` displacement filter, `opacity="0.10"`. NOT linear gradients.
   The stripes must feel like a hide, not a barcode
5. **Grain overlay** — `body::before` with SVG fractalNoise, `opacity:0.5`, `mix-blend-mode:overlay`
6. **Footer** — `#0a0a0b`, zebra-stripe top border, Independence Academy acknowledgment,
   Frank's birthday, copyright

**Current header tagline:**
> Frank the Happy Zebra makes people's day as he travels and makes new friends

---

## 4. FRANK'S STORY BIBLE

### The Origin — April 13, 2022

John was at the Renaissance Indianapolis North bar in Carmel, Indiana, during a charity event
for The Independence Academy (a school for autistic learners). A large stuffed zebra was in
the silent auction. John made an offhand comment. His friends challenged it. He bought a $50
event ticket, got a bidding number, and spent the evening bidding from his phone at the bar.

He lost. Outbid at $550 by an anonymous stranger. His friends were delighted.

John promised: *"In two weeks I'll be back at this bar. And there will be a zebra sitting next to me."*

He drove home to Cary, North Carolina. Executed a stuffed zebra procurement operation.
Two weeks later, a large box arrived at Kelley's house. She opened it, took a selfie with Frank
(4:48 PM — EXIF verified), and her son Zac walked in, took one look, held up one hand,
said "I don't want to know," and went upstairs. She drove to the Renaissance without Frank.
John retrieved Frank from her car himself and walked him into the bar.

**Frank had no name yet.** Friends were texted. Locals were consulted. John's daughter
**Jessica** suggested Frank — a nod to "Frank the Fruit Striped Zebra" from Juicy Fruit gum.
Frank was neither fruity nor chewy, but it was a cool name. It was also, coincidentally,
**John's father's name** — an irony that would become more significant about a year later.
That story has not yet been written. When it is, it belongs in the "John sincere" voice.

**Frank's verified birthday: April 13, 2022.**
Both origin photos were taken that day: Kelley's unboxing selfie at 4:48 PM,
the bar meeting photo at 6:28 PM. 99 minutes apart.

### The Road Years

Post-COVID, John was doing extensive driving — Michigan, Florida, North Carolina, Atlanta.
Frank rode shotgun in the passenger seat of his truck. Strangers kept encouraging a social
media presence. Frank's Instagram (@footprintsoffrank) launched July 9, 2022.

**The archive: 196 Instagram posts, July 2022 – April 2026.**
- 124 posts have GPS coordinates
- Frank's range: Caribbean coast to the Netherlands
- Roughly 119 US posts, 5 European posts
- Average caption length: ~130 characters (expanding to long-form blog is the whole point)

### Key events in the canon (to be expanded as blog posts)

- **The Franknapping** (summer 2022) — Frank Jr. was "abducted" at a family reunion.
  A ransom note appeared. John's brother, retired police Captain L. Belen, was consulted.
  Many fingerprints were found on the note, including his own. No suspects identified.
  *Storyteller voice.*

- **iWIN Gala** (date TBD from archive) — Frank Jr. attended an Indiana Women in Need
  charity gala in a salmon vest, white dress shirt, and red sequined bow tie.
  Full red-carpet moment. *Storyteller voice.*

- **The Safari** — John rode a real zebra in Africa (photo exists: you on zebra's back,
  Serengeti sky, blue jeans). Frank's origin species, met in person.
  *Cosmic/cathartic register. John sincere + Storyteller hybrid.*

- **Micro-Frank at the Little Hellion** — finger puppet perched on a beer bottle.
  Dual-track joke: adults read the bottle name, kids see the tiny zebra.
  Neither audience needs an explanation. *Frank voice.*

- **Pico-Frank at the Ritz** — tiny ceramic zebra in a gift box on a white napkin
  with a backward "R" (Ritz-Carlton branding). "You have been Franked."
  *Storyteller voice, very short, very dry.*

- **Frank Jr. goes to the Netherlands / Dublin** — passport stamps, John's Bar Dublin,
  Guinness tour, Margraten. *Frank Jr. first-person voice.*

- **Frank's father** — the story of John's dad, Francis "Frank" Belen Sr., and the irony of the name.
  Has not been written yet. Handle with care. *John sincere voice.*

---

## 5. THE FRANK CINEMATIC UNIVERSE (FCU CAST)

| Character | Description | First appearance | Voice |
|---|---|---|---|
| **Frank** | The original. 30 inches. Black and white. Rides shotgun. | April 13, 2022 | First person, exclamation-rich |
| **Frank Jr.** | World traveler. Passport stamps on 2 continents. Tuxedo owner. | July 9, 2022 (Denver pub) | First person, slightly more worldly |
| **Micro-Frank** | Finger puppet. Impossibly small. Two-continent impact. | December 2022 | First person, big energy in small package |
| **Pico-Frank** | Tiny ceramic figurine. Has been to the Netherlands, the Ritz. | May 2025 | Third person only. The universe speaks for him. |
| **Aqua-Frank** | Colorful inflatable pool floatie. Broke the black-and-white rule. | April 2024 | Third person. Weather-watcher. Unbothered. |
| **Beach crew** | Unnamed gnome, duck, baby, mini horse, smiling rubber zebra. | TBD | Collectively "& more." Names pending. |

**The casting director has never officially closed.**

FCU data file lives at `_data/franks.yml` (to be created during Jekyll build session).
Blog posts can tag which Frank(s) star in them.

### Frank's Hashtag Canon (from Instagram archive)
These are real, established tags — use them consistently:
- `#franksfriends` (54 uses — most popular)
- `#frankjrtravels` (34) / `#franktravels` (34)
- `#zebralove` (27) / `#zebralicious` (14)
- `#franksessories` (13) — Frank's wardrobe/accessories
- `#youhavebeenfranked` (4) — Pico-Frank's signature move
- `#microfrank` (4) / `#kidsrule` (4)
- `#frankloveskids` (3)
- `#milehighfrank` (2) / `#flyingfrank` (2) / `#admiralsclub` (2)

---

## 6. THE THREE NARRATOR VOICES

**Voice 1 — Frank speaking (most blog posts)**
First person. Exclamation points welcome. Frank addresses the reader as "you."
He breaks the fourth wall constantly. Big energy. Kid-friendly. Calls John "Dad."
*"I got to fly on a plane with Dad, today! I sat in first class!
You would not believe the snack situation up there."*

**Voice 2 — The Storyteller (set-piece adventures)**
Mock-formal third person. Dry wit. Perfect for detective-noir situations
(the Franknapping), gala appearances, diplomatic incidents.
*"Tragedy was NARROWLY averted today at the family reunion.
Former Detective, Captain L. Belen was consulted, though after discovering
many prints on the note, including his own, no concrete suspects were identified."*

**Voice 3 — John, plain (milestone moments)**
No character, no bit. Direct, warm, sincere. Used sparingly — for charity moments,
milestones, loss, gratitude. When John speaks plainly, it lands because he doesn't do it often.
*"Anyone who wonders why we do what we do need only look into the eyes of a child."*

**Calibrating adult humor:**
The Pixar test. The joke must work at the literal level for a kid AND at a second layer
for the adult. The second layer is NEVER explained. If it requires a wink emoji, it failed.
*Good: "Frank prefers his road trips like his cocktails — old-fashioned."*
*Bad: "Frank's having an Old Fashioned 🍸😏 don't tell mom!"*

---

## 7. FRANK'S POSTING RULES

```
1. PG. The Independence Academy is the lodestar.
2. Other people's kids: photos only with consent, no names.
3. The bourbon jokes are seasoning. The road is the meal.
4. Frank speaks first person. The Storyteller speaks third. John speaks plain.
   Pick the voice the moment is asking for.
5. Fun first. Always.
```

---

## 8. THE INDEPENDENCE ACADEMY COMMITMENT

Frank started with a silent auction at The Independence Academy (iaindiana.org) —
a school for autistic learners in Carmel, Indiana. This is mentioned:
- In the origin story on index.html
- In the footer on every page
- Will be mentioned naturally in the origin blog post

Running joke / real commitment: if footprintsoffrank ever generates revenue from
social media or merchandise, half goes to The Independence Academy.
When that day comes, there will be a "Frank Gives Back" page.
Until then: the footer line carries it. No fundraising appeals. Just quiet acknowledgment.

---

## 9. SOCIAL MEDIA

- **Instagram:** instagram.com/footprintsoffrank (196 posts, July 2022–present)
- **Facebook:** facebook.com/footprintsoffrank
- Both linked in site footer and hero CTA buttons
- Design system to be applied to FB banner + IG profile/highlights (future session)
- Instagram archive exported and parsed — frank_posts.json contains full caption history
  with GPS coordinates. This is the source material for blog post expansion.

**Blog post workflow:**
1. John picks an Instagram post from the archive
2. Finds or uploads the original photo(s)
3. Claude Code expands the caption into a full blog post using the appropriate narrator voice
4. Photo goes in `assets/images/posts/YYYY-MM-DD-slug/`
5. Post goes in `_posts/YYYY-MM-DD-slug.md`
6. Push to GitHub → auto-deploys via GitHub Pages Jekyll build

---

## 10. KEY PEOPLE IN THE STORY

| Person | Role | Notes |
|---|---|---|
| **John** | Frank's owner, narrator, road companion | Lives in Cape Coral, FL. Mac Studio. Apple loyalist. |
| **Kelley** | John's partner. Frank's reluctant first handler. | Refused to carry Frank into the bar. Her nail polish is #A82423. |
| **Jessica** | John's daughter. Named Frank. | Juicy Fruit connection. "Frank the Fruit Striped Zebra." |
| **Zac** | Kelley's son, 22 at the time. | Walked in, saw Frank, said "I don't want to know," went upstairs. Pull quote. |
| **Francis "Frank" Belen Sr.** | John's father. Frank the zebra's namesake. | The zebra's name was suggested by Jessica as a Juicy Fruit cartoon nod, but it landed on the same name as John's dad. The name Frank carries more weight than anyone knew at first. Handle this story with care — *John sincere voice.* |
| **Captain L. Belen** | John's brother. Retired police captain. | Consulted during the Franknapping. Many fingerprints on the ransom note, including his own. No suspects identified. *Storyteller voice.* |

---

## 11. CURRENT STATUS & NEXT STEPS

*(Update this section at the end of every Claude Code session)*

**Completed:**
- [x] Domain registered (GoDaddy), DNS configured
- [x] Zoho email (frank@footprintsoffrank.com) working with Apple Mail
- [x] GitHub repo created (iMacDude/footprintsoffrank.com)
- [x] Calling card index.html built and live
- [x] GitHub Pages enabled with custom domain
- [x] HTTPS enforced
- [x] footprintsoffrank.com is LIVE as of May 4, 2026
- [x] Design system locked (colors, fonts, texture, red rail)
- [x] All cast thumbnails cropped and uploaded
- [x] CLAUDE.md created

**Next session — Jekyll setup:**
- [ ] Install Jekyll locally (check Ruby version first: `ruby -v`)
- [ ] Scaffold `_config.yml`, `_layouts/`, `_posts/`, `assets/`
- [ ] Build `default.html` layout inheriting the existing design system
- [ ] Build `post.html` layout for blog posts
- [ ] Create `_data/franks.yml` FCU character data file
- [ ] Write first blog post: "The Franknapping" (summer 2022, Storyteller voice)
- [ ] Add blog post index to homepage (2-3 most recent posts)
- [ ] Push and verify GitHub Pages Jekyll build succeeds

**After Jekyll:**
- [ ] Apply design system to Facebook banner + Instagram profile/highlights
- [ ] Add DMARC record (monitoring mode: p=none)
- [ ] Set up Cloudflare Access MFA for photos.thebelens.com (separate project)
- [ ] Photo scanning pipeline when Epson FastFoto FF-680W is ready

---

## 12. WHAT CLAUDE CODE SHOULD NEVER DO

- Change #A82423 to any other red
- Replace the organic SVG zebra texture with linear gradients
- Use WordPress, PHP, or any server-side language
- Add tracking pixels, analytics, or ad networks
- Use Google services of any kind (privacy principle)
- Publish content with other people's children by name
- Break the existing index.html or rename/move the image files it references
- Write Frank's voice as "wacky mascot." Frank is dignified. He has places to be.
