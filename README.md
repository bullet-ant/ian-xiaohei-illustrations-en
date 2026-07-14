# Ian Xiaohei Illustrations

> Turn the judgments, processes, states, and metaphors in articles into white-background, hand-drawn, quirky-but-clean in-article illustrations.
>
> 16:9 landscape | Xiaohei IP | pure white hand-drawn | sparse red/orange/blue annotations | Codex Skill

---

## What is this repo

Ian Xiaohei Illustrations is a Codex Skill that guides an AI agent to generate in-article illustrations for articles, posts, blogs, Notion docs, and methodology content.

It is not a generic illustration prompt, nor a PPT infographic template. Its core goal is: first understand the cognitive anchor points in the article, then turn one judgment, process, structure, state, or metaphor into a memorable 16:9 hand-drawn explanatory image.

The default visual IP is "Xiaohei" (小黑): a small character with a solid black body, white dot eyes, thin legs, and a blank expression. Xiaohei is not a mascot, not a sticker, and not decoration standing in the corner — it's an absurdist worker seriously participating in the operation of the system.

In one sentence: **make AI not just "add an illustration," but draw out one key cognitive action from the article.**

---

## Who is this for

Especially good for:

- People writing articles who need in-article illustrations
- People creating knowledge-based content, methodology content, or AI workflow content
- People who want to turn abstract judgments into concrete metaphors
- People who want an illustration style that's lighter, weirder, and more personally distinctive than a PPT infographic
- People using Codex for content production who want a consistent, reusable visual language

Not a good fit for:

- People who want commercial illustration, brand key visuals, or polished flat illustration
- People who want traditional PPT infographics, complex architecture diagrams, or flowcharts
- People who want children's cartoons, cute IP characters, or emoji/sticker styles
- People who want to cram large blocks of text, long explanations, or a full course page into one image
- People who need strictly editable vector source files

---

## What it produces

Default output:

- 16:9 landscape in-article illustrations
- A shot list of 4-8 images per article
- For each image: theme, core meaning, structure type, Xiaohei's action, and suggested annotation text
- Final PNG images, saved to the workspace's `assets/<article-slug>-illustrations/`

Not output by default:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable graphics
- Commercial posters or cover key visuals
- Text-heavy infographics

---

## Visual style

This skill uses Ian's "Xiaohei absurdist in-article illustration" style by default:

- Pure white background — no paper texture, beige tones, shadows, or gradients
- Black hand-drawn line art, thin lines, slight jitter
- Generous white space — the subject occupies only about 40%-60% of the frame
- A sparse amount of red, orange, and blue handwritten annotations
- Each image expresses only one core action, structure, state, or metaphor
- Xiaohei must participate in the core action — never just decoration
- Quirky, creative, and clean, but never childish or cutesy

---

## Example results

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sort by Purpose

![Sort by Purpose](examples/images/02-sort-by-purpose.png)

### One Fish, Many Uses

![One Fish, Many Uses](examples/images/03-one-fish-many-uses.png)

### Handoff Path

![Handoff Path](examples/images/04-handoff-path.png)

### Information Well

![Information Well](examples/images/05-information-well.png)

### Idea Press

![Idea Press](examples/images/06-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/07-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/08-trust-bridge.png)

These images are style calibration samples, not composition templates. When using the skill, reinvent the metaphor from the current article — don't copy the objects or composition of old examples.

---

## Installation

Clone the repo:

```bash
git clone https://github.com/helloianneo/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

Copy the skill into the Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

After installing, use it in Codex like this:

```text
Use $ian-xiaohei-illustrations to design and generate 5 Xiaohei absurdist in-article illustrations for this article.
```

---

## How to use it

### Planning illustrations only

```text
Use $ian-xiaohei-illustrations. Don't generate images yet.
Analyze the article below for where illustrations would add value, and output a shot list of about 5 images.
For each image, specify: which paragraph it follows, theme, core meaning, structure type, what Xiaohei is doing, and suggested annotation words.

<paste article>
```

### Generating in-article illustrations directly

```text
Use $ian-xiaohei-illustrations to generate 4 Xiaohei absurdist in-article illustrations for the article below.
Requirements: 16:9 landscape, pure white background, black hand-drawn line art, sparse red/orange/blue handwritten annotations.

<paste article>
```

### Generating one image for a single concept

```text
Use $ian-xiaohei-illustrations to generate one in-article illustration for: "Trust isn't shouted into existence — it's laid down piece by piece, one piece of evidence at a time."
The image should be quirky but clean, and Xiaohei must carry out the core action.
```

### Removing a title or incorrect text from an image

```text
Use $ian-xiaohei-illustrations to help me edit this image — remove the "Flowchart" title in the top-left corner, keep everything else unchanged.
```

See more examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

This skill's process:

1. Read the article, Markdown, Notion content, screenshot, or topic provided by the user
2. Extract the core ideas, cognitive turning points, process structures, and passages suited for visualization
3. Output a shot list first: pick only one cognitive anchor per image
4. Choose a structure type for each image: workflow, system component, before/after comparison, character state, conceptual metaphor, method layering, map/route, or mini comic panel
5. Reinvent a low-tech, absurd but coherent physical metaphor
6. Have Xiaohei carry out the core action
7. Call the image model separately for each image
8. Check against the QA checklist: white background, white space, Xiaohei's action, annotations, not PPT-like, not a copy of old examples
9. Save the final PNG and report its purpose and path

---

## Directory structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The subdirectory that actually needs to be installed into Codex is:

```text
ian-xiaohei-illustrations/
```

The root-level README, LICENSE, NOTICE, and examples are GitHub-facing documentation.

---

## Notes

- The shorter the text in an image, the more stable the result.
- Each image should convey only one core structure — don't turn the article into an instruction manual.
- Xiaohei must carry out the core action; if the image would still fully work with Xiaohei removed, that means Xiaohei is too decorative.
- The example images are only for calibrating line density, white space, restrained color use, and how Xiaohei participates — don't replicate their compositions.
- AI image models may produce typos, hallucinated labels, style drift, or extraneous titles — check the output after generation.
- If the text has serious typos, prioritize reducing the amount of annotation text and regenerate.

---

## Related projects

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — a hand-drawn technical PPT-style slide generation skill
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — a curated collection of Claude Code Skills / Agents / Plugins
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — a guide to building a personal knowledge base with Obsidian + Claude AI

---

## About the author

**Ian** — Product designer / solo-company practitioner / AI builder

Building a one-person company with a team of AI.

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Website: [www.ianneo.xyz](https://www.ianneo.xyz)
- WeChat: `ianneoxyz`
- Email: hello.neoc@gmail.com

---

## Keep exploring

This Xiaohei illustration skill is just one small tool in the personal production system I'm building with AI.

If you're also using AI for content, knowledge bases, workflows, or productization, check out my website: [www.ianneo.xyz](https://www.ianneo.xyz).

If you just want to observe for now, follow my [X/Twitter](https://x.com/ianneo_ai).

To learn about the Indie Builders Club, add me on WeChat: `ianneoxyz`, note "OPC".

<p>
  <img src="assets/ian-wechat-qr.jpg" alt="Ian's WeChat QR code" width="120">
</p>

If scanning isn't convenient, you can also search for WeChat ID: `ianneoxyz`.

---

## License

MIT License. See [LICENSE](LICENSE).
