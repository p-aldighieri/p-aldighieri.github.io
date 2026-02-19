# AGENTS.md

## Workspace Repositories
- Website repo: `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website`
- CV source repo: `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package`

## CV Refresh Workflow
Use this workflow when asked to update the website CV from the CV repository.

1. Pull latest CV changes:
   - `git -C /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package fetch origin`
   - `git -C /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package pull --ff-only origin main`

2. Build PDFs in the CV repo:
   - `cd /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package`
   - `latexmk -pdf CV-en-pedro-braga-soares.tex`
   - `latexmk -pdf CV-pt-pedro-braga-soares.tex`
   - If `latexmk` is unavailable, compile with `pdflatex` until references settle.

3. Copy outputs into website files:
   - `cp /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package/CV-en-pedro-braga-soares.pdf /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website/files/CV-pedro-braga-soares-en.pdf`
   - `cp /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package/CV-en-pedro-braga-soares.pdf /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website/files/CV-pedro-aldighieri-en.pdf`
   - `cp /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/CV_package/CV-pt-pedro-braga-soares.pdf /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website/files/CV-pedro-braga-soares-pt.pdf`

4. Verify website references and changes:
   - Confirm links in `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website/_pages/cv.md`.
   - Check changed files with:
     - `git -C /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website status --short`

## Naming Rule (Aldighieri vs Braga-Soares)
- Keep both English filenames updated to avoid broken links:
  - `CV-pedro-braga-soares-en.pdf` (new/current surname style)
  - `CV-pedro-aldighieri-en.pdf` (legacy compatibility)
- Keep Portuguese as:
  - `CV-pedro-braga-soares-pt.pdf`
- If website links are renamed later, update this file so source-to-target mapping stays explicit.
