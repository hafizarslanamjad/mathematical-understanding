# Mathematical Understanding

**Mathematical Understanding** is a Quarto website containing long-form blogs about how people construct, preserve, and reason with mathematical meaning. The project examines mathematics not only as a formal system of symbols and rules, but also as an activity shaped by language, visual representation, conceptual models, prior knowledge, and explanatory design.

**[Read the blogs online](https://hafizarslanamjad.github.io/mathematical-understanding/)**

## Published Blog Posts

### Before Mathematics Begins

**How Language and Visual Representation Shape Mathematical Understanding**

This article investigates the representational work that occurs before formal mathematical reasoning begins. It argues that an explanation should be evaluated not only for mathematical correctness, but also for how effectively its language, notation, diagrams, examples, and sequence support the construction of a coherent mental model.

**[Read Before Mathematics Begins](https://hafizarslanamjad.github.io/mathematical-understanding/articles/before-mathematics-begins/)**

### When Symbols Stay the Same but Meaning Changes

**A Cognitive Framework for Preserving Context in Mathematical Reasoning**

This article examines silent contextual switching: a change in the conceptual model used to interpret an expression while its visible symbols remain unchanged. Using the fraction $5/5$ as its central case study, it develops a framework for preserving meaning within a model and translating explicitly when moving into another.

**[Read When Symbols Stay the Same but Meaning Changes](https://hafizarslanamjad.github.io/mathematical-understanding/articles/when-symbols-stay-the-same/)**

### The Reasoning Hidden Inside a Probability Calculation

**What the Expression \(210 \times \frac{4}{7}\) Requires a Learner to Understand**

This article reconstructs the reasoning hidden inside a seemingly simple probability calculation. It examines how quantities acquire mathematical roles, how a probability derived from regions becomes applicable to repeated trials, how units preserve meaning, and how multiplication compresses proportional scaling and accumulated expected contributions.

**[Read The Reasoning Hidden Inside a Probability Calculation](https://hafizarslanamjad.github.io/mathematical-understanding/articles/reasoning-hidden-inside-a-probability-calculation/)**

## Repository structure

```text
mathematical-understanding/
├── .github/
│   └── workflows/
│       └── publish.yml
├── articles/
│   ├── before-mathematics-begins/
│   │   ├── figures/
│   │   └── index.qmd
│   └── when-symbols-stay-the-same/
│       └── index.qmd
├── .gitignore
├── _quarto.yml
├── index.qmd
├── references.bib
├── styles.css
└── README.md
```

The root `index.qmd` is the website homepage. Each article has its own directory under `articles/` and uses `index.qmd` as its source filename, producing a clean directory-based URL when published. Article-specific figures remain with the article that uses them. Shared website configuration is defined in `_quarto.yml`, shared styling belongs in `styles.css`, and bibliographic records belong in `references.bib`.

The `.quarto/` and `_site/` directories may appear locally after previewing or rendering the website. They contain generated caches and rendered output and are not authoritative source content. They should remain excluded from version control.

## Requirements

Local development requires [Quarto](https://quarto.org/) and a text editor such as Visual Studio Code. Git is required for version control and publication through GitHub.

Verify the Quarto installation with:

```bash
quarto check
```

## Previewing the website locally

Open a terminal in the repository root and run:

```bash
quarto preview
```

Quarto renders the website, starts a local preview server, and refreshes the browser when a source file is saved. To stop the preview server safely, return to the terminal and press `Ctrl+C`.

Preview the complete website rather than an individual article so that navigation, shared styling, internal links, and project-level configuration are tested together.

## Rendering the website locally

Before publishing significant changes, perform a complete render:

```bash
quarto render
```

The generated website is written to `_site/`. This directory can be inspected locally, but it should not be committed because publication is handled automatically.

## Adding a new blog

Create a directory under `articles/` using a lowercase, hyphen-separated name:

```text
articles/article-name/
├── figures/
└── index.qmd
```

Add the article metadata and content to its `index.qmd`, store article-specific images in its `figures/` directory, and add a link and description to the root `index.qmd`. Internal website links should target Quarto source files rather than generated HTML files.

For mathematical notation, use `$...$` for inline mathematics and `$$...$$` for display mathematics. Mermaid diagrams can be included directly in Quarto Mermaid code blocks.

## Publication workflow

The `main` branch contains the authored source. The generated website is published to the `gh-pages` branch by the workflow in `.github/workflows/publish.yml`.

After editing and verifying the website locally, publish changes with the normal Git workflow:

```bash
git status
git add .
git commit -m "Describe the change"
git push
```

Every push to `main` triggers GitHub Actions. The workflow installs Quarto, renders the complete project, and publishes the result to GitHub Pages. Deployment progress can be inspected in the repository's **Actions** tab.

The published website is available at:

**[https://hafizarslanamjad.github.io/mathematical-understanding/](https://hafizarslanamjad.github.io/mathematical-understanding/)**

## Source and generated content

The Quarto files are the authoritative article sources. Generated HTML files should not be edited manually because they will be replaced during the next render. Corrections must be made in the relevant `.qmd` file, verified through `quarto preview` or `quarto render`, committed to `main`, and then deployed by the publishing workflow.

## Project status

The repository currently contains two article projects. *Before Mathematics Begins* has a complete conceptual draft. *When Symbols Stay the Same but Meaning Changes* has a complete structural draft and is undergoing source-level verification of mathematical rendering and presentation. Future revisions will add scholarly citations, refine visual explanations, consolidate repeated arguments where necessary, and prepare the blogs for possible publication in longer academic or book-length forms.

## Repository

The source is maintained at **[hafizarslanamjad/mathematical-understanding](https://github.com/hafizarslanamjad/mathematical-understanding)**.