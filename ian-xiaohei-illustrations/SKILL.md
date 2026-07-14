---
name: ian-xiaohei-illustrations
description: Generate Ian-style illustrations for English article body text. Used when users request generation of "whimsical," "Xiaohei," "hand-drawn," "body illustrations," "article illustrations," "illustration suggestions," "shot list," "detitling/image editing," and similar tasks for English articles, posts, blogs, Notion documents, workflow documentation, methodologies, processes, structures, states, metaphors, or viewpoints. Defaults to the Xiaohei IP, pure white hand-drawn style, sparse red-orange-blue annotations, and a clean yet wildly imaginative visual style.
---

# Ian Xiaohei Whimsical Body Illustrations

## Core Positioning

Design and generate 16:9 landscape body illustrations for English articles. The goal is not commercial illustration, PowerPoint infographics, or cute cartoons, but rather to turn the key judgments, processes, structures, states, or metaphors in the article into a clean, whimsical, creative, readable but not instruction-manual-like hand-drawn explanatory image.

The default visual IP is "Xiaohei": solid black, white-dot eyes, thin legs, blank expression, earnestly doing something absurd yet coherent. Xiaohei must participate in the core action of the scene—not just stand off to the side as decoration.

## Read These References First

Load as the task requires; don't cram the context all at once:

- `references/style-dna.md`: Style DNA, colors, text, taboos.
- `references/xiaohei-ip.md`: Xiaohei IP's appearance, personality, action library, and taboos.
- `references/composition-patterns.md`: Structure types, original metaphor methods, and anti-cliché rules.
- `references/prompt-template.md`: Single-image generation prompt template.
- `references/qa-checklist.md`: Post-generation checks and iteration rules.
- `assets/examples/`: For low-frequency visual calibration only; not part of the default generation path. Do not copy the composition, objects, or annotations of these examples.

## Workflow

### 1. Digest the Body Text

First read the body text, links, Notion pages, Markdown files, or screenshot content the user provides. Extract:

- What the core viewpoint is
- Which paragraphs carry the cognitive turning points
- Which content is suitable for explaining with an image
- Which parts are only suitable for text and don't need an image

Don't illustrate uniformly. Prioritize "cognitive anchors," such as: core judgments, two breakpoints, input-output loops, branching/splitting, before-and-after comparisons, one-input-many-outputs (repurposing), continuation paths, common pitfalls, character state changes.

### 2. Produce an Illustration Strategy First

If the user only says "analyze how to illustrate / think about where illustrations are needed," provide a shot list first. For each image, clearly write:

- Which paragraph it goes after
- The image's theme
- The core meaning
- The structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested English annotation words

Default 4-8 images. For very short articles, 1-3; even for long articles, don't easily exceed 9. Enough is enough—avoid turning the body text into a picture book.

### 3. Single-Image Generation

If the user explicitly requests "generate / output / make an image / help me generate," don't stop to wait for confirmation; use the built-in `image_gen` to generate each one separately. Don't combine multiple images into one.

Each image conveys only one core structure. The prompt must include:

- 16:9 landscape English body illustration
- Pure white background
- Black hand-drawn line art
- Sparse red/orange/blue English handwritten annotations
- Ample white space
- Xiaohei as the core action subject
- No PowerPoint, commercial illustration, childish cuteness, complex architecture, or top-left-corner type titles

Do not replicate past examples. Examples only provide style density and Xiaohei's mode of participation; you cannot directly reuse existing compositions like "conveyor belt breakpoint / Xiaohei pulling a string / material fish / stamp toolbox / common pitfall path," unless the user explicitly requests replicating a specific image. Each time, reinvent a strange but coherent metaphor from the current article.

### 4. Check and Iterate

After generation, check `references/qa-checklist.md`. If the following problems appear, prioritize regenerating or local editing:

- Xiaohei is just decoration
- The scene is too crowded
- Too much like a flowchart/PowerPoint
- Too much text or serious typos
- Titles like "common pitfalls / flowchart / system architecture diagram" appear in the top-left corner
- The style is too cute, childish, or rigid
- The background is not a clean white base

### 5. Save and Deliver

If the user is working within a workspace, copy the final images to:

```text
assets/<article-slug>-illustrations/
```

Name them in order:

```text
01-topic-name.png
02-topic-name.png
```

Keep the original generated files; don't overwrite existing assets unless the user explicitly requests replacement.

## Output Guidelines

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- The purpose of each image
- The save path
- Which images are most solid, and which are optional

Don't give lengthy explanations of style theory; let the images speak for themselves.
