# goldbach

## Build (macOS)

You can build the LaTeX document `main.tex` in two ways:

1) latexmk (recommended with VS Code LaTeX Workshop)
- Install a TeX distribution that includes `latexmk`:
	- Minimal: install BasicTeX from https://tug.org/mactex/morepackages.html
	- Full: install MacTeX from https://tug.org/mactex/
- Ensure `/Library/TeX/texbin` is on your PATH so VS Code can find `latexmk`.
	- Add to your shell profile (e.g. `~/.zprofile` or `~/.bash_profile`):
		`export PATH="/Library/TeX/texbin:$PATH"`
- Verify:
	- `latexmk -v`
- In VS Code, using the LaTeX Workshop extension, run Build (Recipe: latexmk).

2) Tectonic (single-binary alternative)
- Install: `brew install tectonic`
- Build from terminal: `tectonic main.tex`
- In LaTeX Workshop, set the recipe to use Tectonic if you prefer (see the extension docs).

### Notes
- The footer logo `KULEUVEN_GENT_RGB_LOGO.png` is optional; if present in the project root, it will be included automatically.
- This project uses common AMS/math packages and should build under TeX Live (MacTeX/BasicTeX) or Tectonic without extra configuration.
