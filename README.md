# Article Study Notes Skill

This repository contains one installable Codex skill:

- `article-study-notes`

The skill turns articles, book chapters, lecture slides, PDFs, EPUBs, Markdown files, reports, interviews, speeches, literature, policy documents, technical papers, folders, and other substantial text materials into reusable Markdown study notes.

It confirms the note language and depth before drafting when they are unspecified, writes a `.md` file by default, and supports restrained Markdown enhancements when they remain readable as ordinary Markdown.

It chooses different narrative structures for different material types: research articles, empirical studies, technical papers, reviews, theory essays, textbook chapters, lecture handouts, primary texts, case studies, reports, and multi-source folders.

For complex, broad, or controversial materials, it asks before adding external web/database scholarship. If external scholarship is used, it is clearly marked; if it is not used, the note says so briefly.

## Structure

```text
article-study-notes/
|-- SKILL.md
|-- evals/
|   |-- basic_acceptance.md
|   `-- evals.json
`-- references/
    |-- discipline-adapters.md
    |-- material-type-structures.md
    |-- output-formats.md
    |-- review-article-patterns.md
    |-- runtime-contract.md
    `-- source-quality.md
```

## Installation

Install or copy the `article-study-notes/` folder into your Codex skills directory. The installable skill folder is `article-study-notes`; the surrounding repository provides packaging, documentation, evaluation context, and licensing.

## Design

The runtime contract in `references/runtime-contract.md` guides the model's internal reading process: document profile, content map, scholarship map, and output plan. The final note should not expose that internal checklist unless the user asks for an audit.

Markdown enhancements are designed to stay portable. The skill should mention that Obsidian is excellent for long-term knowledge bases, Typora is convenient for local reading and export, GitHub/GitLab are useful for publishing and collaboration, and VS Code with Mermaid preview extensions works well for project-based notes. Vault-specific assumptions should be avoided unless the user provides local instructions.
