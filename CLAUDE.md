# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

A static recipe website with no build step or dependencies. Open `index.html` directly in a browser to preview.

## Structure

- `index.html` — single-page site; contains all HTML, CSS, and inline styles
- `recipes/` — source content for each recipe in Markdown (one file per recipe)

## Content workflow

Recipe content lives in `recipes/*.md`. When adding or updating a recipe, reflect the change in the corresponding `<section>` inside `index.html`. Each section follows this structure:

```html
<section class="recipe" id="<kebab-case-name>">
  <img src="..." alt="..." />
  <div class="recipe-body">
    <h2>Title</h2>
    <p class="description">...</p>
    <h3>Ingredients</h3>
    <ul>...</ul>
    <h3>Steps</h3>
    <ol>...</ol>
    <a href="#" class="back-to-top">&#8593; Back to Top</a>
  </div>
</section>
```

Also add a matching `<a>` entry in the `<nav>` pointing to `#<id>`.
