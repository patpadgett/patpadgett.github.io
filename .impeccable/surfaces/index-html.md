---
version: 1
slug: "index-html"
primary_target: "index.html"
related_targets: ["posts","tags","start-here","about","404.html"]
---

# Surface brief: blog.patpadgett.com (front page, post page, tag pages, Start Here, About, 404)

Scope: whole site rebuild, replacement visual world. Visitor mode: Read.
Audience: a general reader who likes a story, mostly on a phone from a social link; recruiters second.
Job: finish one post, click another. Proof/content: 125 voiced posts in /data/pat/websites/blog/drafts-voiced.
Constraints: flat HTML from a Python build; no CDN fonts, comments, newsletter; [PAT:] posts never build;
posts publish only on/after their date; career posts are quieter but the design does not know that.
Chosen by user: IMPECCABLE'S PICK (seed 78442aac), The Photocopied Show Flyer, over the assigned digest.
Memorable moment: the front page is a telephone pole of flyers; each post is a flyer you tear off and the
white text sheet underneath is the story. Unresolved: keep or fold the 2018 post; author photo (none for now).

## Direction contract

THESIS: A punk-voiced engineer's stories deserve the format his scene already used to shout: the
photocopied show flyer, toner-black condensed caps on cheap colored copy paper, taped to a pole. It
refuses the default arrangement (name, bio, chronological list on white with a blue accent) and the
digest arrangement it beat. The list IS a pole of flyers; the post IS a flyer with a white sheet stapled
under it.

OWN-WORLD: Copy-paper grounds: goldenrod #f2c230, astrobright pink #e94f8a, electric blue #2f6fe4, and
a plain white #f4f1ea sheet for body text. Toner black #111 for all display type. Big Shoulders (var,
already self-hosted at music.patpadgett.com) at heavy weight, caps, tight tracking, for headlines; Special
Elite typewriter for the info block (date, no., word count, tags); Permanent Marker for the grease-pencil
marks (Start Here, read); Archivo for 900-word body text at 18px on the white sheet. Materials: halftone
dot pattern on any image (CSS), a torn/rough top edge on every flyer (SVG mask), a masking-tape strip
holding each flyer (CSS pseudo-element, slight rotation), toner speckle texture at low opacity. Each
flyer is rotated 0.5-2 degrees off true; the white sheet under a post is dead straight. No borders,
shadows, gradients or rounded corners anywhere; paper, tape, toner only.

STORY: The visitor lands on a pole plastered with flyers, newest on top, and understands in one second
that this is one loud person's stories. They read the giant headline and the one-line proof under it,
tear it off (click), and get a white sheet with 900 words in a comfortable measure and nothing else
until the end, where the info block, tags, and the next flyer wait. Recruiters find "career" and
"mediation" tags in the info block and a Start Here flyer marked in grease pencil.

FIRST VIEWPORT: Desktop 1440: the newest post's flyer fills the viewport height, rotated -1deg, goldenrod
ground, masking tape at top center; headline in Big Shoulders heavy caps at ~11vw across two to three
lines; below it the proof line in Special Elite; at the bottom the info block (Sep 21 2026 / No. 001 /
818 words / corkscrew, c, open-source). Behind it, the edges of two older flyers (pink, blue) peek out
rotated the other way. The masthead is a small taped label top-left: "PAT PADGETT" in Big Shoulders and
"stories, told loud" in Special Elite; nav (Start Here, Tags, About, RSS) as four tape tabs top-right.
Mobile 390: the same flyer, headline at ~17vw, tape and edges preserved, one flyer per screen.
Primary action: the whole flyer is the link.

FORM: The Photocopied Show Flyer; position 1 on my grounded list (IMPECCABLE'S PICK card), user-chosen
over the roll's assignment (position 3, Hacker Quarterly Digest). Seed key 78442aac. Signature
interaction: tearing a flyer off the pole; on click the flyer lifts, rotates to 0, and the white sheet
slides out from beneath it (view transition / CSS, reduced-motion: instant). Motion grammar: paper only,
short (180-260ms), ease-out, no fades of text.

FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict,
DESIGN.md, and every shipping raster carrying its provenance
