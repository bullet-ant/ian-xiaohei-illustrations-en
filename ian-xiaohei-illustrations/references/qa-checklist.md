# QA Checklist

## Must-Pass Items

- Is 16:9 landscape.
- Background is a clean white base.
- Has Xiaohei.
- Xiaohei takes on the core action, not just decoration.
- Did not replicate an old case composition, but generated a new metaphor for the current article.
- The scene is whimsical, creative, and interesting.
- Clean and uncluttered; the main subject occupies no more than about 60% of the scene.
- One image conveys only one core structure.
- English annotations are few, short (1-3 words each), and readable.
- All English words are spelled correctly.
- Orange is used only for the main path or arrows.
- Red is used only for key points, problems, warnings, or results.
- Blue is used only for supplementary notes, feedback, or system state.

## Failure Signals

If the following occur, regenerate or do local editing:

- The top-left corner has a title like "common pitfalls / Workflow / system architecture diagram / roadmap."
- Xiaohei looks like a mascot, meme, or cute cartoon.
- The scene looks like a PowerPoint, course slides, or a formal flowchart.
- Too many elements, too many arrows, too many nodes.
- The text turns into long explanatory sentences.
- The background has paper texture, shadows, gradients, beige tones, or noise.
- A realistic UI screenshot or techy interface.
- Misspelled English words or unreadable labels.
- The scene is too rigid, with no absurd metaphor.
- Too similar to an old case composition in `assets/examples/`.

## Iteration Methods

- Too ordinary: make Xiaohei the action subject and add a strange but coherent metaphor.
- Too complex: cut nodes, keep only one action and 3-5 short labels.
- Too cute: emphasize deadpan, blank serious expression, not cute, not mascot.
- Too PowerPoint: remove the title, borders, tidy grids, and excess arrows; switch to a hand-drawn scene.
- Too much like an old case: keep the core meaning, swap out the main object and Xiaohei's action.
- Text errors: prioritize local editing (see the "fix a misspelled label" prompt); if there are many errors, regenerate and reduce the number of labels.

## Delivery Judgment

A high-quality image should make the reader first feel "a bit weird," then grasp the structure within 1 second.
If the first impression is a tutorial page rather than an absurd product sketch on white paper, it fails.