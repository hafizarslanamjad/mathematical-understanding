# Mathematical Understanding

**Mathematical Understanding** is a Quarto website containing long-form articles and books about how people construct, preserve, communicate, and apply mathematical meaning. The project examines mathematics not only as a formal system of symbols and rules, but also as an activity shaped by language, visual representation, conceptual models, programming, prior knowledge, and explanatory design.

**[Visit Mathematical Understanding](https://hafizarslanamjad.github.io/mathematical-understanding/)**

## Book in Progress

### Mathematical Programming

**From Computational Meaning to Equations and Code**

This book develops the intellectual bridge between ordinary programming and mathematical representation. It begins with concrete computational examples and progressively teaches readers how to discover structures such as selection, counting, aggregation, weighting, normalization, state transitions, vectors, matrices, and tensor operations inside code.

The book is being written and published one comprehensive mini-section at a time. Its chapter structure remains provisional so that explanations, examples, and conceptual dependencies can be refined as the manuscript develops.

**[Read Mathematical Programming](https://hafizarslanamjad.github.io/mathematical-understanding/books/mathematical-programming/)**

#### Published Chapters

- **[Chapter 1 — Two Ways of Describing a Computation](https://hafizarslanamjad.github.io/mathematical-understanding/books/mathematical-programming/chapters/01-two-ways-of-describing-computation/)** explains how ordinary code can be examined for the mathematical relationship it implements.

- **[Chapter 2 — Boolean Values as Mathematical Objects](https://hafizarslanamjad.github.io/mathematical-understanding/books/mathematical-programming/chapters/02-boolean-values-as-mathematical-objects/)** develops conditions into binary numerical contributions and derives conditional counting as a sum of indicators.

## Published Blog Posts

### Before Mathematics Begins

**How Language and Visual Representation Shape Mathematical Understanding**

This article investigates the representational work that occurs before formal mathematical reasoning begins. It argues that an explanation should be evaluated not only for mathematical correctness, but also for how effectively its language, notation, diagrams, examples, and sequence support the construction of a coherent mental model.

**[Read Before Mathematics Begins](https://hafizarslanamjad.github.io/mathematical-understanding/articles/before-mathematics-begins/)**

### When Symbols Stay the Same but Meaning Changes

**A Cognitive Framework for Preserving Context in Mathematical Reasoning**

This article examines silent contextual switching: a change in the conceptual model used to interpret an expression while its visible symbols remain unchanged. Using the fraction $5/5$ as its central case study, it develops a framework for preserving meaning within a model and translating explicitly when moving into another.

**[Read When Symbols Stay the Same but Meaning Changes](https://hafizarslanamjad.github.io/mathematical-understanding/articles/when-symbols-stay-the-same/)**

### Structuring Probability Problem

**Fractions Needed for Probability**

This article reconstructs the reasoning hidden inside a seemingly simple probability calculation. It examines how quantities acquire mathematical roles, how a probability derived from regions becomes applicable to repeated trials, how units preserve meaning, and how multiplication compresses proportional scaling and accumulated expected contributions.

**[Read The Reasoning Hidden Inside a Probability Calculation](https://hafizarslanamjad.github.io/mathematical-understanding/articles/structuring-probability-problem/)**

### When Mathematics Changes the Expression

**Equivalence, Derived Quantities, and the Construction of Sample Variance**

This article investigates how mathematics rewrites existing quantities and constructs new ones without losing semantic control. Using sample variance as its central case, it explains subtraction as relative position, centering as a change of reference, squaring as quadratic measurement, and mathematical creativity as design under constraints.

**[Read When Mathematics Changes the Expression](https://hafizarslanamjad.github.io/mathematical-understanding/articles/when-mathematics-change-the-expression/)**

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
│   ├── structuring-probability-problem/
│   │   ├── figures/
│   │   │   └── spinner-probability-problem.png
│   │   └── index.qmd
│   ├── when-mathematics-change-the-expression/
│   │   └── index.qmd
│   └── when-symbols-stay-the-same/
│       └── index.qmd
├── books/
│   └── mathematical-programming/
│       ├── chapters/
│       │   ├── 01-two-ways-of-describing-computation/
│       │   │   └── index.qmd
│       │   └── 02-boolean-values-as-mathematical-objects/
│       │       └── index.qmd
│       └── index.qmd├── .gitignore
├── _quarto.yml
├── index.qmd
├── references.bib
├── styles.css
└── README.md
```

The root `index.qmd` is the website homepage. Each article has its own directory under `articles/` and uses `index.qmd` as its source filename, producing a clean directory-based URL when published. Books are stored under `books/`. The `books/mathematical-programming/index.qmd` file is the landing page for the book, while its chapter sources are stored under `books/mathematical-programming/chapters/`. Article-specific figures remain with the article that uses them. Shared website configuration is defined in `_quarto.yml`, shared styling belongs in `styles.css`, and bibliographic records belong in `references.bib`.

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

The repository currently contains four long-form articles and one book in progress. The articles examine mathematical understanding through explanatory representation, contextual preservation, the organization of probability problems, and the construction of mathematical expressions. The developing book, *Mathematical Programming: From Computational Meaning to Equations and Code*, investigates how computational requirements can be transformed into mathematical structures and then into executable programs.

## Repository

The source is maintained at **[hafizarslanamjad/mathematical-understanding](https://github.com/hafizarslanamjad/mathematical-understanding)**.
