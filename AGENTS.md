# AGENTS.md

## Workspace Repositories
- Website repo: `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website`
- CV source repo: `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package`

## CV Refresh Workflow
Use this workflow when asked to update the website CV from the CV repository.

1. Pull latest CV changes:
   - `git -C /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package fetch origin`
   - `git -C /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package pull --ff-only origin main`

2. Build the English PDF in the CV repo:
   - `cd /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package`
   - `latexmk -pdf CV-en-pedro-braga-soares.tex`
   - If `latexmk` is unavailable, compile with `pdflatex` until references settle.

3. Copy output into website files:
   - `cp /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package/CV-en-pedro-braga-soares.pdf /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website/files/CV-pedro-aldighieri-en.pdf`

4. Verify website references and changes:
   - Confirm links in `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website/_pages/cv.md`.
   - Check changed files with:
     - `git -C /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website status --short`

## Naming Rule
- Keep the public English CV filename as:
  - `CV-pedro-aldighieri-en.pdf`
- Do not recreate removed Braga-Soares English or Portuguese CV PDFs unless website links are intentionally changed again.
- If website links are renamed later, update this file so source-to-target mapping stays explicit.
