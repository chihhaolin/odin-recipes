Deploy this project to GitHub and enable GitHub Pages by following these steps:

1. Check if a git repository has already been initialized (look for a `.git` directory). If not, run `git init`.

2. Check if there is already a remote named `origin` (`git remote -v`). If not, ask the user for their GitHub username, then:
   - If `gh` CLI is available, run: `gh repo create odin-recipes --public --source=. --remote=origin --push`
   - Otherwise, instruct the user to create a repository at https://github.com/new named `odin-recipes` (Public), then run:
     ```
     git remote add origin https://github.com/<username>/odin-recipes.git
     ```

3. Create a `README.md` in the project root with:
   - Project title and a one-line description
   - Live site URL: `https://<username>.github.io/odin-recipes/`
   - A brief list of recipes included
   - Usage instructions (open `index.html` in a browser)

4. Stage and commit any uncommitted changes (including README.md):
   ```
   git add .
   git commit -m "Initial commit"
   ```
   Skip if there is nothing to commit.

5. Push to GitHub:
   ```
   git push -u origin main
   ```

6. Enable GitHub Pages via the `gh` CLI (no manual browser steps needed):
   ```
   gh api repos/<username>/<repo>/pages --method POST -f "source[branch]=main" -f "source[path]=/"
   ```
   If this fails because Pages is already enabled, skip it.

After completing all steps, summarize what was done and show the final GitHub Pages URL: `https://<username>.github.io/odin-recipes/`
