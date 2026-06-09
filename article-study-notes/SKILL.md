---
name: article-study-notes
description: Use when turning any substantial text material, including articles, book chapters, lecture slides, EPUB chapters, PDFs, Word files, Markdown, reports, essays, interviews, speeches, literature, classical texts, policy documents, technical papers, or folders of materials into high-quality Markdown study notes, with portable Markdown enhancements available when useful, grounded in the source text and clearly marked scholarship.
---

# Article Study Notes

## Purpose

Create high-quality learning notes for the user's future self. The output should preserve the source's core logic and important content rather than repeat the source paragraph by paragraph.

Do not produce assignment prose, source ledgers, prompt transcripts, OCR reports, review logs, or language that exposes the working process. The finished note should read as a reusable study object.

The note must be information-preserving. Do not compress unfamiliar or difficult material so aggressively that the future reader loses definitions, argument steps, evidence, examples, narrative structure, imagery, methods, limitations, objections, replies, or conclusion boundaries.

## Interaction Defaults

Before generating the final note, ask the user when any of these choices are not already clear:

- Note language.
- Depth: `concise`, `standard`, or `deep`.
- Whether to use portable Markdown enhancements. Mention that the generated `.md` file works especially well with Obsidian for long-term retrieval, backlinks, tags, concept hubs, and graph-style note systems; Typora for local reading and export; GitHub/GitLab for publishing and collaboration; and VS Code with Mermaid preview extensions for project-based notes. Enhancements must remain readable as ordinary Markdown.
- For folders or multiple files: whether to create one integrated note, process files one by one, or use another structure.
- For complex, broad, or controversial materials: whether to supplement with web/database scholarship.
- Destination and filename for the `.md` file, unless local workspace instructions already define them.

If the material is too long for one pass, process it in batches and then produce one integrated note. Keep the user informed about the batch plan.

## Inputs

Use the user's provided material and preferences:

- Source material: any substantial text material, including PDF, PPTX/PPT, Word, EPUB, Markdown, TXT, web-exported text, extracted text, transcript, report, article, essay, literary text, classical text, legal/policy text, or a local folder of materials.
- Discipline, course, or topic, if provided.
- Note language: confirm before drafting unless already specified.
- Output format: write a `.md` file by default. Prompt the user that the note can use portable Markdown enhancements for tools such as Obsidian, Typora, GitHub/GitLab, and VS Code. Use plain Markdown as the baseline; enhancements may be used when the user agrees or when local instructions request them, and they must remain readable as Markdown.
- Depth: ask the user to choose `concise`, `standard`, or `deep` unless already specified.
- Local reference folders supplied by the user, such as primary texts, secondary literature, reading packets, lecture-specific folders, datasets, appendices, or bibliographies.

If the material cannot be read reliably or is too fragmentary to support a good note, explain what is missing and ask for a text extract, clearer source, or permission to produce a limited note.

## Workflow

1. Build the internal runtime contract from `references/runtime-contract.md`.
2. Diagnose the material internally:
   - document profile
   - content map
   - scholarship map
   - output plan
3. Select the material-type structure. Read `references/material-type-structures.md` before drafting so the note follows the source's genre: research article, empirical article, technical paper, review, theory essay, book chapter, lecture, primary text, case study, report, or multi-source folder.
4. Select the discipline adapter. Read `references/discipline-adapters.md` when the material involves philosophy, humanities, social sciences, AI, business/management, finance, or AI-business overlap.
5. If the material is a review, survey, state-of-the-art article, overview, handbook, encyclopedia, or literature-review article, also read `references/review-article-patterns.md`.
6. Use source hierarchy and citation rules from `references/source-quality.md` when adding scholarly discussion. For complex, broad, or controversial material, ask before supplementing with web/database scholarship.
7. Use `references/output-formats.md` to render portable Markdown. If the user has not chosen, briefly explain that Obsidian, Typora, GitHub/GitLab, and VS Code can all work well with `.md` notes, with different strengths.
8. Draft the final note and save it as a `.md` file.
9. Verify the `.md` file exists at the intended destination.
10. Run the final quality check before delivery.

## Course Or Local Profile Mode

Use this mode when the material belongs to a recurring course, seminar, lecture sequence, reading group, or the user's established local note workflow.

Source order:

1. User instructions define destination, filename, language, note shape, and special conventions.
2. Course materials, lecture slides, syllabi, or assigned readings define the session boundary, title, examples, and emphasis.
3. A user-designated primary text, textbook, article, monograph, or reading packet provides the main argumentative or conceptual order when it is more coherent than slide order.
4. User-added local folders supplement the note when they clarify concepts, textual basis, empirical evidence, methods, scholarly dispute, or background.
5. External web or database sources are supplementary and require user confirmation unless the user already requested scholarly expansion. Use them to verify bibliographic details, locate primary passages, and expand high-value scholarly background without displacing the local source hierarchy.

Writing rules:

- Before drafting, identify the course/session unit, the controlling source, and auxiliary sources.
- Preserve the controlling source's argument order inside each section when that order is visible. Compress by removing repetition and low-value examples, not by rearranging the logic.
- Make the final prose source-grounded but not source-led. Avoid phrases like `the slides say`, `the textbook mentions`, `after searching`, `the material shows`, or similar process language unless the user asks for an audit.
- Integrate lecture or classroom material as examples, emphasis, or supplementary explanation within the relevant conceptual or argumentative node.
- For primary texts, classic passages, legal provisions, formulas, datasets, or other source anchors, quote only short passages that carry conceptual, evidential, or argumentative weight. Immediately explain what the quoted item does in the argument.
- If a quotation or passage location cannot be verified, paraphrase it rather than presenting it as a direct quotation.
- Use tables, diagrams, section summaries, or concept maps only when they reduce cognitive load. They are not mandatory.
- If local workspace instructions define destination, filename, language, or note shape, follow them for the current workspace. Do not treat those local preferences as universal skill behavior.

## Depth And Coverage

Default to enough detail for a reader who has not read the source recently. A good note is not a short abstract; it is a reusable learning object.

Preserve, when present:

- the source's motivating problem and background setup
- key terms with definitions and nearby distinctions
- the author's main claim, subclaims, premises, evidence, and reasoning steps
- important examples, cases, experiments, data, formulas, or textual passages
- stated limitations, scope conditions, objections, and replies
- what the conclusion proves and what it does not prove

Compression rules:

- Condense repetition, rhetoric, literature lists, and low-value procedural detail.
- Do not omit a step merely because it is intermediate; omit it only if it does not affect understanding.
- For unfamiliar, classic, technical, or concept-dense material, prefer `standard` or `deep` depth unless the user asks for a brief note.
- Use tables, diagrams, or bullet structures to hold detail cleanly rather than replacing detail with vague summary.

## Default Note Structure

Use this only as a fallback. Prefer the narrative structure for the material type in `references/material-type-structures.md`, then adapt it to the discipline and user context.

```markdown
# Title

Reading path: discipline; material type; reading focus.

Opening orientation: a few paragraphs that identify the problem, stakes, source hierarchy, and reading route.

## 1. Core Problem

## 2. Concepts And Framework

## 3. Argument Or Explanation

## 4. Scholarly Discussion

## 5. Understanding Points

## Argument Summary Or Key Takeaways

## Key Concept Table

## References
```

Adapt section names and language to the user's chosen note language and context. For philosophy, prefer the philosophy structure in `references/discipline-adapters.md`.

Use the closing summary and concept table when the material is complex enough to benefit from retrieval aids. They should synthesize the note rather than replace the main explanation.

## Hard Rules

- Base the main reconstruction on the source material.
- Separate source reconstruction from external scholarly discussion.
- Cite external scholarly sources in a references section using the note's chosen language.
- Ask before using external scholarly expansion. Recommend it for complex, broad, or controversial material, aiming for 4-6 high-weight, verifiable academic sources where available when the user agrees.
- Treat 4-6 as a target, not a quota; never use low-quality sources to fill the count.
- Keep external scholarship embedded in the relevant substantive nodes unless a standalone discussion section is clearer.
- Do not invent authors, titles, years, page numbers, DOIs, URLs, textual locations, formulas, data, or citations.
- Do not pad the note to hit a fixed length.
- Do not over-compress source reconstruction into a high-level abstract.
- Do not add personal reflections unless the user explicitly asks.
- Do not force Mermaid diagrams; use them only when they clarify structure.
- Do not expose the review process in final notes. Avoid `source says`, `slides mention`, `OCR`, `checked`, `pending`, page ledgers, or self-check language unless the user asks for a working audit.

## Final Quality Check

Before delivery, verify:

- The note is not just paragraph-by-paragraph summary.
- The core question, concepts, argument, and conclusions are clear.
- The note language was confirmed before drafting.
- The note was saved as a `.md` file.
- The generated `.md` file exists at the intended destination.
- For classical, literary, narrative, or canonical texts, the source's own order, narrative movement, imagery, rhetoric, and historical context are preserved instead of being forced into argument reconstruction.
- Definitions, distinctions, argument steps, evidence, examples, and limitations are preserved when they matter.
- Scholarly discussion is traceable to references.
- If external scholarship was not added, the note says so briefly in the references or source note area.
- External scholarship supports the source reconstruction without taking over the note's main structure.
- Markdown is readable across common Markdown tools.
- The user was prompted that `.md` notes can work well with Obsidian, Typora, GitHub/GitLab, and VS Code, with different strengths.
- Markdown enhancements, if used, remain valid Markdown and do not dominate the note.
- The narrative structure fits the material type; the note does not force every source into the same generic outline.
- Opening orientation, summaries, tables, and diagrams help the reader navigate; they do not become decorative scaffolding.
- The note is information-preserving: concise where the source is simple, deeper where the source is difficult or unfamiliar.
