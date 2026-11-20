# LaTeX CV with GitHub Actions

This repository stores a one-page LaTeX curriculum vitae and builds it
automatically with GitHub Actions.

## Pipeline

1. Check out the repository.
2. Compile `main.tex` into `main.pdf`.
3. Upload the PDF as a workflow artifact.
4. Create a GitHub Release with `main.pdf` attached.

Pull requests compile the CV without creating a release. Pushes to `main`
build and publish a new release.

## Source

- `main.tex`: CV source
- `.github/workflows/build-cv.yml`: build and release automation
