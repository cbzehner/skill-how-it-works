# skill-how-it-works

Build a polished, on-site `/how-it-works` page that explains a codebase's micro-systems in the site's own visual style. Produces prose with real code excerpts pinned to a commit SHA, hand-authored SVG diagrams in the site's palette, a sticky TOC with vanilla scrollspy, and de-slopified writing.

The output is shareable on Hacker News, Lobsters, internal docs, or as a standalone artifact — because it looks like the rest of the product, not a generic Markdown blog post.

## What it does

Walks the user through six phases:

1. **Brainstorm scope** — pick 5–7 concrete micro-systems to feature.
2. **Source the content** — read the actual code; mine session history for anecdotes.
3. **Detect the site** — extract palette, typography, generator, conventions.
4. **Build the skeleton** — content + template + CSS + diagram component + scrollspy.
5. **Author 5–7 SVG diagrams** in the site's palette.
6. **Write and de-slopify** the prose using Michael Lynch's principles.

Adapts to Zola, Hugo, Jekyll, Astro, Next.js, Eleventy, Gatsby, plain HTML, or falls back to a single self-contained HTML file when no static site is detected.

## Installation

```bash
cd ~/.claude/skills
ln -s ~/Developer/Personal/skill-how-it-works/skills/how-it-works how-it-works
```

## Usage

Trigger with any of:

- "Add a /how-it-works page to my site"
- "Build me an architecture explainer for this repo"
- "I want a HN-shareable writeup of how this works"

## Worked example

`swimfrancisco.com/how-it-works` is the original instance. A Zola + Cloudflare Worker site. Seven sections, hand-authored amber-on-navy SVG diagrams, right-rail TOC. Source: [github.com/cbzehner/swimfrancisco](https://github.com/cbzehner/swimfrancisco).

## License

MIT.
