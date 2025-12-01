# AI Agent Instructions

## Purpose

The primary goal for you is to write clear, concise, and well-structured documentation using Markdown.

## Guidelines

1. **Use Markdown Syntax:**

- Headings, lists, code blocks, tables, links, and images should follow standard Markdown formatting.

2. **Clarity and Brevity:**

- Write in simple, direct language.
- Avoid unnecessary jargon or complex sentences.

3. **Structure:**

- Organize documentation with appropriate headings and subheadings.
- Use bullet points or numbered lists for steps and key points.
- Separate different subjects into different pages
- Make sure that each file starts with an order number. (e.g. 1-Home.md)
- Put all docs in a `docs` folder in the root of the repository.
- Make sure that the 1-Home.md file only contains a small introduction with links to all other pages

4. **Code Examples:**

- Include code snippets in fenced code blocks.
- Add brief explanations above or below code samples.

5. **Consistency:**

- Maintain consistent formatting throughout the document.
- Use the same terminology for recurring concepts.

6. **Audience Awareness:**

- Tailor documentation to the intended audience, being developers and technical people.
- Provide context or prerequisites when necessary.

7. **References:**

- Link to external resources or related documentation when helpful.
- Use the `Microsoft Docs MCP` as a reference.

8. **Azure DevOps Wiki:**

- The docs will be published on Azure DevOps wiki's
- Make sure that each page is referenced in a `.order` file (see [here](https://learn.microsoft.com/en-us/azure/devops/project/wiki/wiki-file-structure?view=azure-devops)). If no .order file exists, please create one.
- Make sure each page has a table of contents. Use the `[[_TOC_]]` placeholder for this

9. **Diagrams:**

- Use diagrams to illustrate complex concepts or workflows.
- Use the [Mermaid](https://mermaid-js.github.io/mermaid/#/) syntax for creating diagrams in Markdown.
- Make sure mermaid diagrams are wrapped in a code block with `::: mermaid` as start tag and `:::` as the end tag so it is supported in Azure DevOps.
