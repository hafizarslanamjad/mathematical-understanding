# Before Mathematics Begins

This repository contains the source and rendered HTML version of **Before Mathematics Begins: How Language and Visual Representation Shape Mathematical Understanding**, an article by Hafiz Arslan Amjad.

The article investigates a process that occurs before formal mathematical reasoning: the learner must interpret external representations and organize them into a mental model. Its central argument is that mathematical explanations should be evaluated not only for correctness, but also for how effectively their language, notation, diagrams, examples, and sequence support the construction of meaning.

Mathematical equations or other mathematical subjects may appear as case studies, but they are not the primary subject. The article is concerned with the design of mathematical explanations and draws conceptually from cognitive psychology, instructional design, linguistics, and mathematics education.

## Central ideas

The article develops several connected claims:

- mathematical reasoning depends on prior representational construction;
- information may be present even when its relationships remain difficult to perceive;
- learners must reconstruct relationships that explanations leave implicit;
- productive mathematical inference should be distinguished from avoidable interpretive repair;
- prior knowledge helps explain why experts and beginners perceive the same explanation differently;
- explanatory design should direct cognitive effort toward the intended mathematics.

## Repository contents

- `article.qmd` — the primary Quarto source containing the prose, LaTeX mathematics, tables, and Mermaid diagrams.
- `article.html` — the rendered standalone HTML article.
- `README.md` — an overview of the project and instructions for working with the source.

The Quarto source is the authoritative version of the article. The HTML file should be regenerated whenever the source changes.

## Requirements

To render or preview the article locally, install [Quarto](https://quarto.org/) and use a text editor such as Visual Studio Code. A modern web browser is required to view the HTML output.

## Previewing the article

Open a terminal in the repository directory and run:

```bash
quarto preview article.qmd
```

Quarto will render the article, start a local preview server, and normally open the result in a browser. Changes saved to `article.qmd` will be reflected in the preview. To stop the preview server safely, return to the terminal and press `Ctrl+C`.

## Rendering the article

To create the HTML output without starting a preview server, run:

```bash
quarto render article.qmd --to html
```

The rendered result will be written to `article.html` unless the project configuration specifies another output location.

## Project status

The main conceptual argument and conclusion have been drafted. Future revisions may consolidate overlapping passages, improve individual visualizations, add scholarly citations, verify claims against relevant research, and refine the article for possible publication as a research paper or book chapter.

## Repository

The project is maintained at [hafizarslanamjad/mathematical-understanding](https://github.com/hafizarslanamjad/mathematical-understanding).