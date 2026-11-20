# LaTeX CV with GitHub Actions

This repository stores a LaTeX build wrapper for the CV source and builds it
automatically with GitHub Actions. The original PDF pages are embedded through
the `pdfpages` package so the layout remains unchanged.

## Pipeline

1. Check out the repository.
2. Compile `main.tex` into `main.pdf`.
3. Upload the PDF as a workflow artifact.
4. Create a GitHub Release with `main.pdf` attached.

Pull requests compile the CV without creating a release. Pushes to `main`
build and publish a new release.

## Source

- `main.tex`: LaTeX build wrapper
- `source_cv.pdf`: original CV pages
- `.github/workflows/build-cv.yml`: build and release automation
