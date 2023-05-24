# matse-spicker

# 3rd Semester
[![Stochastik](https://github.com/pblan/matse-spicker/actions/workflows/sto.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/sto.yml)

[![Softwaretechnik](https://github.com/pblan/matse-spicker/actions/workflows/swt.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/swt.yml)

[![Datenbanken](https://github.com/pblan/matse-spicker/actions/workflows/db.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/db.yml)

# 4th Semester
[![Numerik 1](https://github.com/pblan/matse-spicker/actions/workflows/num1.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/num1.yml)

[![Web-Engineerung und Internettechnologien](https://github.com/pblan/matse-spicker/actions/workflows/weit.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/weit.yml)

[![Kommunikationssysteme](https://github.com/pblan/matse-spicker/actions/workflows/kosy.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/kosy.yml)

# Compulsory Courses
[![Einführung in Data Science](https://github.com/pblan/matse-spicker/actions/workflows/ds.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/ds.yml)

[![Einführung in die Künstliche Intelligenz](https://github.com/pblan/matse-spicker/actions/workflows/ki.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/ki.yml)

[![Einführung in Machine Learning](https://github.com/pblan/matse-spicker/actions/workflows/ml.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/ml.yml)

[![Microcontrollertechnik](https://github.com/pblan/matse-spicker/actions/workflows/mct.yml/badge.svg)](https://github.com/pblan/matse-spicker/actions/workflows/mct.yml)


## VS Code Setup 
Um die Spicker einfach in Visual Studio Code mit der LaTeX Workshop Extension kompilieren zu können, kann man die Workspace Einstellung des _latexmk_ Rezeptes um die Umgebungsvariable _TEXINPUTS_ wie folgt ergänzen:

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
                "TEXINPUTS": ":.:%WORKSPACE_FOLDER%/latex-libs"
            }
        },
```