# research-paper

Research paper from us!

## how-to Linux

1. Install Latex plugin,

```bash
apt install texlive-extra-utils latexmk -y
```

2. Install VSCode Latex extension, https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop

3. Everytime you save the tex file, it will automatically generate the pdf file.


## how-to macos

1. Install mactex plugin here https://www.tug.org/mactex/mactex-download.html or 

```bash 
brew install mactex
```


2. Install VSCode Latex extension, https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop

3. Configure vscode user settings.

  - Press Command+Shift+P, and open "Preferences: Open User Settings(JSON)" and append these lines:

```json
"latex-workshop.latex.tools": [
      {
        "name": "latexmk",
        "command": "latexmk",
        "args": [
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "-pdf",
          "-outdir=%OUTDIR%",
          "%DOC%"
        ],
        "env": {
          "PATH": "/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin:/Library/TeX/texbin:/Library/Apple/usr/bin"
        }
      },
    ],
    "latex-workshop.latex.recipes": [
      {
        "name": "latexmk 🔃",
        "tools": [
          "latexmk"
        ],
      },
    ],
    "latex-workshop.latex.clean.fileTypes": [
        "*.aux",
        "*.bbl",
        "*.blg",
        "*.idx",
        "*.ind",
        "*.lof",
        "*.lot",
        "*.out",
        "*.toc",
        "*.acn",
        "*.acr",
        "*.alg",
        "*.glg",
        "*.glo",
        "*.gls",
        "*.ist",
        "*.fls",
        "*.log",
        "*.fdb_latexmk",
        "*.snm",
        "*.nav",
    ],
```

  - Reload window
