---
name: "blog.patpadgett.com"
description: "The Photocopied Show Flyer: colored paper and toner on a wooden pole."
colors: {"toner": "#111111", "goldenrod": "#f0c419", "pink": "#ff6fa8", "blue": "#4a90d9", "green": "#79c65a", "orange": "#ff8a3d", "sheet": "#f4f1ea", "pole": "#3a2f27", "tape": "rgba(236,222,170,.86)"}
typography: {"display": {"fontFamily": "\"Big Shoulders\",\"Archivo Narrow\",\"Arial Narrow\",sans-serif", "fontSize": "clamp(56px,11vw,170px)", "fontWeight": 900, "lineHeight": 0.88, "letterSpacing": "-.025em"}, "headline": {"fontFamily": "\"Big Shoulders\",\"Archivo Narrow\",\"Arial Narrow\",sans-serif", "fontSize": "clamp(46px,8.4vw,132px)", "fontWeight": 900, "lineHeight": 0.88, "letterSpacing": "-.025em"}, "body": {"fontFamily": "\"Archivo\",system-ui,sans-serif", "fontSize": "clamp(18px,1.25vw,20px)", "fontWeight": 400, "lineHeight": 1.6, "letterSpacing": "normal"}, "label": {"fontFamily": "\"Special Elite\",\"Courier New\",monospace", "fontSize": "15px", "fontWeight": 400, "lineHeight": 1.55, "letterSpacing": "normal"}, "proof": {"fontFamily": "\"Special Elite\",\"Courier New\",monospace", "fontSize": "clamp(17px,1.6vw,22px)", "fontWeight": 400, "lineHeight": 1.4, "letterSpacing": "normal"}, "nav": {"fontFamily": "\"Big Shoulders\",\"Archivo Narrow\",\"Arial Narrow\",sans-serif", "fontSize": "19px", "fontWeight": 800, "lineHeight": 1.55, "letterSpacing": ".01em"}, "marker": {"fontFamily": "\"Permanent Marker\",\"Comic Sans MS\",cursive", "fontSize": "clamp(20px,2.2vw,30px)", "fontWeight": 400, "lineHeight": 1.55, "letterSpacing": "normal"}, "title": {"fontFamily": "\"Big Shoulders\",\"Archivo Narrow\",\"Arial Narrow\",sans-serif", "fontSize": "2rem", "fontWeight": 800, "lineHeight": 1, "letterSpacing": "-.01em"}}
spacing: {"column-gutter": "clamp(12px,3vw,48px)", "pole-gap": "56px", "compact-gap": "36px", "next-gap": "40px", "theme-gap": "48px", "tab-gap": "10px"}
components: {"flyer": {"backgroundColor": "{colors.goldenrod}", "textColor": "{colors.toner}", "typography": "{typography.headline}", "padding": "clamp(28px,5vw,64px) clamp(20px,4vw,56px) clamp(24px,3vw,40px)"}, "nav-tab": {"backgroundColor": "{colors.tape}", "textColor": "{colors.toner}", "typography": "{typography.nav}", "padding": "9px 16px"}, "nav-tab-hover": {"backgroundColor": "{colors.toner}", "textColor": "{colors.sheet}"}, "tag-tab": {"backgroundColor": "{colors.tape}", "textColor": "{colors.toner}", "padding": "8px 14px"}, "sheetpaper": {"backgroundColor": "{colors.sheet}", "textColor": "{colors.toner}", "typography": "{typography.body}", "padding": "clamp(40px,6vw,88px) clamp(20px,5vw,72px) clamp(48px,6vw,88px)"}, "theme": {"backgroundColor": "{colors.sheet}", "textColor": "{colors.toner}", "padding": "clamp(28px,4vw,56px)"}}
---

# Design System: blog.patpadgett.com

## Overview

**Creative North Star: "The Photocopied Show Flyer"**

The Photocopied Show Flyer puts heavy condensed headlines on colored copy paper against a wooden telephone pole. Tape, torn edges, toner damage and offset sheets supply the material vocabulary; there are no paper shadows, borders, gradients or rounded corners.

Long-form writing sits on a straight, untextured off-white sheet. The display treatment stops at the story: Archivo carries the paragraphs, while typewriter metadata and marker annotations have separate roles.

**Key Characteristics:**
- Colored copy paper with toner-black text.
- Torn masks and translucent tape, not card chrome.
- Condensed uppercase display type; straight, quiet reading sheets.
- Short paper movement with plain-link fallback.

This is a source-grounded record, not a redesign proposal. Authority: `/data/pat/websites/blog/build/assets/flyer.css`, `tear.js`, and `build.py`; checked against the local index and Andrew W.K. post. The direction contract supplies the already-chosen metaphor, not replacement CSS values. The inspected build includes future dates and visible preview placeholders; it is not evidence of production publication eligibility.

## Colors

Flat colored copy paper carries dark type. CSS custom-property names are preserved in the frontmatter.

### Primary
- `--goldenrod`: #f0c419. Default flyer ground, outer focus outline, selection text, article-link and footer-link hover ground.
### Secondary
- `--pink`: #ff6fa8. Flyer variant, rear lead sheet, article-link underline and preview-placeholder ground.
- `--blue`: #4a90d9. Flyer variant and rear lead sheet.
### Tertiary
- `--green`: #79c65a. Flyer variant and fourth theme-list strip.
- `--orange`: #ff8a3d. Flyer variant and Start Here page heading.
### Neutral
- `--toner`: #111111. Text on paper, inverted interactive grounds, selection ground and preformatted-code ground.
- `--sheet`: #f4f1ea. Reading sheet, brand label, intro, theme groups and optional flyer ground; text on the pole and inverted controls.
- `--pole`: #3a2f27. Body ground beneath procedural wood and staple marks.
- `--tape`: rgba(236,222,170,.86). Translucent tape strips and navigation/tag/pager tabs.

Non-token material colors: inline code uses rgba(0,0,0,.06); staple strokes are #9a9a96 at .42 opacity, a paper remnant is #d8d0bd at .28, and the wood crack is #120d09 at .75. These are material details, not new paper variants. Sidecar tonal ramps are generated preview metadata, not shipped palette steps.

## Typography

Four self-hosted faces use `font-display:swap`. Big Shoulders and normal Archivo expose weights 100–900. Archivo italic is a separate 400 face; Special Elite and Permanent Marker are 400. All font URLs live under `/assets/fonts/`; Big Shoulders is preloaded.

- `--display`: "Big Shoulders","Archivo Narrow","Arial Narrow",sans-serif.
- `--type`: "Special Elite","Courier New",monospace.
- `--marker`: "Permanent Marker","Comic Sans MS",cursive.
- `--body`: "Archivo",system-ui,sans-serif.

The scale is component-specific, not a modular ratio. Unless overridden, text inherits body line-height 1.55 and normal tracking; normal text weight is 400. Bold article text uses browser bold styling; it is not a separate declared token.

| Role | Size | Weight / line-height / tracking |
| --- | --- | --- |
| Body base | 18px | Archivo 400 / 1.55 / normal |
| Article | clamp(18px,1.25vw,20px) | Archivo 400 / 1.6 / normal |
| Flyer h1/h2 | clamp(46px,8.4vw,132px) | Big Shoulders 900 / .88 / -.025em |
| Lead h1/h2 | clamp(56px,11vw,170px) | Same as flyer |
| Next flyer h2 | clamp(34px,4.2vw,64px) | Same as flyer |
| Compact flyer h2 | clamp(34px,5.4vw,84px) | Same as flyer |
| Brand strong | 30px | Big Shoulders 900 / 1 / -.01em |
| Brand subtitle | 13px | Special Elite 400 / 1.55 / normal |
| Intro | clamp(16px,1.4vw,19px) | Special Elite 400 / 1.55 / normal |
| Proof | clamp(17px,1.6vw,22px) | Special Elite 400 / 1.4 / normal |
| Info and kick | 15px | Special Elite 400 / 1.55 / normal |
| Nav and pager links | 19px | Big Shoulders 800 / 1.55 / .01em |
| Tag tabs | 16px; tag directory 18px | Special Elite 400 / 1.55 / .01em inherited from tab rule |
| Marker | clamp(20px,2.2vw,30px) | Permanent Marker 400 / 1.55 / normal |
| Tail and footer | 16px | Special Elite 400 / 1.55 / normal |
| Tail byline | 22px | Permanent Marker 400 / 1.55 / normal |
| Article h2 | 2rem | Big Shoulders 800 / 1 / -.01em |
| Article h3 | 1.4rem | Big Shoulders 700 / inherited 1.6 / normal |
| Theme h2 | clamp(40px,5vw,72px) | Big Shoulders 900 / .9 / -.02em |
| Theme item title | clamp(22px,2.4vw,32px) | Big Shoulders 800 / 1 / normal |
| Theme item subtitle | 15px | Special Elite 400 / 1.55 / normal |

Flyer headings balance text, wrap anywhere, and offset left -.035em. Flyer, brand, nav, article h2 and theme headings are uppercase; article h3 is not forced uppercase. Tags are lowercase. Article code is Special Elite at .95em, pre at .9em with line-height 1.5; blockquotes use Special Elite. Article links retain toner text, a 3px pink underline and 3px underline offset, including visited state.

## Layout

The main pole, post head, next section, page head, tag directory, themes, pager and footer use a centered 1180px maximum column. Shared horizontal padding is clamp(12px,3vw,48px). The sheet wrapper is narrower at 1080px; article and tail each cap at 68ch. No component forces a viewport-height flyer.

- Mast: flex, space-between, start alignment, 16px gap; padding 28px clamp(16px,4vw,56px) 0; z-index 5.
- Pole: grid, 56px gap, padding 40px shared-gutter 100px; compact gap 36px. Intro max 56ch, margin 0 0 8px 2%, padding 14px 20px.
- Flyer: padding clamp(28px,5vw,64px) clamp(20px,4vw,56px) clamp(24px,3vw,40px). Compact uses clamp(20px,3vw,36px) clamp(18px,3vw,44px) clamp(18px,2vw,28px).
- Post head: 40px top padding, no bottom padding, -.8deg rotation. Sheet wrapper: 28px top margin, 60px bottom padding, z-index 2. Sheet padding: clamp(40px,6vw,88px) clamp(20px,5vw,72px) clamp(48px,6vw,88px).
- Article paragraphs: bottom 1.25em; h2 margin 2.4em 0 .7em, h3 2em 0 .5em; lists left padding 1.4em and bottom margin 1.25em; li margin .3em 0. Blockquote margin 1.5em 0 1.5em 1.5em. Pre margin 1.5em -12px, padding 20px 24px, horizontal scrolling.
- Next: grid gap 40px; repeat(auto-fit,minmax(min(100%,420px),1fr)); 100px bottom padding. Page head rotates .8deg. Tag directory padding 36px shared-gutter 120px.
- Themes: grid gap 48px, padding 40px shared-gutter 120px. Theme padding clamp(28px,4vw,56px); list grid gap 14px.
- Pager: margin -40px auto 0, 16px flex gap, space-between, 100px bottom padding. Footer: 80px bottom padding; link row gap 12px 20px; paragraph max 70ch and top margin 18px.

Rotation and offset custom properties are intentional. `--rot` defaults to -1deg on cast and -.7deg on theme; generated flyer choices are -1.2, 1.1, -.6, 1.8, .4 and -1.6deg. `--ml` / `--mr` default to 0; generator left choices are 0,0,5,0,3,0% and right choices 0,4,0,9,0,2%, indexed separately. The inspected index consequently repeats -1.6deg; do not claim random per-card rotations. `--r` defaults to 0deg for nav/tabs/pager and -.5deg for theme links. `--ground` selects flyer or theme-strip paper color. `--tx`, `--tw`, `--tr` control tape position, width and angle: defaults 50%,120px,-3deg; generated x choices 50,38,62,45,57%, angles -3,4,-6,2,5deg. Post-header tape is 44% / 3deg; sheet tape is 150px / 2deg.

### At max-width:720px

Article body becomes 19px. Mast top padding becomes 18px, direction column, alignment start; nav justifies start. Brand strong becomes 24px. Pole gap becomes 40px, but the more-specific `.pole.compact` remains 36px. Cast margins are zeroed with important custom-property overrides. Ordinary flyer h1/h2 becomes clamp(44px,15.5vw,84px); lead becomes clamp(56px,17.5vw,96px). More-specific next and compact h2 rules retain their own clamps. Mark moves from absolute positioning to static inline-block with 12px bottom margin. Lead back-sheet insets become -2% 2% 6% 4% and 5% 4% -3% 1%. Pre margins become 1.5em -8px. Existing rotations and tape remain.

## Elevation & Depth

Paper has no shadows. Depth comes from overlap, flat paper colors, tape translucency and rotation. `.paper` isolates stacking; its grain pseudo-element is z-index 0 and its children z-index 1. Tape is z-index 3. Lead back sheets use z-index -1. The body clips horizontal overflow (its final declaration is overflow-x:hidden); html uses overflow-x:clip.

The deliberate exception is the wooden pole: a fixed `body::before`, inset 0, z-index -1, pointer-events none, uses `linear-gradient(90deg,rgba(0,0,0,.78),rgba(0,0,0,.25) 18%,rgba(0,0,0,0) 46%,rgba(0,0,0,.2) 76%,rgba(0,0,0,.8))`. This is cylinder shading. Faint staple scars and a remnant are the pole's history, not decoration on paper. The scars repeat in a 700px by 900px SVG; wood repeats at 300px by 900px, using fractal noise frequency .35 .003, four octaves, seed 11, a brown color matrix and one vertical crack.

## Shapes

Paper has no decorative borders, radii, gradients or shadows. Focus outlines and text underlines are accessibility affordances, not paper borders. The article separator removes its border and prints `* * *` instead.

All root material custom properties are in use:
- `--torn-a`: SVG 100×100, rect 1,1 at 98×98; fractal noise .09 .04, 3 octaves, seed 2, displacement 2.6.
- `--torn-b`: same geometry; noise .06 .11, 3 octaves, seed 9, displacement 3.1.
- `--torn-c`: same geometry; noise .12 .05, 2 octaves, seed 17, displacement 2.2.
- `--grain`: 160×160 SVG, stitched fractal noise .9, 2 octaves; color matrix makes black alpha `.55 -.2`. Paper and intro apply it with multiply blending and opacity .5; the article sheet does not.

Torn masks fit center/100% 100% no-repeat, including WebKit declarations; they affect all edges, not only the top. Tape is 28px high at top -13px, translated -50% on x and rotated by `--tr`, masked with torn-c. Tape on a masked paper element can be clipped by that same mask.

The expensive toner filter is limited to `.lead .toner,h1.toner`: noise .02 .06 / 2 octaves / seed 7 drives displacement 2.4 on R/G channels; blotch noise .012 .02 / 3 / seed 5 multiplies fine noise 1.1 / 2 / seed 3, then an alpha matrix and composite remove ink. Ordinary non-lead h2 elements carry the class without running this filter. Article images use grayscale(1) contrast(1.2), not a halftone-dot implementation.

## Components

### Masthead and nav tabs

Brand is an off-white label, padding 10px 16px 8px, rotation -1.5deg, tape width 70px / angle 4deg. Subtitle top margin is 2px. Nav wraps with 10px gaps and right alignment. Five actual links read all stories, start here, tags, about, rss; only the first four have explicit rotations 2,-1.5,1,-2.5deg, the fifth inherits 0deg. Links have padding 9px 16px and minimum 44px height and width. Hover or `[aria-current]` inverts toner/sheet. The post mast is quiet: no nav until the tail.

### Flyer / cast anchor, info, mark and lead-wrap

The whole cast is a real block link, outside the masked paper. It lifts to rotate(0deg) translateY(-4px) on hover or focus-visible, transitioning transform over .22s cubic-bezier(.2,.8,.2,1). Flyer variants cycle goldenrod, pink, blue, green, orange, sheet. Proof sits 22px below the heading, max 60ch. Info starts at clamp(24px,3vw,44px), wraps as flex with gap 6px 0, and separates entries with `/`, padding 0 .8em, opacity .6. Dates are uppercase but weight 400. Actual entries are date, number, words, minutes; tags are in the tail, not inside the whole-card link.

Mark uses -8deg rotation, z-index 2, right clamp(12px,3vw,40px), top clamp(14px,3vw,36px). Lead-wrap adds pink torn-b at inset -3% -2% 6% 4%, rotation 2.6deg, and blue torn-c at 5% 3% -4% -3%, rotation -3.2deg.

### Sheetpaper, tail and tabs

Sheetpaper is straight, off-white, torn-c and taped; it lacks `.paper` and therefore lacks grain. Tail begins 64px below the article and resets info top margin to 0. Tabs wrap with 10px gap and top margin 14px; padding 8px 14px, minimum 44px in both dimensions. Odd tabs rotate -1.5deg, even 1.2deg. Ineligible tags are spans at opacity .7, padding 8px 4px, minimum height 44px, not fake links. Byline margin-top 28px, rotation -2deg; tail nav also starts 28px below and aligns left.

### Next and pager

Next presents newer then older flyers with a 15px Special Elite kick at margin-top 18px. Pager links reuse nav styling; first rotates -1.5deg, last 1.2deg (a sole link matches both, so the last rule wins). Page count is 16px Special Elite on the pole, vertically centered.

### Theme

Theme is a taped torn off-white group at -.7deg; even groups rotate .9deg. Optional paragraph margin is 12px 0 22px, max 60ch; generated Start Here groups currently contain heading and list. List strips have padding 14px 16px, no list markers, and default goldenrod / -.5deg. Multiples of 2 use pink / .6deg, 3 blue / -.9deg, 4 green / .4deg, with later rules winning overlaps. Subtitles start 6px below titles. There is no special theme-link hover state in the source, only the global focus outline.

### Footer

A wrapping row of sister-site and RSS links sits directly on the pole. Links use sheet text, minimum 44px height and width, padding 0 6px; hover uses goldenrod and toner. The writing credit follows after 18px. No footer card is introduced.

### Motion and accessibility floor

Cross-document view transitions opt in with `navigation:auto`. Root snapshots have no animation; the flyer group lasts .26s with cubic-bezier(.2,.8,.2,1). Old flyer animation is none and opacity 0; new flyer animation is none. Post-header paper and `.cast.tearing .flyer` share `view-transition-name:flyer`. `tear.js` intercepts cast clicks only when startViewTransition exists and reduced motion is not requested; it excludes meta/control/non-primary-button clicks, adds tearing, starts an empty transition, then navigates on ready. There is no implemented white-sheet slide-out or text fade. Without support or JS, ordinary href navigation remains.

Reduced motion removes element transitions and animations with important rules, changes smooth scrolling to auto, and disables cross-document navigation transitions; JS exits early. Hover/focus transform still applies instantly, not animated.

Global focus-visible is a 4px solid goldenrod outline at 4px offset. Focus inside paper or sheetpaper switches outline color to toner. Nav, tab, pager and footer link minima are 44px; this is not a claim that inline prose links meet a 44px box. Article measure is 68ch, line-height 1.6 and mobile body 19px. Maintain contrast and keyboard usability; source inspection alone is not an audited WCAG conformance result.

## Do's and Don'ts

### Do
- Do edit /data/pat/websites/blog/build/assets/flyer.css and rebuild; assets/flyer.css under this project is generated.
- Do keep article text at 68ch maximum, line-height 1.6, and 19px at widths up to 720px.
- Do keep the focusable cast outside the torn mask and retain visible focus outlines.
- Do retain real links, semantic headings, English document language, labeled navigation and image alt text.
- Do gate publication by date and unresolved [PAT:] markers; use preview overrides only for review.

### Don't
- Don't add gradients, shadows, borders or radii to paper; the pole lighting is the deliberate exception to the gradient ban.
- Don't put grain or toner filters over article prose.
- Don't describe the contract's older palette, halftone dots or sliding body-sheet animation as implemented.
- Don't add CDN fonts, comments, newsletter prompts or enabled analytics without authorization.

### Build rules that shape the design

`build.py` generates flat HTML from Markdown/YAML. Default production selection excludes posts containing `[PAT:` and dates after `--date` (default today in America/New_York); exclusion is reported rather than aborting the whole build. `--allow-placeholders` and `--include-future` are review overrides, not publication defaults. Preview placeholders use pink marker styling. The inspected Andrew W.K. page contains these marks and the index contains future-dated posts; do not deploy that snapshot as proof that the gates passed.

`MIN_TAG = 3`: only tags attached to at least three selected posts earn pages and links; smaller tags stay text spans. `PER_PAGE = 24`: the pole paginates, newest first, instead of expanding forever. Only the first flyer on the first index page gets lead-wrap and lead size. Start Here lists include only selected posts. Flyer rotation, mask, margin, tape and color choices are deterministic; preserve the generator's selection rules rather than hand-editing generated HTML. Analytics IDs are empty by default. No comments or newsletter UI is generated.


## Polish pass (2026-09-21) — flow, alignment, props, motion
- One gutter token `--g` for masthead, hero, columns, pager, list pages and footer; headline/dek/kicker share a left edge (italic overhang compensated).
- Kicker `date · No. · read time` wraps as units, separator at line end. Masthead price strip on its own line, pluralises.
- Thin-newsstand state (index, <6 cards): the main column carries a taped "Next issue" card with an undeveloped-photo square, a two-column "Coming attractions" classifieds list of the next eight dated posts, and a Clip & Save RSS coupon; a red double-rule PREMIERE ISSUE stamp sits on the next-issue card while fewer than three posts exist. All of it disappears as the stand fills.
- Start Here hides empty theme lists and says how many are "still at the printer"; blurbs no longer fall into the numeral column.
- About: floated "File photo" Polaroid of Pat; tail rule matches the 62ch measure.
- Footer: two columns — checkout links + colophon left, PRINTED ON FLAT HTML sticker and 99¢ right.
- Motion: the starburst slaps on once (`slap`), the stamp lands (`stampin`), nav tabs settle flat on hover, cards lift on title hover, and below-fold boxes land on the stand as they scroll in (`.pre → .in`, IntersectionObserver, only elements below the first viewport, 4s safety). Reduced motion disables all of it.
- Drop cap is an upright reversed-out Nunito letter; inline code hugs punctuation.
