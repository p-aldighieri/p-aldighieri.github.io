# AGENTS.md

## Workspace Repositories
- Website repo: `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website`
- CV source PDF (already built — do not compile it): `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Pessoais/Currículo & Carreira/CVs/CV-pedro-aldighieri-en.pdf`

## CV Refresh Workflow
Use this workflow when asked to update the website CV. The source is a built PDF, not a LaTeX repo — just copy it over. Do not try to compile anything.

1. Copy the source PDF into website files:
   - `cp "/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Pessoais/Currículo & Carreira/CVs/CV-pedro-aldighieri-en.pdf" /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website/files/CV-pedro-aldighieri-en.pdf`

2. Verify website references and changes:
   - Confirm links in `/Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website/_pages/cv.md`.
   - Check changed files with:
     - `git -C /Users/p-aldighieri/Library/CloudStorage/OneDrive-Personal/Codebook/Website status --short`

## Naming Rule
- Keep the public English CV filename as:
  - `CV-pedro-aldighieri-en.pdf`
- Do not recreate removed Braga-Soares English or Portuguese CV PDFs unless website links are intentionally changed again.
- If website links are renamed later, update this file so source-to-target mapping stays explicit.
