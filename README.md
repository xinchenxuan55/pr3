# LaTeX CV with GitHub Actions

This repository contains the CV as editable LaTeX source and builds it
automatically with GitHub Actions. The source was reconstructed from the
applicant's existing CV and keeps its one-page, two-column structure.

## Pipeline

1. Check out the repository.
2. Compile `main.tex` into `main.pdf`.
3. Upload the PDF as a workflow artifact.
4. Create a GitHub Release with `main.pdf` attached.

Pull requests compile the CV without creating a release. Pushes to `main`
build and publish a new release.

## Source

- `main.tex`: editable LaTeX CV source
- `photo.png`: portrait used by the header
- `.github/workflows/build-cv.yml`: build and release automation
