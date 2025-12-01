# ADO Wiki Documentation Instructions

## Description
This folder contains guidance and guardrails for writing clear, concise, and well-structured technical documentation in Markdown that will be published to Azure DevOps Wikis. The primary reference is `copilot-instructions.md`, which defines style, structure, and workflow expectations for contributors and AI assistants.

## Authors
- Robin Agten (robin.agten@delaware.pro)

## Features
- Markdown-first approach: headings, lists, code blocks, tables, links, and images follow standard Markdown.
- Clarity and brevity: simple, direct language; avoid jargon and overly complex sentences.
- Structured docs: organize with headings/subheadings and lists; separate topics into individual pages.
- Repository layout: put all docs in a root-level `docs` folder; prefix filenames with an order number (e.g., `1-Home.md`).
- Home page guidance: `1-Home.md` contains a short intro plus links to all other pages.
- Code examples: use fenced code blocks and add a short explanation.
- Consistency: keep formatting and terminology consistent across pages.
- Audience focus: write for developers/technical readers; include context and prerequisites where helpful.
- References: link to external resources and prefer the Microsoft Docs MCP for authoritative sources.
- Azure DevOps Wiki integration: include a `[[_TOC_]]` placeholder for table of contents; ensure each page is listed in a `.order` file (create one if missing).
- Diagrams with Mermaid: use Mermaid for workflows/architecture; wrap diagrams inside code fences using `::: mermaid` and end with `:::` for Azure DevOps compatibility.
